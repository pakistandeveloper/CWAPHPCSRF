𝓒𝓸𝓭𝓮 𝓦𝓲𝓽𝓱 𝓪𝓱𝓶𝓮𝓭

PHP CSRF TOKEN GENRATOR

How to Genrate?

first of all CWA_Plugins/CsrfGenrate.php in your php code

Your form. like That.

Token Create.
<form action="" method="POST">

    Add Input Hidden Field  And Add this code on hiddenfield value <?php echo $CSRF->Create() ?>
    After that Set the name="" done
    

        <input type="hidden" name="CsrfFormField" value="<?php echo $CSRF->Create() ?>">
       
 </form>

 Token Verify
 $CSRF->Check($_POST['CsrfFormField']) || return True || False

true == Access
false == Redirect Error
