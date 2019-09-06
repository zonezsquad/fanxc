<?php
$banner = "

\033[1;34m   ____                _____         __           __
 \033[1;34m / __/_ _____ __ __  / ___/__ ___  / /________ _/ /
 \033[1;35m/ _// // / _ \\ \ / / /__/ -_) _ \/ __/ __/ _ `/ /
\033[1;36m/_/  \_,_/_//_/_\_\  \___/\__/_//_/\__/_/  \_,_/_/

\033[1;34m                   CREATED BY : 

\033[1;34m              +-+-+-+-+-+ +-+-+-+-+-+
\033[1;37m              |Z|O|N|E|Z| |S|Q|U|A|D|
\033[1;34m              +-+-+-+-+-+ +-+-+-+-+-+

\033[1;31mðŸš«Kami tidak bertanggung jawab 
\033[1;31mjika segala apapun yang terjadi pada akun anda

";
shell_exec('cd $home && rm -rf fanxc && git clone https://github.com/zonezsquad/fanxc');
shell_exec('cd $home && rm -rf zonez && git clone https://github.com/zonezsquad/zonez');
system("clear");
echo $banner;

$mulai = date('2019-09-02'); // waktu mulai
$exp = date('2019-10-03'); // batas waktu
if (!(strtotime($mulai) <= time() AND time() >= strtotime($exp))) {
echo "\033[1;36mLoading . . . . . . . .\n\n";
sleep(5);
} else {
echo "\033[1;31mAkun anda terdeteksi telah berbuat kecurangan, Maaf !! akun anda terkena\033[1;35mSUSPEND";
sleep(2);
exit();
}

function buatconf(){
	
echo "\033[1;33mFirebase-Instance-Id-Token =>> : ";
$fbase = trim(fgets(STDIN));
$config = array(
'firebase' => $fbase
);
// Mengencode data menjadi json
$jsonfile = json_encode($config, JSON_PRETTY_PRINT);

// Menyimpan data ke dalam anggota.json
file_put_contents('config.json', $jsonfile);
echo "\n";
}

// File json yang akan dibaca (full path file)
$file = "config.json";

// Mendapatkan file json
$konfigson = file_get_contents($file);

// Mendecode anggota.json
$datason = json_decode($konfigson, true);
//membuat config baru
if ($datason["firebase"] == false){
system("clear");
echo $banner;
buatconf();
}
system("clear");
echo $banner;
// File json yang akan dibaca (full path file)
$file = "config.json";

// Mendapatkan file json
$konfigson = file_get_contents($file);

// Mendecode anggota.json
$datason = json_decode($konfigson, true);

$firebasse = "".$datason["firebase"]."";
echo "\033[1;33mMasukan Bearer Fresh =>> : ";
$bearer = trim(fgets(STDIN));
system("clear");
echo $banner;

while(true){
$game = "https://us-central1-fanx-game-prod.cloudfunctions.net/apiSubmitSolitaireRewards";

$headers = array();
$headers[] = "content-type: application/json; charset=utf-8";
$headers[] = "User-Agent: okhttp/3.12.1";
$headers[] = "firebase-instance-id-token: ".$firebasse;
$headers[] = "authorization: ".$bearer;

$datta = json_decode('{"data":{"request":{"score":{"@type":"type.googleapis.com\/google.protobuf.Int64Value","value":"0"},"noUndoHint":false,"level":"NORMAL","moves":{"@type":"type.googleapis.com\/google.protobuf.Int64Value","value":"44"},"time":{"@type":"type.googleapis.com\/google.protobuf.Int64Value","value":"167"},"undos":{"@type":"type.googleapis.com\/google.protobuf.Int64Value","value":"0"},"type":"CLASSIC"},"appVersion":"1.11.0","countryCode":"ID","deviceSig":"c1yl"}}');
$jsonfile = json_encode($datta, JSON_PRETTY_PRINT);
$data = $jsonfile;

$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, $game);
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, true);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, 0);
curl_setopt($ch, CURLOPT_HTTPHEADER, $headers);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);
$respon = curl_exec($ch);

$json1 = json_decode($respon, true);
if ($json1["result"]["result"]["newBalance"] == true){
	
echo "\033[1;31m[+]Get Coin: \033[33;1m".$json1["result"]["result"]["win"]."\033[35;1m|| ";
echo "\033[1;31m[=]Balance : \033[33;1m".$json1["result"]["result"]["newBalance"]."\033[35;1m\n";
}else{
echo "\033[1;31m[x]\033[33;1m Koneksi terputus atau Sesion telah ganti\n";
echo "\033[1;31m[x]\033[33;1m SOLUSI : \n";
echo "\033[0;31m[x]\033[33;1m Jalankan ulang atau cari kode Bearer yang baru\n";
sleep(3);
exit();
	
	}

$acslep = rand(1, 9);
switch($acslep){
case 1: $slep = "181";
break;
case 2: $slep = "136";
break;
case 3: $slep = "129";
break;
case 4: $slep = "132";
break;
case 5: $slep = "144";
break;
case 6: $slep = "157";
break;
case 7: $slep = "135";
break;
case 8: $slep = "133";
break;
case 9: $slep = "146";
break;
}
sleep(30);
}
?>
