<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>陳毓文｜在地文化與都市規劃</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@400;600;700;900&family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EDE6D6;
    --paper-deep:#E3DAC5;
    --ink:#1F2A24;
    --ink-soft:#4A443C;
    --indigo:#33507A;
    --indigo-deep:#233A5C;
    --brick:#9C3D2E;
    --line: rgba(31,42,36,0.15);
    --serif:'Noto Serif TC', serif;
    --sans:'Noto Sans TC', sans-serif;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:var(--sans);
    line-height:1.75;
    -webkit-font-smoothing:antialiased;
  }
  a{color:inherit;}
  .wrap{max-width:920px;margin:0 auto;padding:0 28px;}

  /* subtle paper texture */
  body::before{
    content:"";
    position:fixed; inset:0;
    background-image:
      repeating-linear-gradient(0deg, rgba(31,42,36,0.015) 0px, rgba(31,42,36,0.015) 1px, transparent 1px, transparent 3px);
    pointer-events:none;
    z-index:0;
  }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    padding:120px 0 90px;
    background:var(--ink);
    color:var(--paper);
    overflow:hidden;
  }
  .hero::after{
    content:"";
    position:absolute;
    right:-120px; top:-120px;
    width:420px;height:420px;
    border:1px solid rgba(237,230,214,0.14);
    border-radius:50%;
  }
  .hero::before{
    content:"";
    position:absolute;
    right:-40px; bottom:-160px;
    width:300px;height:300px;
    border:1px solid rgba(237,230,214,0.1);
    border-radius:50%;
  }
  .hero .eyebrow{
    font-family:var(--serif);
    font-size:15px;
    letter-spacing:0.08em;
    color:#C9B98E;
    margin-bottom:22px;
  }
  .hero h1{
    font-family:var(--serif);
    font-weight:900;
    font-size:clamp(48px, 9vw, 88px);
    margin:0 0 18px;
    line-height:1.05;
    letter-spacing:0.02em;
  }
  .hero .role{
    font-family:var(--serif);
    font-size:clamp(18px,3vw,24px);
    color:#D8CFB4;
    margin:0 0 34px;
    font-weight:400;
  }
  .hero p.lede{
    max-width:560px;
    font-size:16.5px;
    color:#CFC7B2;
    margin:0 0 40px;
  }
  .hero .cta-row{
    display:flex; gap:16px; flex-wrap:wrap;
  }
  .btn{
    display:inline-flex; align-items:center; gap:8px;
    padding:13px 26px;
    border-radius:2px;
    font-size:14.5px;
    text-decoration:none;
    border:1px solid rgba(237,230,214,0.35);
    transition:background .2s ease, border-color .2s ease, color .2s ease;
  }
  .btn-primary{
    background:var(--paper);
    color:var(--ink);
    border-color:var(--paper);
  }
  .btn-primary:hover{ background:#fff; }
  .btn-ghost{ color:var(--paper); }
  .btn-ghost:hover{ border-color:var(--paper); }

  /* ---------- SECTION HEADERS ---------- */
  section{ position:relative; z-index:1; padding:76px 0; }
  section + section{ border-top:1px solid var(--line); }
  .section-head{
    display:flex; align-items:baseline; justify-content:space-between;
    margin-bottom:44px; gap:24px; flex-wrap:wrap;
  }
  .section-head h2{
    font-family:var(--serif);
    font-size:clamp(26px,4vw,34px);
    font-weight:700;
    margin:0;
  }
  .section-head .num{
    font-family:var(--serif);
    font-size:15px;
    color:var(--ink-soft);
    opacity:0.55;
  }

  /* ---------- ABOUT ---------- */
  .about-grid{
    display:grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap:56px;
  }
  .about-text p{ margin:0 0 20px; font-size:16px; color:var(--ink-soft); max-width:60ch;}
  .about-text p:last-child{margin-bottom:0;}
  .edu-card{
    background:var(--paper-deep);
    border:1px solid var(--line);
    padding:26px 28px;
    margin-bottom:16px;
  }
  .edu-card:last-child{margin-bottom:0;}
  .edu-card .yr{ font-size:13px; color:var(--indigo-deep); letter-spacing:0.03em; margin-bottom:6px;}
  .edu-card h3{ font-family:var(--serif); font-size:18px; margin:0 0 4px;}
  .edu-card .deg{ font-size:14.5px; color:var(--ink-soft); }
  .edu-card .role-note{ font-size:13px; color:var(--brick); margin-top:6px; }

  /* ---------- TIMELINE / WORK ---------- */
  .timeline{ position:relative; }
  .timeline::before{
    content:"";
    position:absolute; left:9px; top:6px; bottom:6px;
    width:1px; background:var(--line);
  }
  .tl-item{ position:relative; padding-left:44px; margin-bottom:44px; }
  .tl-item:last-child{ margin-bottom:0; }
  .tl-item::before{
    content:"";
    position:absolute; left:2px; top:6px;
    width:16px; height:16px; border-radius:50%;
    background:var(--paper);
    border:2px solid var(--indigo);
  }
  .tl-item .dates{
    font-size:13px; color:var(--indigo-deep); letter-spacing:0.03em; margin-bottom:6px; font-weight:500;
  }
  .tl-item h3{
    font-family:var(--serif); font-size:20px; margin:0 0 4px; font-weight:700;
  }
  .tl-item .org{
    font-size:14px; color:var(--ink-soft); margin-bottom:14px;
  }
  .tl-item ul{ margin:0; padding-left:20px; }
  .tl-item li{ font-size:15px; color:var(--ink-soft); margin-bottom:6px; }
  .tl-item li:last-child{margin-bottom:0;}

  /* ---------- SKILLS ---------- */
  .skills-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(230px,1fr));
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .skill-cell{
    background:var(--paper);
    padding:26px 24px;
  }
  .skill-cell .mark{ color:var(--brick); font-family:var(--serif); font-size:20px; }
  .skill-cell p{ margin:10px 0 0; font-size:14.5px; color:var(--ink-soft); }

  /* ---------- MEDIA / SOCIAL ---------- */
  .media-lede{ font-size:16px; color:var(--ink-soft); max-width:64ch; margin:0 0 36px;}
  .project-list{ list-style:none; margin:0; padding:0; border-top:1px solid var(--line);}
  .project-list li{
    display:flex; justify-content:space-between; gap:20px;
    padding:16px 0; border-bottom:1px solid var(--line);
    font-size:15px;
  }
  .project-list .client{ color:var(--ink-soft); min-width:180px; }
  .project-list .title{ font-weight:500; text-align:right; }

  /* ---------- CONTACT / FOOTER ---------- */
  .contact{
    background:var(--indigo-deep);
    color:var(--paper);
  }
  .contact .section-head h2{ color:var(--paper); }
  .contact .section-head .num{ color:#B9C4D6; }
  .contact-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:28px;
  }
  .contact-card{
    border:1px solid rgba(237,230,214,0.22);
    padding:24px;
  }
  .contact-card .label{ font-size:12.5px; letter-spacing:0.05em; color:#B9C4D6; margin-bottom:10px;}
  .contact-card .value{ font-size:15.5px; word-break:break-word; }
  .contact-card a{ text-decoration:none; border-bottom:1px solid rgba(237,230,214,0.4); }
  .contact-card a:hover{ border-color:var(--paper); }

  footer{
    text-align:center;
    padding:28px 0;
    font-size:12.5px;
    color:var(--ink-soft);
    opacity:0.7;
  }

  @media (max-width:760px){
    .about-grid{ grid-template-columns:1fr; }
    .hero{ padding:90px 0 64px; }
    section{ padding:56px 0; }
    .project-list li{ flex-direction:column; gap:4px; }
    .project-list .title{ text-align:left; }
  }

  :focus-visible{ outline:2px solid var(--indigo); outline-offset:2px; }
</style>
</head>
<body>

<header class="hero">
  <div class="wrap">
    <div class="eyebrow">在地紋理 · 歷史建築 · 都市規劃</div>
    <h1>陳毓文</h1>
    <p class="role">都市里人規劃組 2024 工讀生｜「步行城市 Walkable City」本編</p>
    <p class="lede">我是陳毓文，畢業於輔仁大學景觀設計學系，現就讀台灣大學建築與城鄉研究所。長期投入文化資產修復、社區走讀與地方行銷，致力於讓更多人認識自己腳下的土地。</p>
    <div class="cta-row">
      <a class="btn btn-primary" href="https://github.com/victorchen-hub" target="_blank" rel="noopener">在 GitHub 上看我的專案</a>
      <a class="btn btn-ghost" href="#contact">聯絡方式</a>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-head">
      <h2>個人簡介</h2>
      <span class="num">01 — 關於我</span>
    </div>
    <div class="about-grid">
      <div class="about-text">
        <p>學習、體驗新事物和接受挑戰，是我永不停歇的學習原動力。每當看到自己的成長與進步，就更加充滿了學習的熱情——這種成就感是無可比擬的。</p>
        <p>畢業設計首次接觸大尺度的都市計畫與規劃議題後，我對「都市中各式多元的社會與空間需要仔細探討」產生了濃厚興趣，因而選擇臺大城鄉所就讀，並朝著文化資產、文化治理與都市更新等方向持續鑽研。</p>
        <p>除了學術訓練，我也長期在文化資產場域工作，並經營「步行城市 Walkable City」粉專的本編——身分與所學都指向同一件事：我對台灣在地紋理、歷史、建築與規劃的熱愛與熟悉。</p>
      </div>
      <div class="about-edu">
        <div class="edu-card">
          <div class="yr">2018 — 2022</div>
          <h3>輔仁大學</h3>
          <div class="deg">景觀設計學系學士學位</div>
          <div class="role-note">畢學會美宣長</div>
        </div>
        <div class="edu-card">
          <div class="yr">2022 — 至今</div>
          <h3>臺灣大學</h3>
          <div class="deg">建築與城鄉研究所，就讀中</div>
          <div class="role-note">所學會會長</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="work">
  <div class="wrap">
    <div class="section-head">
      <h2>工作經歷</h2>
      <span class="num">02 — 歷程</span>
    </div>
    <div class="timeline">

      <div class="tl-item">
        <div class="dates">2023/6 — 至今</div>
        <h3>專案講師</h3>
        <div class="org">川端藝會所</div>
        <ul>
          <li>負責進行公文與分析文字撰寫</li>
          <li>全祥茶坊文化資產潛力調查評估案</li>
          <li>城南文化資產盤點與活化企劃提案</li>
          <li>基本建築與景觀設計案</li>
          <li>城南文化走讀導覽員</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="dates">2023/6 — 2024/4</div>
        <h3>副研究員</h3>
        <div class="org">新境界智庫</div>
        <ul>
          <li>負責進行公文與分析文字撰寫</li>
          <li>會議設計與籌辦</li>
          <li>文化資產、媒體、出版等經濟與文化分析</li>
          <li>國家文化政策擬定</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="dates">2022/11 — 2023/7</div>
        <h3>工讀生</h3>
        <div class="org">文房・文化閱讀空間（頂新和德文教基金會）</div>
        <ul>
          <li>節慶活動之企劃提案、採購與籌辦</li>
          <li>研究幸町職務官舍群之史料，彙整史蹟地圖、解說板繪製，補齊文房長期缺乏正確史料貢獻的問題</li>
          <li>擔任歷史建築內部導覽專員，以平易近人方式將日式建築構造之美深植民眾心中</li>
          <li>植栽種植與建築養護</li>
          <li>文房餐飲提供之咖啡、茶飲、餐點製作</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="dates">2022/12 — 2023/12</div>
        <h3>特約編輯</h3>
        <div class="org">《Taipei Walker》文化雜誌</div>
        <ul>
          <li>街頭攝影與文字敘述，以美吸引讀者愛上自身文化與土地</li>
          <li>臺北在地故事推廣與文化行銷，讓文化進入所有人心中</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="dates">2020/12 — 2021/2</div>
        <h3>工讀生</h3>
        <div class="org">禾拓規劃設計顧問有限公司</div>
        <ul>
          <li>負責進行提案公文與景觀設計基地分析文字撰寫</li>
          <li>負責工作坊會議紀錄，提高會後資料彙整效率</li>
          <li>整理辦公文件與書籍，提高工作活動空間與效率</li>
          <li>基本的電腦繪圖與手稿測繪</li>
          <li>參與新北市板橋區「府中雙城」環境改善計畫</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="dates">2020/6 — 2020/9</div>
        <h3>實習生</h3>
        <div class="org">中冶環境造型顧問有限公司</div>
        <ul>
          <li>負責進行提案公文與景觀設計基地分析文字撰寫</li>
          <li>負責工作坊會議紀錄，提高會後資料彙整效率</li>
          <li>整理辦公文件與書籍，提高工作活動空間與效率</li>
          <li>基本的電腦繪圖與手稿測繪</li>
          <li>參與歷史建築「月眉糖廠製糖工場」修復及再利用計畫、臺北市大安區林務局局長宿舍歷建修復及再利用計畫、金瓜石礦業景觀活化暨輕便軌道復駛評估案</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-head">
      <h2>技能</h2>
      <span class="num">03 — 能力</span>
    </div>
    <div class="skills-grid">
      <div class="skill-cell">
        <div class="mark">文</div>
        <p>以文章推廣在地旅行與文化行銷，對日治時期台北歷史尤其熟悉</p>
      </div>
      <div class="skill-cell">
        <div class="mark">媒</div>
        <p>擅長運用社群媒體發揚在地文化，經營自媒體累積實績</p>
      </div>
      <div class="skill-cell">
        <div class="mark">繪</div>
        <p>熟練 Ai、Ps、CAD 等繪圖與文件軟體，具備現場測繪能力</p>
      </div>
      <div class="skill-cell">
        <div class="mark">溝</div>
        <p>出色的溝通與遠距工作能力，能與團隊一起工作</p>
      </div>
      <div class="skill-cell">
        <div class="mark">壓</div>
        <p>能夠承受工作壓力，並能同時進行多項工作</p>
      </div>
    </div>
  </div>
</section>

<section id="media">
  <div class="wrap">
    <div class="section-head">
      <h2>社群媒體與自媒體經營</h2>
      <span class="num">04 — 步行城市</span>
    </div>
    <p class="media-lede">自 2021 年起經營「步行城市 Walkable City」IG／FB 帳號，以街頭攝影與文字敘述，讓讀者愛上自身文化與土地；持續推動臺北在地故事與文化行銷，也承接多項政府與地方單位的合作案。</p>
    <ul class="project-list">
      <li><span class="client">新竹市政府 x 蚯蚓整合文化</span><span class="title">新竹新築——新竹建築旅行的推廣計畫</span></li>
      <li><span class="client">暗坑文化工作室</span><span class="title">跟著輕軌去旅行——安坑內五庄（安康接待室）</span></li>
      <li><span class="client">客委會 x 洄游創生</span><span class="title">2023 桐花祭 X 新竹文學採點開箱</span></li>
      <li><span class="client">苗栗縣政府文資科</span><span class="title">A2 出磺坑礦場礦業歷史散步道管理營運計畫</span></li>
      <li><span class="client">客委會 x 光蘊數位</span><span class="title">第二屆浪漫台三線藝術季</span></li>
    </ul>
  </div>
</section>

<section id="contact" class="contact">
  <div class="wrap">
    <div class="section-head">
      <h2>聯絡方式</h2>
      <span class="num">05 — Contact</span>
    </div>
    <div class="contact-grid">
      <div class="contact-card">
        <div class="label">GITHUB</div>
        <div class="value"><a href="https://github.com/victorchen-hub" target="_blank" rel="noopener">github.com/victorchen-hub</a></div>
      </div>
      <div class="contact-card">
        <div class="label">EMAIL</div>
        <div class="value"><a href="mailto:r11544001@g.ntu.edu.tw">r11544001@g.ntu.edu.tw</a></div>
      </div>
      <div class="contact-card">
        <div class="label">PHONE</div>
        <div class="value">0910-605-535</div>
      </div>
      <div class="contact-card">
        <div class="label">INSTAGRAM</div>
        <div class="value"><a href="https://www.instagram.com/walkable_city" target="_blank" rel="noopener">@walkable_city</a></div>
      </div>
      <div class="contact-card">
        <div class="label">步行城市 專欄</div>
        <div class="value"><a href="https://taipeiwalker.walkerland.com.tw/authors/78/articles" target="_blank" rel="noopener">Taipei Walker 文章列表</a></div>
      </div>
      <div class="contact-card">
        <div class="label">ADDRESS</div>
        <div class="value">104 台北市中山區大直街94巷1弄22號2樓</div>
      </div>
    </div>
  </div>
</section>

<footer>© 2026 陳毓文 · 以在地文化與都市規劃為業</footer>

</body>
</html>
