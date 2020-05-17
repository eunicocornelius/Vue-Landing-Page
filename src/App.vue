<template>
  <body>
    <!-- <div>
      <nav>
        <ul class="navbar-nav nav navbar-expand-lg">
          <li class="nav-item active"><a >0274-5305505</a></li>
          <li class="nav-item active"><a >Live Chat</a></li>
          <li class="nav-item active"><a >Member Area</a></li>
        </ul>
      </nav>
    </div> -->
    <hr class="full">
    <!--Navbar Section Start-->
    <nav class="bg-white navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse d-flex flex-row-reverse" id="navbarSupportedContent">
        <ul class="navbar-nav nav navbar-right">
          <li class="nav-item active">
            <a class="nav-link" href="#">Hosting <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Domain <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Server <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Website <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Afiliasi <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Promo <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Pembayaran <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Review <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Kontak <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active">
            <a class="nav-link" href="#">Blog <span class="sr-only">(current)</span></a>
          </li>
        </ul>
      </div>
    </nav>
    <!--Navbar Section End-->
    <hr class="full">
    <!--Hosting Section Start-->
    <div id="php-hosting-section" class="row">
      <div class="col-sm-6">
        <h1 class="mont-bold">PHP Hosting</h1>
        <h2 class="mont-light">Cepat, Handal, penuh dengan modul PHP yang Anda butuhkan</h2>
        <ul class="mont-hairline check space">
          <li >Solusi PHP untuk preforma query yang lebih cepat</li>
          <li >Konsumsi memori yang lebih rendah</li>
          <li >Support PHP 5.3, PHP 5.4, PHP 5.5, PHP 5.6, PHP 7</li>
          <li >Fitur enkripsi IonCube dan Zend Guard Loaders</li>
        </ul>
      </div>
      <div class="col">
        <img src="./assets/svg/illustration-banner-PHP-hosting-01.svg">
      </div>
    </div>
    <!--Hosting Section End-->
    <hr class="full">
    <!-- Components Section Start -->
    <div id="components-section" class="row mont-light">
      <div class="col-12 col-sm-4 component">
        <div><img src="./assets/images/zendguard.png"></div>
        <div>PHP Zend Guard Loader</div>
      </div>
      <div class="col-12 col-sm-4 component">
        <div><img src="./assets/images/composer.png"></div>
        <div>PHP Composer</div>
      </div>
      <div class="col-12 col-sm-4 component">
        <div><img src="./assets/images/ioncube.png"></div>
        <div>PHP ionCube Loader</div>
      </div>
    </div>
    <!-- Components Section End -->
    <!-- SG Hosting Section Start -->
    <div id="sg-hosting-section" class="text-center">
      <div class="mont-bold"><h2>Paket Hosting Singapura yang Tepat</h2></div>
      <div class="mont-light"><h4>Diskon 40% + Domain dan SSL Gratis untuk Anda</h4></div>
    </div>
    <!-- SG Hosting Section End -->
    <!-- Pricing Section Start-->
      <div class="row price justify-content-center">
        <div v-for="data in myJson" :key="data.name">
          <template v-if="data.best == true">
          <!-- Title Start -->
          <div class="col-12 price-container text-center best-seller">
            <div class="price-title text-white">
              <p>{{data.name}}</p>
            </div>
          </div>
          <!-- Title End -->
          <!-- Price Start -->
          <div class="col-12 price-container text-center pt-3 best-seller">
            <p class="price-discount text-white">Rp {{data.disc_price}}</p>
            <div class="row justify-content-center">
              <div class="price-text text-white">Rp </div>
              <div><p class="price-f text-white">{{data.price_f}}</p></div>
              <div><p class="price-b text-white">{{data.price_b}}</p></div>
              <div class="price-text text-white">/bln</div>
            </div>
          </div>
          <!-- Price End -->
          </template>
          <template v-if="data.best == false">
          <!-- Title Start -->
          <div class="col-12 price-container text-center">
            <div class="price-title">
              <p>{{data.name}}</p>
            </div>
          </div>
          <!-- Title End -->
          <!-- Price Start -->
          <div class="col-12 price-container text-center pt-3">
            <p class="price-discount text-muted">Rp {{data.disc_price}}</p>
            <div class="row justify-content-center">
              <div class="price-text text-muted">Rp </div>
              <div><p class="price-f">{{data.price_f}}</p></div>
              <div><p class="price-b">{{data.price_b}}</p></div>
              <div class="price-text text-muted">/bln</div>
            </div>
          </div>
          <!-- Price End -->
          </template>
          <template v-if="data.best == true">
          <!-- Pengguna Start-->
          <div class="col-12 price-container text-center pt-3 best-pengguna">
            <div class="row justify-content-center">
              <p class="price-pengguna ml-3 text-white">{{data.pengguna}}</p>
              <div class="price-text ml-1 mr-3 text-white">Pengguna Terdaftar</div>
            </div>
          </div>
          <!-- Pengguna End-->
          </template>
          <template v-if="data.best == false">
          <!-- Pengguna Start-->
          <div class="col-12 price-container text-center pt-3">
            <div class="row justify-content-center">
              <p class="price-pengguna ml-3">{{data.pengguna}}</p>
              <div class="price-text ml-1 mr-3">Pengguna Terdaftar</div>
            </div>
          </div>
          <!-- Pengguna End-->
          </template>
          <div class="col-12 price-container text-center pt-3 pb-5">
          <!-- List Start -->
          <template v-if="data.id == 1">
            <ul class="mont-light desc-price">
              <li><b>0.5X RESOURCE POWER</b></li>
              <li><b>500 MB</b> Disk Space</li>
              <li><b>Unlimited</b> Bandwith</li>
              <li><b>Unlimited</b> Databases</li>
              <li><b>1</b> Domain</li>
              <li><b>Instant</b> Backup</li>
              <li><b>Unlimited SSL</b> Gratis Selamanya</li>
            </ul>
          </template>
          <template v-if="data.id == 2">
            <ul class="mont-light desc-price">
              <li><b>1X RESOURCE POWER</b></li>
              <li><b>Unlimited</b> Disk Space</li>
              <li><b>Unlimited</b> Bandwith</li>
              <li><b>Unlimited</b> POP3 Email</li>
              <li><b>Unlimited</b> Databases</li>
              <li><b>10</b> addon Domains</li>
              <li><b>Instant</b> Backup</li>
              <li><b>Domain</b> Gratis Selamanya</li>
              <li><b>Unlimited SSL</b> Gratis Selamanya</li>
            </ul>
          </template>
          <template v-if="data.id == 3">
            <ul class="mont-light desc-price">
              <li><b>2X RESOURCE POWER</b></li>
              <li><b>Unlimited</b> Disk Space</li>
              <li><b>Unlimited</b> Bandwith</li>
              <li><b>Unlimited</b> POP3 Email</li>
              <li><b>Unlimited</b> Databases</li>
              <li><b>Unlimited</b> addon Domains</li>
              <li><b>Instant</b> Backup</li>
              <li><b>Domain</b> Gratis Selamanya</li>
              <li><b>Unlimited SSL</b> Gratis Selamanya</li>
              <li><b>Private</b> Name Server</li>
              <li><b>Spam Assasin</b> Mail Protection</li>
            </ul>
          </template>
          <template v-if="data.id == 4">
            <ul class="mont-light desc-price">
              <li><b>3X RESOURCE POWER</b></li>
              <li><b>Unlimited</b> Disk Space</li>
              <li><b>Unlimited</b> Bandwith</li>
              <li><b>Unlimited</b> POP3 Email</li>
              <li><b>Unlimited</b> Databases</li>
              <li><b>Unlimited</b> addon Domains</li>
              <li><b>Magic Auto</b> Backup & Restore</li>
              <li><b>Domain</b> Gratis Selamanya</li>
              <li><b>Unlimited SSL</b> Gratis Selamanya</li>
              <li><b>Private</b> Name Server</li>
              <li><b>Prioritas</b> Layanan Support</li>
              <li><b>Spam Assasin</b> Mail Protection</li>
            </ul>
          </template>
          <template v-if="data.best == true">
          <button class="hosting-button">Pilih Sekarang</button>
          </template>
          <template v-if="data.best == false">
          <button class="modul-button">Pilih Sekarang</button>
          </template>
          <!-- List End -->
          </div> 
        </div>
      </div>
      

    <!-- Pricing Section End-->
    <!-- Limit Section Start-->
    <div id="sg-hosting-section" class="text-center">
      <div class="mont-light pb-4"><h2>Powerful dengan Limit PHP yang Lebih Besar</h2></div>
      <div class="mont-light row justify-content-md-center">
        <table class="table table-bordered col-5 mr-4">
          <tr>
            <td><i class="fas fa-check-circle float-left text-success"></i>max execution time 300s</td>
          </tr>
          <tr>
            <td class="bg-light"><i class="fas fa-check-circle float-left text-success"></i>max execution time 300s</td>
          </tr>
          <tr>
            <td><i class="fas fa-check-circle float-left text-success"></i>php memory limit 1024 MB</td>
          </tr>
        </table>
        <table class="table table-bordered col-5">
          <tr>
            <td><i class="fas fa-check-circle float-left text-success"></i>post max size 128 MB</td>
          </tr>
          <tr>
            <td class="bg-light"><i class="fas fa-check-circle float-left text-success"></i>upload max filesize 128 MB</td>
          </tr>
          <tr>
            <td><i class="fas fa-check-circle float-left text-success"></i>max input vars 2500</td>
          </tr>
        </table>
      </div>
    </div>
    <!-- Limit Section End-->
    <hr class="short">
    <!-- Paket Hosting Section Start-->
    <div id="paket-hosting-section" class="text-center">
      <div class="mont-light pb-4 pt-5"><h2>Semua Paket Hosting Sudah Termasuk</h2></div>
      <div class="row justify-content-md-center pb-5">
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/semua_versi.svg"></div>
          <h5 class="mont-bold">PHP Semua Versi</h5>
          <p class="mont-light desc">Pilih mulai dari versi PHP 5.3 s/d PHP 7. <br> Ubah sesuka Anda!</p>
        </div>
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/mysql.svg"></div>
          <h5 class="mont-bold">MySQL Versi 5.6</h5>
          <p class="mont-light desc">Nikmati MySQL versi terbaru, tercepat dan<br> kaya akan fitur.</p>
        </div>
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/cpanel.svg"></div>
          <h5 class="mont-bold">Panel Hosting cPanel</h5>
          <p class="mont-light desc">Kelola website dengan panel canggih yang<br> familiar di hati Anda.</p>
        </div>
      </div>
      <div class="row justify-content-md-center">
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/uptime.svg"></div>
          <h5 class="mont-bold">Garansi Uptime 99.9%</h5>
          <p class="mont-light desc">Data center yang mendukung kelangsungan <br> website Anda 24/7.</p>
        </div>
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/innodb.svg"></div>
          <h5 class="mont-bold">Database InnoDB Unlimited</h5>
          <p class="mont-light desc">Jumlah dan ukuran database yang tumbuh<br> sesuai kebutuhan Anda.</p>
        </div>
        <div class="col-12 col-sm-4">
          <div class="img-paket mb-5 mx-auto"><img src="./assets/svg/remote.svg"></div>
          <h5 class="mont-bold">Wildcard Remote MySQL</h5>
          <p class="mont-light desc">Mendukung s/d 25 max_user_connections<br> dan 100 max_connecitons.</p>
        </div>
      </div>
    </div>
    <!-- Paket Hosting Section End-->
    <hr class="short">
    <!-- Laravel Section Start -->
    <div id="laravel-section" class="text-center">
      <div class="mont-light pb-4 pt-5"><h2>Mendukung Penuh Framework Laravel</h2></div>
        <div class="row">
          <div class="col-sm-6 text-left">
            <h6 class="mont-light space">
              Tak perlu menggunakan dedicated server ataupun VPS <br>
              yang mahal. Layanan PHP hosting murah kami <br>
              mendukung penuh framework favorit Anda.
            </h6>


            <ul class="mont-light check space">
              <li class="laravel-desc float-left">Install Laravel <b>1 klik</b>  dengan Softaculous Installer.</li>
              <li class="laravel-desc float-left">Mendukung ekstensi <b>PHP MCrypt, phar, mbstring, json,</b>  dan <b>fileinfo.</b></li>
              <li class="laravel-desc float-left">Tersedia <b>Composer</b> dan <b>SSH</b> untuk menginstal packages pilihan Anda.</li>
            </ul>
            <br>
            <p class=" mont-light desc-small">Nb. Composer dan SSH hanya tersedia pada paket Personal dan Bisnis</p>
            <div class="text-center text-sm-left">
              <button class="hosting-button">Pilih Hosting Anda</button>
            </div>
          </div>
        <div class="col">
          <img src="./assets/svg/laravel_hosting.svg">
        </div>
      </div>
    </div>
    <!-- Laravel Section End -->
    <hr class="full">
    <!-- Modul Section Start -->
    <div id="modul-section" class="text-center pb-5">
      <div class="mont-light pb-4 pt-5"><h2>Modul Lengkap untuk Menjalankan Aplikasi PHP Anda.</h2></div>
        <div class="row text-left ml-5">
        <ul class="col-12 col-sm-3">
          <li v-for="modul in moduls1" :key="modul.message">
            {{ modul.message }}
          </li>
        </ul>
        <ul class="col-12 col-sm-3">
          <li v-for="modul in moduls2" :key="modul.message">
            {{ modul.message }}
          </li>
        </ul>
        <ul class="col-12 col-sm-3">
          <li v-for="modul in moduls3" :key="modul.message">
            {{ modul.message }}
          </li>
        </ul>
        <ul class="col-12 col-sm-3">
          <li v-for="modul in moduls4" :key="modul.message">
            {{ modul.message }}
          </li>
        </ul>
        </div>
    </div>
    <div class="text-center">
      <button class="modul-button">Selengkapnya</button>
    </div>
    <!-- Modul Section End -->
    <!-- Linux Section Start -->
    <div id="linux-section" class="row pt-5">
      <div class="col-12 col-sm-6 ">
        <div class="mont-light pb-4 "><h2>Linux Hosting yang Stabil dengan Teknologi LVE</h2></div>
        <p class="mont-light desc-linux">SuperMicro <b>Intel Xeon 24-Cores</b> server dengan RAM <b>128 GB</b> dan <br>
        teknologi <b>LVE CloudLinux</b> untuk stabilitas server Anda Dilengkapi <br>
        dengan <b>SSD</b> untuk kecepatan <b>MySQL</b> dan caching. Apache load balancer <br>
        berbasis LiteSpeed Technologies, <b>CageFS</b> security. <b>Raid-10</b> protection <br>
        dan auto backup untuk keamanan website PHP Anda.
        </p>
        <div class="text-center text-sm-left">
          <button class="hosting-button">Pilih Hosting Anda</button>
        </div>
      </div>
      <div class="col-12 col-sm-6 mt-5">
        <img src="./assets/images/Image_support.png">
      </div>
    </div>
    <!-- Linux Section End -->
    <div id="app" class="main">
    </div>
  </body>
</template>

<script>
import json from './data.json'
export default {
  name: 'App',
  components: {
  },
  data(){
      return {
        myJson: json,
        moduls1: [
          { message: 'IcePHP' },
          { message: 'apc' },
          { message: 'apcu' },
          { message: 'apm' },
          { message: 'ares' },
          { message: 'bcmath' },
          { message: 'bcompiler' },
          { message: 'big_int' },
          { message: 'bitset' },
          { message: 'bloomy' },
          { message: 'bz2_filter' },
          { message: 'clamav' },
          { message: 'coin_acceptor' },
          { message: 'crack' },
          { message: 'dba' },
        ],
        moduls2: [
          { message: 'http' },
          { message: 'huffman' },
          { message: 'idn' },
          { message: 'igbinary' },
          { message: 'imagick' },
          { message: 'imap' },
          { message: 'inclued' },
          { message: 'inotify' },
          { message: 'interbase' },
          { message: 'intl' },
          { message: 'ioncube_loader' },
          { message: 'ioncube_loader_4' },
          { message: 'jsmin' },
          { message: 'json' },
          { message: 'Idap' },
        ],
        moduls3: [
          { message: 'nd_pdo_mysql' },
          { message: 'oauth' },
          { message: 'oci8' },
          { message: 'odbc' },
          { message: 'opcache' },
          { message: 'pdf' },
          { message: 'pdo' },
          { message: 'pdo_dblib' },
          { message: 'pdo_firebird' },
          { message: 'pdo_mysql' },
          { message: 'pdo_odbc' },
          { message: 'pdo_pgsql' },
          { message: 'pdo_sqlite' },
          { message: 'pgsql' },
          { message: 'phalcon' },
        ],
        moduls4: [
          { message: 'stats' },
          { message: 'stem' },
          { message: 'stomp' },
          { message: 'suhosin' },
          { message: 'sybase_ct' },
          { message: 'sysvmsg' },
          { message: 'sysvsem' },
          { message: 'sysvshm' },
          { message: 'tidy' },
          { message: 'timezonedb' },
          { message: 'trader' },
          { message: 'translit' },
          { message: 'uploadprogress' },
          { message: 'uri_template' },
          { message: 'uuid' },
        ],

      }
    }
  }
</script>
<style>
  /* Montserrat Font */
  @font-face {
    font-family: 'mont-black';
    src: url('assets/fonts/montserrat/Montserrat-Black.otf');
  }
  @font-face {
    font-family: 'mont-bold';
    src: url('assets/fonts/montserrat/Montserrat-Bold.otf');
  }
  @font-face {
    font-family: 'mont-hairline';
    src: url('assets/fonts/montserrat/Montserrat-Hairline.otf');
  }
  @font-face {
    font-family: 'mont-light';
    src: url('assets/fonts/montserrat/Montserrat-Light.otf');
  }
  @font-face {
    font-family: 'mont-regular';
    src: url('assets/fonts/montserrat/Montserrat-Regular.otf');
  }
  /* Robotto Font */
  @font-face {
    font-family: 'roboto-black';
    src: url('assets/fonts/roboto/Roboto-Black.ttf');
  }
  @font-face {
    font-family: 'roboto-blacki';
    src: url('assets/fonts/roboto/Roboto-BlackItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-bold';
    src: url('assets/fonts/roboto/Roboto-Bold.ttf');
  }
  @font-face {
    font-family: 'roboto-boldcon';
    src: url('assets/fonts/roboto/Roboto-BoldCondensed.ttf');
  }
  @font-face {
    font-family: 'roboto-boldconi';
    src: url('assets/fonts/roboto/Roboto-BoldCondensedItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-boldi';
    src: url('assets/fonts/roboto/Roboto-BoldItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-con';
    src: url('assets/fonts/roboto/Roboto-Condensed.ttf');
  }
  @font-face {
    font-family: 'roboto-coni';
    src: url('assets/fonts/roboto/Roboto-CondensedItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-i';
    src: url('assets/fonts/roboto/Roboto-Italic.ttf');
  }
  @font-face {
    font-family: 'roboto-light';
    src: url('assets/fonts/roboto/Roboto-Light.ttf');
  }
  @font-face {
    font-family: 'roboto-lighti';
    src: url('assets/fonts/roboto/Roboto-LightItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-med';
    src: url('assets/fonts/roboto/Roboto-Medium.ttf');
  }
  @font-face {
    font-family: 'roboto-medi';
    src: url('assets/fonts/roboto/Roboto-MediumItalic.ttf');
  }
  @font-face {
    font-family: 'roboto-regular';
    src: url('assets/fonts/roboto/Roboto-Regular.ttf');
  }
  @font-face {
    font-family: 'roboto-thin';
    src: url('assets/fonts/roboto/Roboto-Thin.ttf');
  }
  @font-face {
    font-family: 'roboto-thini';
    src: url('assets/fonts/roboto/Roboto-ThinItalic.ttf');
  }
  * {
    box-sizing: border-box;
  }
  body {
    line-height: 1.4;
    padding: 0 5%;
  }
  
  hr.full{
    margin-left:-100%;
    margin-right:-100%;
  }

  hr.short{
    border: 1.5px solid lightgray;
    width: 10%;
  }

  nav {
    margin-left:-5%;
    margin-right:-5%;
  }

  ul {
    list-style-type: none;
    padding-inline-start: 0;
    padding-top: 0.5rem;
  } 

  ul.check li::before {
    content: "\f058";
    font-family: "Font Awesome 5 Free";
    margin-right:0.5rem;
  }

  .checked::before {
    content: "\f058";
  }

  .notlong{
    margin: 0;
  }

  .desc {
    font-size: 0.7rem;
  }

  .desc-price{
    font-size: 0.7rem;
  }
  
  .desc-price b{
    font-family: mont-bold;
  }

  .desc-linux b{
    font-family: mont-bold;
  }

  .desc-small {
    font-size: 0.7rem;
    padding-top: 5rem;
  }

  .desc-linux {
    font-size: 0.8rem;
  }

  .laravel-desc {
    font-size: 0.8rem;
  }

  .img-paket{
    height: 30%;
    width: 30%;
  }

  .space {
    line-height: 30px;
  }

  .hosting-button{
    background-color: #0090EF;
    color: white;
    font-family: mont-bold;
    padding: 10px 27px;
    margin-top: 15px;
    border-radius: 50px;
  }

  .modul-button{
    background-color: white;
    font-family: mont-bold;
    padding: 10px 27px;
    margin-top: 15px;
    border-radius: 50px;
    border-color: black;
  }


  .price-title {
    font-family: mont-bold;
    font-size: 2rem;
  }

  .price-container {
    border-style: solid;
    border-width: thin;
    border-color: lightgrey;
  }

  .price-discount {
    text-decoration: line-through;
    font-family: mont-light;
  }

  .price-text {
    font-family: mont-light;
  }

  .price-f {
    font-family: mont-bold;
    font-size: 3rem;
    margin-top: -15px;
  }

  .price-b {
    font-family: mont-bold;
  }

  .price-pengguna {
    font-family: mont-bold;
  }

  .best-seller {
    background-color: #0090EF;
  }

  .best-pengguna {
    background-color: rgb(0, 103, 172);
  }

  .component img {
    width:50%;
    height: 250px;
}

  #php-hosting-section {
    margin-top:3rem;
    margin-bottom:3rem;
  }

  #components-section {
    margin-top:3rem;
    margin-bottom:3rem;
  }
  #sg-hosting-section {
    margin-top:5rem;
    margin-bottom:5rem;
  }
  #laravel-section {
    margin-bottom:5rem;
  }
  
  /* Font Call */
  .mont-black {
    font-family: mont-black;
  }
  .mont-bold {
    font-family: mont-bold;
  }
  .mont-hairline {
    font-family: mont-hairline;
  }
  .mont-light {
    font-family: mont-light;
  }
  .mont-regular {
    font-family: mont-regular;
  }
  

</style>
