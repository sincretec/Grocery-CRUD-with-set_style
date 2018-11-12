# Grocery-CRUD-with-set_style
Grocery CRUD with set_style_td and set_style_th functions to change datatables and flexigrid themes

Maybe this could be a branch of Grocery CRUD

This functions allow some control over:
- Column Width
- Font family, size, color, weight...

I said "some" control, because column width is "almost" controlled. flexigrid theme is more flexible than datatables in this issue. 
Column width can not be smaller than content or header. 
If it is asigned a smaller font to the cell, then it is posible to reduce column width.

It is based on sugestions by https://www.grocerycrud.com/forums/user/703-crina/ in http://www.grocerycrud.com/forums/topic/902-is-it-possible-alter-render-of-th-widths/

The files midified are:
application\libraries\Grocery_CRUD.php
assets\grocery_crude\themes\datatables\views\list.php
assest\grocery_crude\themes\flexigrid\views\list.php

Just overwrite them.

        ...
        $th_styles = array( 'evento' => 'width: 20px;',
                            'DID' => 'width:20px; text-align: center;',
                            'T'   => 'width: 20px; text-align: center; color:blue;',
                            'H'   => 'width: 20px; text-align: center;',
                            'C'   => 'width: 20px; text-align: center;'
                        );
        $crud->set_style_th($th_styles);
        
        $td_styles = array( 'e' => 'width:150px; font-size:9pt;',
                            'log_id' => 'width:150px; font-size:9pt;',
                            'DID' => 'width:150px; font-size:9pt;',
                            'accion' => 'width:150px; font-size:9pt;',
                            'valores' => 'width:400px; font-size:9pt;',
                            'fecha' => 'width:150px; font-size:9pt;'
                        );

        $crud->set_style_td($td_styles);
        $crud->render();
