<script type="text/javascript">
  $(document).ready(function(){
    
    
    /////////////////////////////////////////////////////////////////////////////////
    $('.select_size').change(function(){
      $('#Variants-i option').removeClass('selected_item');
      var _this = $(this);
      var opt_1 = _this.val();
      var opt_2 = _this.parents('.bundle__product_variant').find('.select_color option:selected').val()
      var option = opt_1 + ' / ' + opt_2 ;
      var select = _this.parents('.bundle__products').find('.main_select')
      select.find('option').each(function(){
        var variant = $(this).attr('data-title');
        if(variant == option){
          //console.log('variant: '+ variant);
          console.log('yesy' + variant, option)
          _this.parents('.bundle__products').find('.main_select option').removeAttr('selected');
          $(this).attr('selected', 'selected').trigger('change');
        }
      });
    });

    
    $('.select_color').change(function(){
      var _this = $(this);
      var opt_1 = _this.val();
      var opt_2 = _this.parents('.bundle__product_variant').find('.select_size option:selected').val()
      var option = opt_2 + ' / ' + opt_1 ;
//       var ftrdimg = $('.bundle__product_first_featured_image img').attr('srcset', );
      var select = _this.parents('.bundle__products').find('.main_select')
      select.find('option').each(function(){
        var variant = $(this).attr('data-title');
        var image = _this.parents('.bundle__products').find('.main_select option:selected').attr('data-image');;
        console.log(image)
        if(variant == option){
          //console.log('variant: '+ variant);
          //console.log('yesy' + variant, option)
          _this.parents('.bundle__products').find('.main_select option').removeAttr('selected');
          $(this).attr('selected', 'selected').trigger('change');
        }
        $(this).parents('.bundle__product_sides').find('.bundle__product_first_featured_image img').attr('srcset', image)
      });
    });
    //////////////////////////////////////
    $(document).on('click', '.cutom_atc', function(e) {
      e.preventDefault();
      $('select[name="id"] option:selected').each(function(){
        var checkValues = $(this).val();
        //console.log('checkValues ' +checkValues);        
        $.ajax({
          type: "post",
          url: '/cart/add.js',
          data: {
            id: checkValues,
            quantity: 1,
//             properties: { "bundle": "Bundle Product" }
          },
          async: false,
          success: function(data){
            window.location.href="/cart";
          }
        });
      });
    });
    
  });
</script>
