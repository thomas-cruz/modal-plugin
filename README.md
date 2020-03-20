# modal-plugin
A jquery modal plugin

Variables:  
Message: What the content/body of the modal will be
Title: Title of modal, can be empty
Scrollable (true or false)
CloseButton (true or false): Close button on footer of modal

Example
HTML
<a class="btn btn-primary view-pdf" href="http://www.pentax-manuals.com/manuals/service/canon_p_repair.pdf">PDF</a>

JS
$(function(){    
    $('.view-pdf').on('click',function(){
        var pdf_link = $(this).attr('href');
        var iframe = '<div class="iframe-container"><iframe src="'+pdf_link+'"></iframe></div>'
        $.createModal({
          title:'Canon P Repair Manual',
          message: iframe,
          closeButton:true,
          scrollable:false
        });
        return false;        
    });    
})
