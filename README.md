# megarokun
UltimateOAuth.php
<?php
require_once('UltimateOAuth.php'); //

function mic( $len ){ //

$sn = substr(md5(microtime(true)),0,$len);

return $sn;
}


$uo = new UltimateOAuth('CK', 'CS');
$uo->directGetToken("ID","パスワード");

while (true){ //

$mes = mic( 100 ); //

$res = $uo->post('statuses/update', ['status' => "@null ${mes}"]);

} //while
