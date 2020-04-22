<?php
function sudebe($fn,$ln,$username,$email,$password){
    $x = 0; 
        $ch = curl_init();
curl_setopt($ch, CURLOPT_URL, 'https://www.sudebe.com/includes/ajax/core/signup.php');
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_POSTFIELDS, "first_name=$fn&last_name=$ln&username=$username&email=$email&password=$password&gender=female&birth_month=12&birth_day=12&birth_year=1916&newsletter_agree=on&privacy_agree=on");
curl_setopt($ch, CURLOPT_ENCODING, 'gzip, deflate');

$headers = array();
$headers[] = 'Authority: www.sudebe.com';
$headers[] = 'Accept: application/json, text/javascript, */*; q=0.01';
$headers[] = 'X-Requested-With: XMLHttpRequest';
$headers[] = 'User-Agent: Mozilla/5.0 (Linux; Android 5.0; SM-G900P Build/LRX21T) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.113 Mobile Safari/537.36';
$headers[] = 'Content-Type: application/x-www-form-urlencoded; charset=UTF-8';
$headers[] = 'Origin: https://www.sudebe.com';
$headers[] = 'Sec-Fetch-Site: same-origin';
$headers[] = 'Sec-Fetch-Mode: cors';
$headers[] = 'Sec-Fetch-Dest: empty';
$headers[] = 'Referer: https://www.sudebe.com/';
$headers[] = 'Accept-Language: id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7';
$headers[] = 'Cookie: PHPSESSID=68ddf5b51063c868b29ad23d1bbe2cc1; ref=fzn7; _ga=GA1.2.501291031.1587521726; _gid=GA1.2.1306774346.1587521727; __gads=ID=e59fbe209ab56955:T=1587521811:S=ALNI_MbGOjmaU9mY9797Y4YTfj4Ts3oBrw; cookieconsent_status=dismiss; _gat_gtag_UA_155121126_1=1';
curl_setopt($ch, CURLOPT_HTTPHEADER, $headers);

 

 $server_output = curl_exec ($ch);
 curl_close ($ch);
 echo $server_output."\n";
 $x++;

    }

print "[SUDEBE ACCOUNT CREATE]
Register SUDEBE 
Code By : Ranresellerid
\n";

echo "Daftar SUDEBE!\n";
        echo " First Name :\nInput : ";
        $fn = trim(fgets(STDIN));
        echo " Last Name :\nInput : ";
        $ln = trim(fgets(STDIN));
        echo " Username :\nInput : ";
        $username = trim(fgets(STDIN));
        echo " Email :\nInput : ";
        $email = trim(fgets(STDIN));
        echo " Password :\nInput : ";
        $password = trim(fgets(STDIN));
        echo "+==========RESULT=========+\n";
        $execute = sudebe($fn,$ln,$username,$email,$password);
        print $execute;
        echo "+===========END===========+\n";
?>
