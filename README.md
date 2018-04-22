# New
想使用Twig-php 模版引擎必須要先架好php伺服器
PHP 建立服務器
先到wamp官方網站下載wamp x64 or x86 版本
http://www.wampserver.com/
再來需下載 Visual C++ Redistributable for Visual Studio 2015
https://www.microsoft.com/en-us/download/details.aspx?id=48145
及Visual C++ Redistributable for Visual Studio 2012 Update 4
https://www.microsoft.com/en-gb/download/details.aspx?id=30679

請先安裝Visual C++，最後再安裝wamp，安裝完後基本上就沒什麼問題了


Twig安裝
下載composer 
https://getcomposer.org/Composer-Setup.exe
打開cmd命令指示字元，到相關專案目錄下輸入 composer require "twig/twig:^2.0
貼上以下指令建置twig環境
require_once __DIR__ . '/vendor/autoload.php'; //引入twig
$loader = new Twig_Loader_Filesystem(__DIR__ . '/view'); //設定template檔案
$twig = new Twig_Environment($loader); //設定環境變數
$array_data = array(‘foo’ => ‘bar’);  //傳資料
echo $twig ->render('test.html', array(
	'name' => 'USCSS Nostromo',
	'type' => 'Haular',
	'owner' => 'Weyland-Yutani',
	'reg-no' => '180924609',
  ));


