# Nimo-puls
Nimo+ Anime &amp;Manga website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>NIMO+ | Anime & Manga</title>

<style>

/* =========================
   RESET
========================= */

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:Arial,Helvetica,sans-serif;
  background:#07080d;
  color:white;
  overflow-x:hidden;
}

button,
input,
select{
  font:inherit;
}

button{
  cursor:pointer;
}


/* =========================
   SIDEBAR
========================= */

.sidebar{
  position:fixed;
  left:0;
  top:0;
  width:230px;
  height:100vh;
  padding:25px 18px;
  background:#0d0f17;
  border-right:1px solid #242737;
  z-index:1000;
  overflow-y:auto;
}

.logo{
  font-size:28px;
  font-weight:900;
  letter-spacing:3px;
  margin:5px 10px 40px;
}

.logo span{
  color:#8067ff;
}

.menu-title{
  color:#656a7b;
  font-size:10px;
  letter-spacing:2px;
  margin:25px 10px 10px;
}

.menu{
  display:flex;
  flex-direction:column;
  gap:6px;
}

.menu button{
  width:100%;
  border:0;
  padding:13px;
  border-radius:10px;
  text-align:left;
  background:transparent;
  color:#a6aabc;
  transition:.2s;
}

.menu button:hover,
.menu button.active{
  background:#1b1930;
  color:white;
}


/* =========================
   MAIN
========================= */

.main{
  margin-left:230px;
  min-height:100vh;
}

.topbar{
  position:sticky;
  top:0;
  z-index:500;
  height:75px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  padding:0 30px;
  background:rgba(7,8,13,.88);
  border-bottom:1px solid #222534;
  backdrop-filter:blur(20px);
}

.search{
  width:min(500px,55%);
  padding:13px 18px;
  border-radius:12px;
  border:1px solid #292d3d;
  background:#11131c;
  color:white;
  outline:none;
}

.search:focus{
  border-color:#8067ff;
}

.top-right{
  display:flex;
  align-items:center;
  gap:12px;
}

.top-btn{
  width:40px;
  height:40px;
  border-radius:50%;
  border:1px solid #292d3d;
  background:#11131c;
  color:white;
}

.avatar{
  width:40px;
  height:40px;
  border-radius:50%;
  display:flex;
  justify-content:center;
  align-items:center;
  background:linear-gradient(135deg,#8067ff,#00c8ff);
  font-weight:bold;
}

.content{
  padding:30px;
}

.page{
  display:none;
}

.page.active{
  display:block;
}


/* =========================
   HERO
========================= */

.hero{
  min-height:330px;
  padding:45px;
  border-radius:25px;
  background:
  radial-gradient(
    circle at 85% 30%,
    rgba(128,103,255,.5),
    transparent 25%
  ),
  radial-gradient(
    circle at 90% 100%,
    rgba(0,200,255,.18),
    transparent 30%
  ),
  linear-gradient(120deg,#17142c,#0e1523);
  border:1px solid #2b2e41;
}

.badge{
  display:inline-block;
  padding:7px 12px;
  border-radius:20px;
  background:#211d3b;
  border:1px solid #514694;
  color:#bcb3ff;
  font-size:11px;
  letter-spacing:1px;
  margin-bottom:18px;
}

.hero h1{
  font-size:clamp(38px,5vw,62px);
  line-height:1;
  margin-bottom:18px;
}

.hero h1 span{
  background:linear-gradient(90deg,#a08cff,#63d9ff);
  -webkit-background-clip:text;
  color:transparent;
}

.hero p{
  color:#a8adbd;
  max-width:600px;
  line-height:1.7;
  margin-bottom:25px;
}


/* =========================
   BUTTONS
========================= */

.btn{
  border:0;
  padding:12px 18px;
  border-radius:10px;
  font-weight:bold;
  margin-right:8px;
}

.primary{
  background:#8067ff;
  color:white;
}

.secondary{
  background:#191c28;
  color:white;
  border:1px solid #34384b;
}

.danger{
  background:#e84d5b;
  color:white;
}

.success{
  background:#1eae70;
  color:white;
}


/* =========================
   SECTION
========================= */

.section{
  margin-top:40px;
}

.section-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:17px;
}

.section-head h2{
  font-size:22px;
}

.section-head span{
  color:#7f72d8;
  font-size:13px;
}


/* =========================
   CARDS
========================= */

.cards{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:15px;
}

.card{
  background:#10121b;
  border:1px solid #242737;
  border-radius:15px;
  overflow:hidden;
  transition:.25s;
}

.card:hover{
  transform:translateY(-5px);
  border-color:#6655c9;
}

.poster{
  height:210px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:50px;
  background:
  radial-gradient(circle,#51419a,transparent 50%),
  linear-gradient(145deg,#282342,#101521);
}

.card-info{
  padding:13px;
}

.card-info h3{
  font-size:15px;
  margin-bottom:7px;
}

.card-info p{
  color:#727788;
  font-size:12px;
}

.progress{
  height:4px;
  background:#292c38;
  margin-top:12px;
}

.progress div{
  height:100%;
  background:#8067ff;
}

.card-actions{
  display:flex;
  gap:6px;
  margin-top:12px;
}

.card-actions button{
  flex:1;
  border:1px solid #34384b;
  background:#191c28;
  color:white;
  padding:7px;
  border-radius:7px;
  font-size:11px;
}


/* =========================
   SMALL CARDS
========================= */

.small-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
}

.small-card{
  padding:18px;
  background:#10121b;
  border:1px solid #242737;
  border-radius:15px;
}

.small-card .icon{
  font-size:28px;
  margin-bottom:12px;
}

.small-card h3{
  margin-bottom:7px;
}

.small-card p{
  color:#74798a;
  font-size:12px;
  line-height:1.5;
}


/* =========================
   FILTERS
========================= */

.filters{
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  margin-bottom:20px;
}

.filter{
  padding:9px 14px;
  border-radius:20px;
  background:#11131c;
  border:1px solid #292d3d;
  color:#aeb2c2;
}

.filter:hover{
  border-color:#8067ff;
  color:white;
}


/* =========================
   CALENDAR
========================= */

.calendar{
  display:grid;
  grid-template-columns:repeat(7,1fr);
  gap:10px;
}

.day{
  min-height:100px;
  padding:13px;
  border-radius:12px;
  background:#10121b;
  border:1px solid #242737;
}

.day strong{
  display:block;
  margin-bottom:10px;
}

.day span{
  color:#8f82ee;
  font-size:11px;
}


/* =========================
   SETTINGS
========================= */

.settings{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:15px;
}

.setting{
  padding:20px;
  border-radius:15px;
  background:#10121b;
  border:1px solid #242737;
}

.setting h3{
  margin-bottom:8px;
}

.setting p{
  color:#74798a;
  font-size:13px;
  margin-bottom:15px;
}

.setting button,
.setting select{
  padding:9px 14px;
  border-radius:8px;
  border:1px solid #34384b;
  background:#191c28;
  color:white;
}


/* =========================
   PROFILE
========================= */

.profile-box{
  padding:30px;
  border-radius:20px;
  background:linear-gradient(145deg,#15142a,#10131c);
  border:1px solid #2a2d40;
}

.big-avatar{
  width:80px;
  height:80px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:30px;
  font-weight:bold;
  background:linear-gradient(135deg,#8067ff,#00c8ff);
  margin-bottom:15px;
}

.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:12px;
  margin-top:20px;
}

.stat{
  padding:18px;
  background:#10121b;
  border:1px solid #242737;
  border-radius:14px;
}

.stat strong{
  display:block;
  font-size:23px;
  margin-bottom:5px;
}

.stat span{
  color:#707587;
  font-size:12px;
}


/* =========================
   NOTIFICATIONS
========================= */

.notice{
  padding:17px;
  border-radius:13px;
  background:#10121b;
  border:1px solid #242737;
  margin-bottom:10px;
}

.notice strong{
  display:block;
  margin-bottom:5px;
}

.notice span{
  color:#74798a;
  font-size:12px;
}


/* =========================
   LOGIN
========================= */

.auth-box{
  max-width:430px;
  margin:40px auto;
  padding:30px;
  background:#10121b;
  border:1px solid #292d3d;
  border-radius:20px;
}

.auth-box h2{
  margin-bottom:8px;
}

.auth-box p{
  color:#74798a;
  font-size:13px;
  margin-bottom:25px;
}

.auth-input{
  width:100%;
  padding:13px;
  margin-bottom:12px;
  border-radius:9px;
  border:1px solid #303447;
  background:#0b0d14;
  color:white;
  outline:none;
}

.auth-input:focus{
  border-color:#8067ff;
}

.auth-box .btn{
  width:100%;
  margin:5px 0;
}


/* =========================
   VIDEO PLAYER
========================= */

.video-box{
  background:#050509;
  border-radius:18px;
  overflow:hidden;
  border:1px solid #272a3a;
}

.video-box video{
  width:100%;
  max-height:600px;
  display:block;
  background:black;
}

.video-controls{
  padding:15px;
  display:flex;
  align-items:center;
  gap:10px;
  flex-wrap:wrap;
  background:#11131c;
}

.video-controls button,
.video-controls select{
  padding:8px 12px;
  border-radius:8px;
  border:1px solid #34384b;
  background:#191c28;
  color:white;
}

.video-info{
  padding:20px;
  background:#10121b;
}

.video-info h2{
  margin-bottom:8px;
}

.video-info p{
  color:#777d8e;
  line-height:1.6;
}


/* =========================
   MANGA READER
========================= */

.reader{
  max-width:850px;
  margin:auto;
}

.manga-page{
  min-height:500px;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  border-radius:15px;
  background:
  linear-gradient(
    135deg,
    #eeeeee,
    #cfcfcf
  );
  color:#111;
  font-size:70px;
  font-weight:bold;
}

.reader-controls{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:15px;
  margin-top:15px;
}

.reader-controls button{
  padding:10px 18px;
  border-radius:8px;
  border:1px solid #34384b;
  background:#191c28;
  color:white;
}


/* =========================
   ADMIN
========================= */

.admin-box{
  padding:25px;
  background:#10121b;
  border:1px solid #292d3d;
  border-radius:18px;
}

.admin-form{
  display:grid;
  gap:12px;
  max-width:600px;
}

.admin-form input,
.admin-form textarea,
.admin-form select{
  width:100%;
  padding:12px;
  border-radius:8px;
  border:1px solid #303447;
  background:#0b0d14;
  color:white;
}

.admin-form textarea{
  min-height:120px;
  resize:vertical;
}


/* =========================
   MODAL
========================= */

.modal{
  position:fixed;
  inset:0;
  display:none;
  align-items:center;
  justify-content:center;
  background:rgba(0,0,0,.75);
  z-index:2000;
  padding:20px;
}

.modal.show{
  display:flex;
}

.modal-box{
  width:min(500px,100%);
  background:#10121b;
  border:1px solid #34384b;
  border-radius:18px;
  padding:25px;
}

.modal-box h2{
  margin-bottom:10px;
}

.modal-box p{
  color:#858a9b;
  line-height:1.6;
  margin-bottom:20px;
}


/* =========================
   FOOTER
========================= */

footer{
  margin-top:60px;
  padding:30px;
  border-top:1px solid #222534;
  text-align:center;
  color:#626778;
  font-size:12px;
}


/* =========================
   LIGHT THEME
========================= */

body.light{
  background:#f4f5f8;
  color:#111;
}

body.light .sidebar{
  background:#ffffff;
  border-color:#ddd;
}

body.light .main{
  background:#f4f5f8;
}

body.light .topbar{
  background:rgba(255,255,255,.9);
  border-color:#ddd;
}

body.light .search{
  background:#fff;
  color:#111;
  border-color:#ccc;
}

body.light .card,
body.light .small-card,
body.light .setting,
body.light .stat,
body.light .notice,
body.light .auth-box,
body.light .admin-box{
  background:#fff;
  border-color:#ddd;
  color:#111;
}

body.light .card-info p,
body.light .small-card p,
body.light .setting p,
body.light .stat span,
body.light .notice span,
body.light .auth-box p,
body.light .video-info p{
  color:#666;
}

body.light .top-btn{
  background:#fff;
  color:#111;
}

body.light .sidebar .menu button{
  color:#555;
}

body.light .sidebar .menu button:hover,
body.light .sidebar .menu button.active{
  background:#eeeafa;
  color:#111;
}


/* =========================
   RESPONSIVE
========================= */

@media(max-width:1000px){

  .cards{
    grid-template-columns:repeat(3,1fr);
  }

  .small-grid{
    grid-template-columns:repeat(2,1fr);
  }

}

@media(max-width:750px){

  .sidebar{
    width:70px;
    padding:20px 8px;
  }

  .logo{
    font-size:19px;
    text-align:center;
    margin-left:0;
    margin-right:0;
  }

  .menu-title{
    display:none;
  }

  .menu button{
    text-align:center;
    font-size:0;
  }

  .menu button:first-letter{
    font-size:18px;
  }

  .main{
    margin-left:70px;
  }

  .content{
    padding:18px;
  }

  .cards{
    grid-template-columns:repeat(2,1fr);
  }

  .calendar{
    grid-template-columns:repeat(2,1fr);
  }

  .stats{
    grid-template-columns:repeat(2,1fr);
  }

  .settings{
    grid-template-columns:1fr;
  }

}

@media(max-width:500px){

  .topbar{
    padding:0 12px;
  }

  .search{
    width:70%;
  }

  .avatar{
    display:none;
  }

  .hero{
    padding:28px 22px;
  }

  .cards{
    grid-template-columns:1fr 1fr;
  }

  .poster{
    height:170px;
  }

  .small-grid{
    grid-template-columns:1fr;
  }

}

</style>
</head>


<body>


<!-- =========================
     SIDEBAR
========================= -->

<aside class="sidebar">

  <div class="logo">
    NIMO<span>+</span>
  </div>

  <div class="menu-title">DISCOVER</div>

  <div class="menu">

    <button class="active"
      onclick="showPage('home',this)">
      🏠 Home
    </button>

    <button onclick="showPage('trending',this)">
      🔥 Trending
    </button>

    <button onclick="showPage('recommended',this)">
      🎯 Recommended
    </button>

    <button onclick="showPage('calendar',this)">
      📅 Calendar
    </button>

    <button onclick="showPage('anime',this)">
      🎬 Anime
    </button>

    <button onclick="showPage('manga',this)">
      📖 Manga
    </button>

  </div>


  <div class="menu-title">
    MY NIMO
  </div>

  <div class="menu">

    <button onclick="showPage('watchlist',this)">
      💾 Watchlist
    </button>

    <button onclick="showPage('history',this)">
      🕘 History
    </button>

    <button onclick="showPage('stats',this)">
      📊 My Stats
    </button>

    <button onclick="showPage('profile',this)">
      👤 Profile
    </button>

    <button onclick="showPage('notifications',this)">
      🔔 Notifications
    </button>

    <button onclick="showPage('settings',this)">
      ⚙️ Settings
    </button>

  </div>


  <div class="menu-title">
    CREATOR
  </div>

  <div class="menu">

    <button onclick="showPage('admin',this)">
      🛠️ Admin
    </button>

  </div>

</aside>



<!-- =========================
     MAIN
========================= -->

<main class="main">


<header class="topbar">

  <input
    class="search"
    id="search"
    placeholder="Search anime, manga, genres..."
  >

  <div class="top-right">

    <button
      class="top-btn"
      onclick="showPage('notifications',null)">
      🔔
    </button>

    <div
      class="avatar"
      id="topAvatar">
      N
    </div>

  </div>

</header>



<div class="content">


<!-- =========================
     HOME
========================= -->

<section id="home" class="page active">

  <div class="hero">

    <div class="badge">
      NIMO+ NEXT EXPERIENCE
    </div>

    <h1>
      Your world.<br>
      Your <span>Stories.</span>
    </h1>

    <p>
      Discover anime, manga, stories and new worlds.
      Build your personal collection and continue
      where you left off.
    </p>

    <button
      class="btn primary"
      onclick="showPage('trending',null)">
      🔥 Explore Trending
    </button>

    <button
      class="btn secondary"
      onclick="showPage('watchlist',null)">
      💾 My Watchlist
    </button>

  </div>


  <div class="section">

    <div class="section-head">
      <h2>▶ Continue Watching</h2>
      <span>View all →</span>
    </div>


    <div class="cards">


      <div class="card searchable">

        <div class="poster">
          ⚔️
        </div>

        <div class="card-info">

          <h3>Adventure World</h3>

          <p>
            Episode 08 • 72% watched
          </p>

          <div class="progress">
            <div style="width:72%"></div>
          </div>

          <div class="card-actions">

            <button
              onclick="openVideo('Adventure World','Episode 08')">
              ▶ Watch
            </button>

            <button
              onclick="addHistory('Adventure World')">
              + History
            </button>

          </div>

        </div>

      </div>



      <div class="card searchable">

        <div class="poster">
          🔥
        </div>

        <div class="card-info">

          <h3>Flame Hero</h3>

          <p>
            Episode 14 • 45% watched
          </p>

          <div class="progress">
            <div style="width:45%"></div>
          </div>

          <div class="card-actions">

            <button
              onclick="openVideo('Flame Hero','Episode 14')">
              ▶ Watch
            </button>

            <button
              onclick="addHistory('Flame Hero')">
              + History
            </button>

          </div>

        </div>

      </div>



      <div class="card searchable">

        <div class="poster">
          🌙
        </div>

        <div class="card-info">

          <h3>Moon Mystery</h3>

          <p>
            Episode 03 • 28% watched
          </p>

          <div class="progress">
            <div style="width:28%"></div>
          </div>

          <div class="card-actions">

            <button
              onclick="openVideo('Moon Mystery','Episode 03')">
              ▶ Watch
            </button>

            <button
              onclick="addHistory('Moon Mystery')">
              + History
            </button>

          </div>

        </div>

      </div>



      <div class="card searchable">

        <div class="poster">
          ⚡
        </div>

        <div class="card-info">

          <h3>Lightning Days</h3>

          <p>
            Episode 21 • 81% watched
          </p>

          <div class="progress">
            <div style="width:81%"></div>
          </div>

          <div class="card-actions">

            <button
              onclick="openVideo('Lightning Days','Episode 21')">
              ▶ Watch
            </button>

            <button
              onclick="addHistory('Lightning Days')">
              + History
            </button>

          </div>

        </div>

      </div>



      <div class="card searchable">

        <div class="poster">
          🌌
        </div>

        <div class="card-info">

          <h3>Galaxy Story</h3>

          <p>
            Episode 06 • 34% watched
          </p>

          <div class="progress">
            <div style="width:34%"></div>
          </div>

          <div class="card-actions">

            <button
              onclick="openVideo('Galaxy Story','Episode 06')">
              ▶ Watch
            </button>

            <button
              onclick="addHistory('Galaxy Story')">
              + History
            </button>

          </div>

        </div>

      </div>

    </div>

  </div>


  <div class="section">

    <div class="section-head">
      <h2>🆕 Recently Added</h2>
      <span>See all →</span>
    </div>

    <div class="small-grid">

      <div class="small-card">
        <div class="icon">🌊</div>
        <h3>Ocean Dreams</h3>
        <p>New episode added today.</p>
      </div>

      <div class="small-card">
        <div class="icon">🐉</div>
        <h3>Dragon Realm</h3>
        <p>New series added.</p>
      </div>

      <div class="small-card">
        <div class="icon">🚀</div>
        <h3>Space Mission</h3>
        <p>Season 2 available.</p>
      </div>

      <div class="small-card">
        <div class="icon">🧩</div>
        <h3>Mystery Code</h3>
        <p>New mystery series.</p>
      </div>

    </div>

  </div>

</section>



<!-- =========================
     TRENDING
========================= -->

<section id="trending" class="page">

  <div class="section-head">
    <h2>🔥 Trending Now</h2>
    <span>Updated daily</span>
  </div>

  <div class="filters">

    <button class="filter">
      All
    </button>

    <button class="filter">
      Action
    </button>

    <button class="filter">
      Comedy
    </button>

    <button class="filter">
      Fantasy
    </button>

    <button class="filter">
      Mystery
    </button>

    <button class="filter">
      Sports
    </button>

  </div>


  <div class="cards">


    <div class="card searchable">

      <div class="poster">
        🔥
      </div>

      <div class="card-info">

        <h3>Flame Hero</h3>

        <p>
          Action • Fantasy
        </p>

        <div class="card-actions">

          <button
            onclick="addWatchlist('Flame Hero')">
            💾 Save
          </button>

          <button
            onclick="openVideo('Flame Hero','Episode 01')">
            ▶ Watch
          </button>

        </div>

      </div>

    </div>



    <div class="card searchable">

      <div class="poster">
        ⚔️
      </div>

      <div class="card-info">

        <h3>Final Warrior</h3>

        <p>
          Action • Adventure
        </p>

        <div class="card-actions">

          <button
            onclick="addWatchlist('Final Warrior')">
            💾 Save
          </button>

          <button
            onclick="openVideo('Final Warrior','Episode 01')">
            ▶ Watch
          </button>

        </div>

      </div>

    </div>



    <div class="card searchable">

      <div class="poster">
        😂
      </div>

      <div class="card-info">

        <h3>Funny Days</h3>

        <p>
          Comedy
        </p>

        <div class="card-actions">

          <button
            onclick="addWatchlist('Funny Days')">
            💾 Save
          </button>

          <button
            onclick="openVideo('Funny Days','Episode 01')">
            ▶ Watch
          </button>

        </div>

      </div>

    </div>



    <div class="card searchable">

      <div class="poster">
        🌌
      </div>

      <div class="card-info">

        <h3>Galaxy Story</h3>

        <p>
          Sci-Fi • Fantasy
        </p>

        <div class="card-actions">

          <button
            onclick="addWatchlist('Galaxy Story')">
            💾 Save
          </button>

          <button
            onclick="openVideo('Galaxy Story','Episode 01')">
            ▶ Watch
          </button>

        </div>

      </div>

    </div>



    <div class="card searchable">

      <div class="poster">
        🏆
      </div>

      <div class="card-info">

        <h3>Champion</h3>

        <p>
          Sports
        </p>

        <div class="card-actions">

          <button
            onclick="addWatchlist('Champion')">
            💾 Save
          </button>

          <button
            onclick="openVideo('Champion','Episode 01')">
            ▶ Watch
          </button>

        </div>

      </div>

    </div>


  </div>

</section>



<!-- =========================
     RECOMMENDED
========================= -->

<section id="recommended" class="page">

  <div class="section-head">

    <h2>
      🎯 Recommended For You
    </h2>

    <span>
      Based on your activity
    </span>

  </div>


  <div class="cards">

    <div class="card searchable">
      <div class="poster">✨</div>
      <div class="card-info">
        <h3>Magic World</h3>
        <p>Fantasy • Adventure</p>
        <div class="card-actions">
          <button onclick="addWatchlist('Magic World')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">🔎</div>
      <div class="card-info">
        <h3>Hidden Truth</h3>
        <p>Mystery • Drama</p>
        <div class="card-actions">
          <button onclick="addWatchlist('Hidden Truth')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">⚡</div>
      <div class="card-info">
        <h3>Lightning Days</h3>
        <p>Action • Comedy</p>
        <div class="card-actions">
          <button onclick="addWatchlist('Lightning Days')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">🌙</div>
      <div class="card-info">
        <h3>Moon Mystery</h3>
        <p>Mystery</p>
        <div class="card-actions">
          <button onclick="addWatchlist('Moon Mystery')">
            💾 Save
          </button>
        </div>
      </div>
    </div>

  </div>

</section>



<!-- =========================
     CALENDAR
========================= -->

<section id="calendar" class="page">

  <div class="section-head">
    <h2>📅 Release Calendar</h2>
    <span>This week</span>
  </div>

  <div class="calendar">

    <div class="day">
      <strong>MON</strong>
      <span>Dragon Realm<br>EP 12</span>
    </div>

    <div class="day">
      <strong>TUE</strong>
      <span>Flame Hero<br>EP 15</span>
    </div>

    <div class="day">
      <strong>WED</strong>
      <span>Moon Mystery<br>EP 04</span>
    </div>

    <div class="day">
      <strong>THU</strong>
      <span>Galaxy Story<br>EP 07</span>
    </div>

    <div class="day">
      <strong>FRI</strong>
      <span>Final Warrior<br>EP 22</span>
    </div>

    <div class="day">
      <strong>SAT</strong>
      <span>Funny Days<br>EP 09</span>
    </div>

    <div class="day">
      <strong>SUN</strong>
      <span>Ocean Dreams<br>EP 03</span>
    </div>

  </div>

</section>



<!-- =========================
     ANIME
========================= -->

<section id="anime" class="page">

  <div class="section-head">

    <h2>
      🎬 Anime Library
    </h2>

    <span>
      Explore
    </span>

  </div>


  <div class="filters">

    <button class="filter">
      All
    </button>

    <button class="filter">
      Action
    </button>

    <button class="filter">
      Comedy
    </button>

    <button class="filter">
      Fantasy
    </button>

    <button class="filter">
      Mystery
    </button>

  </div>


  <div class="cards">

    <div class="card searchable">
      <div class="poster">⚔️</div>
      <div class="card-info">
        <h3>Adventure World</h3>
        <p>Adventure • 24 Episodes</p>
        <div class="card-actions">
          <button onclick="openVideo('Adventure World','Episode 01')">
            ▶ Watch
          </button>
          <button onclick="addWatchlist('Adventure World')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">🔥</div>
      <div class="card-info">
        <h3>Flame Hero</h3>
        <p>Fantasy • 15 Episodes</p>
        <div class="card-actions">
          <button onclick="openVideo('Flame Hero','Episode 01')">
            ▶ Watch
          </button>
          <button onclick="addWatchlist('Flame Hero')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">🌙</div>
      <div class="card-info">
        <h3>Moon Mystery</h3>
        <p>Mystery • 12 Episodes</p>
        <div class="card-actions">
          <button onclick="openVideo('Moon Mystery','Episode 01')">
            ▶ Watch
          </button>
          <button onclick="addWatchlist('Moon Mystery')">
            💾 Save
          </button>
        </div>
      </div>
    </div>


    <div class="card searchable">
      <div class="poster">🚀</div>
      <div class="card-info">
        <h3>Space Mission</h3>
        <p>Sci-Fi • 20 Episodes</p>
        <div class="card-actions">
          <button onclick="openVideo('Space Mission','Episode 01')">
            ▶ Watch
          </button>
          <button onclick="addWatchlist('Space Mission')">
            💾 Save
          </button>
        </div>
      </div>
    </div>

  </div>

</section>



<!-- =========================
     MANGA
========================= -->

<section id="manga" class="page">

  <div class="section-head">

    <h2>
      📖 Manga Library
    </h2>

    <span>
      Read stories
    </span>

  </div>


  <div class="cards">

    <div class="card searchable">

      <div class="poster">
        📕
      </div>

      <div class="card-info">

        <h3>Moon Mystery</h3>

        <p>
          Chapter 12 • Mystery
        </p>

        <div class="card-actions">

          <button
            onclick="openReader('Moon Mystery')">
            📖 Read
          </button>

          <button
            onclick="addWatchlist('Moon Mystery Manga')">
            💾 Save
          </button>

        </div>

      </div>

    </div>


    <div class="card searchable">

      <div class="poster">
        📗
      </div>

      <div class="card-info">

        <h3>Dragon Realm</h3>

        <p>
          Chapter 25 • Fantasy
        </p>

        <div class="card-actions">

          <button
            onclick="openReader('Dragon Realm')">
            📖 Read
          </button>

          <button
            onclick="addWatchlist('Dragon Realm Manga')">
            💾 Save
          </button>

        </div>

      </div>

    </div>


    <div class="card searchable">

      <div class="poster">
        📘
      </div>

      <div class="card-info">

        <h3>Ocean Dreams</h3>

        <p>
          Chapter 08 • Drama
        </p>

        <div class="card-actions">

          <button
            onclick="openReader('Ocean Dreams')">
            📖 Read
          </button>

          <button
            onclick="addWatchlist('Ocean Dreams Manga')">
            💾 Save
          </button>

        </div>

      </div>

    </div>

  </div>

</section>



<!-- =========================
     WATCHLIST
========================= -->

<section id="watchlist" class="page">

  <div class="section-head">

    <h2>
      💾 My Watchlist
    </h2>

    <span id="watchCount">
      0 saved
    </span>

  </div>

  <div
    id="watchlistContent"
    class="small-grid">
  </div>

</section>



<!-- =========================
     HISTORY
========================= -->

<section id="history" class="page">

  <div class="section-head">

    <h2>
      🕘 Watch History
    </h2>

    <button
      class="btn danger"
      onclick="clearHistory()">
      Clear
    </button>

  </div>

  <div
    id="historyContent"
    class="small-grid">
  </div>

</section>



<!-- =========================
     STATS
========================= -->

<section id="stats" class="page">

  <div class="section-head">

    <h2>
      📊 My NIMO Statistics
    </h2>

    <span>
      Your activity
    </span>

  </div>


  <div class="stats">

    <div class="stat">
      <strong id="episodeStat">
        47
      </strong>
      <span>
        Episodes watched
      </span>
    </div>

    <div class="stat">
      <strong>
        18h
      </strong>
      <span>
        Watch time
      </span>
    </div>

    <div class="stat">
      <strong>
        12
      </strong>
      <span>
        Anime completed
      </span>
    </div>

    <div class="stat">

      <strong id="favoriteStat">
        0
      </strong>

      <span>
        Saved items
      </span>

    </div>

  </div>

</section>



<!-- =========================
     PROFILE
========================= -->

<section id="profile" class="page">

  <div class="section-head">

    <h2>
      👤 My Profile
    </h2>

  </div>


  <div class="profile-box">

    <div
      class="big-avatar"
      id="profileAvatar">
      N
    </div>

    <h2 id="profileName">
      NIMO User
    </h2>

    <p
      id="profileEmail"
      style="color:#777d8e;margin-top:8px;">
      Not logged in
    </p>

    <br>

    <button
      class="btn primary"
      onclick="showPage('login',null)">
      Login / Sign Up
    </button>

  </div>

</section>



<!-- =========================
     NOTIFICATIONS
========================= -->

<section id="notifications" class="page">

  <div class="section-head">

    <h2>
      🔔 Notifications
    </h2>

    <span>
      3 new
    </span>

  </div>


  <div class="notice">

    <strong>
      🔥 New episode available
    </strong>

    <span>
      Flame Hero Episode 15 has been added.
    </span>

  </div>


  <div class="notice">

    <strong>
      📅 Upcoming episode
    </strong>

    <span>
      Dragon Realm releases tomorrow.
    </span>

  </div>


  <div class="notice">

    <strong>
      🎯 New recommendation
    </strong>

    <span>
      NIMO found a new series for you.
    </span>

  </div>

</section>



<!-- =========================
     SETTINGS
========================= -->

<section id="settings" class="page">

  <div class="section-head">

    <h2>
      ⚙️ Settings
    </h2>

    <span>
      NIMO Preferences
    </span>

  </div>


  <div class="settings">


    <div class="setting">

      <h3>
        🌙 Theme
      </h3>

      <p>
        Choose how NIMO looks.
      </p>

      <button onclick="toggleTheme()">
        Change Theme
      </button>

    </div>


    <div class="setting">

      <h3>
        🔔 Notifications
      </h3>

      <p>
        Control episode notifications.
      </p>

      <button onclick="alert('Notifications enabled')">
        Enabled
      </button>

    </div>


    <div class="setting">

      <h3>
        🎚️ Video Quality
      </h3>

      <p>
        Choose your preferred quality.
      </p>

      <select>

        <option>
          Auto
        </option>

        <option>
          1080p
        </option>

        <option>
          720p
        </option>

        <option>
          480p
        </option>

      </select>

    </div>


    <div class="setting">

      <h3>
        ▶️ Playback Speed
      </h3>

      <p>
        Choose playback speed.
      </p>

      <select
        id="globalSpeed"
        onchange="changeVideoSpeed(this.value)">

        <option value="1">
          1x
        </option>

        <option value="1.25">
          1.25x
        </option>

        <option value="1.5">
          1.5x
        </option>

        <option value="2">
          2x
        </option>

        <option value="3">
          3x
        </option>

      </select>

    </div>


  </div>

</section>



<!-- =========================
     LOGIN
========================= -->

<section id="login" class="page">

  <div class="auth-box">

    <h2>
      Welcome to NIMO+
    </h2>

    <p>
      Create a demo account or login.
    </p>


    <input
      class="auth-input"
      id="loginName"
      placeholder="Your name">


    <input
      class="auth-input"
      id="loginEmail"
      type="email"
      placeholder="Email">


    <input
      class="auth-input"
      id="loginPassword"
      type="password"
      placeholder="Password">


    <button
      class="btn primary"
      onclick="loginUser()">
      Login / Sign Up
    </button>


    <button
      class="btn secondary"
      onclick="logoutUser()">
      Logout
    </button>

  </div>

</section>



<!-- =========================
     VIDEO
========================= -->

<section id="video" class="page">

  <div class="section-head">

    <h2 id="videoTitle">
      Video Player
    </h2>

    <span id="episodeTitle">
      Episode
    </span>

  </div>


  <div class="video-box">

    <video
      id="videoPlayer"
      controls
      playsinline>

      <!--
      Add an authorized video URL here later.

      Example:

      <source
        src="YOUR_AUTHORIZED_VIDEO.mp4"
        type="video/mp4">

      -->

      Your browser does not support video.

    </video>


    <div class="video-controls">

      <button
        onclick="playVideo()">
        ▶ Play
      </button>

      <button
        onclick="pauseVideo()">
        ⏸ Pause
      </button>


      <select
        id="videoSpeed"
        onchange="changeVideoSpeed(this.value)">

        <option value="1">
          1x
        </option>

        <option value="1.25">
          1.25x
        </option>

        <option value="1.5">
          1.5x
        </option>

        <option value="2">
          2x
        </option>

        <option value="3">
          3x
        </option>

      </select>


      <button
        onclick="showPage('home',null)">
        ← Back
      </button>

    </div>


    <div class="video-info">

      <h2 id="videoInfoTitle">
        Select a title
      </h2>

      <p>
        This is the NIMO+ video player structure.
        Connect it later to your own or properly
        licensed/authorized video source.
      </p>

    </div>

  </div>

</section>



<!-- =========================
     MANGA READER
========================= -->

<section id="reader" class="page">

  <div class="section-head">

    <h2 id="readerTitle">
      Manga Reader
    </h2>

    <span id="readerPageNumber">
      Page 1
    </span>

  </div>


  <div class="reader">

    <div
      class="manga-page"
      id="mangaPage">

      PAGE 1

    </div>


    <div class="reader-controls">

      <button
        onclick="previousMangaPage()">
        ← Previous
      </button>

      <strong
        id="mangaCounter">
        1 / 5
      </strong>

      <button
        onclick="nextMangaPage()">
        Next →
      </button>

    </div>

  </div>

</section>



<!-- =========================
     ADMIN
========================= -->

<section id="admin" class="page">

  <div class="section-head">

    <h2>
      🛠️ NIMO Admin Panel
    </h2>

    <span>
      Content management
    </span>

  </div>


  <div class="admin-box">

    <h3>
      Add New Content
    </h3>

    <br>


    <div class="admin-form">


      <input
        id="adminTitle"
        placeholder="Anime / Manga title">


      <select id="adminType">

        <option>
          Anime
        </option>

        <option>
          Manga
        </option>

      </select>


      <input
        id="adminGenre"
        placeholder="Genre">


      <input
        id="adminEpisode"
        placeholder="Episode / Chapter">


      <textarea
        id="adminDescription"
        placeholder="Description">
      </textarea>


      <button
        class="btn primary"
        onclick="addAdminContent()">

        + Add Content

      </button>

    </div>


    <br>

    <div id="adminOutput"></div>

  </div>

</section>



<footer>

  <strong>
    NIMO+
  </strong>

  <br><br>

  Anime • Manga • Stories • Your World

  <br><br>

  Built with HTML, CSS & JavaScript

</footer>


</div>

</main>



<!-- =========================
     MODAL
========================= -->

<div
  class="modal"
  id="modal">

  <div class="modal-box">

    <h2 id="modalTitle">
      NIMO+
    </h2>

    <p id="modalText">
      Welcome.
    </p>

    <button
      class="btn primary"
      onclick="closeModal()">
      OK
    </button>

  </div>

</div>



<script>

/* =========================
   PAGE NAVIGATION
========================= */

function showPage(pageId,button){

  document
    .querySelectorAll(".page")
    .forEach(function(page){

      page.classList.remove("active");

    });


  const page =
    document.getElementById(pageId);


  if(page){

    page.classList.add("active");

  }


  document
    .querySelectorAll(".menu button")
    .forEach(function(btn){

      btn.classList.remove("active");

    });


  if(button){

    button.classList.add("active");

  }


  window.scrollTo({
    top:0,
    behavior:"smooth"
  });


  if(pageId==="watchlist"){
    renderWatchlist();
  }


  if(pageId==="history"){
    renderHistory();
  }

}


/* =========================
   SEARCH
========================= */

document
  .getElementById("search")
  .addEventListener("input",function(){

    const value =
      this.value.toLowerCase().trim();


    document
      .querySelectorAll(".searchable")
      .forEach(function(card){

        const text =
          card.innerText.toLowerCase();


        card.style.display =
          text.includes(value)
          ? ""
          : "none";

      });

  });


/* =========================
   LOCAL STORAGE HELPERS
========================= */

function getData(key){

  return JSON.parse(
    localStorage.getItem(key) || "[]"
  );

}


function saveData(key,data){

  localStorage.setItem(
    key,
    JSON.stringify(data)
  );

}


/* =========================
   WATCHLIST
========================= */

function addWatchlist(title){

  let list =
    getData("nimoWatchlist");


  if(!list.includes(title)){

    list.push(title);

    saveData(
      "nimoWatchlist",
      list
    );

    showModal(
      "Saved!",
      title + " has been added to your watchlist."
    );

  }else{

    showModal(
      "Already Saved",
      title + " is already in your watchlist."
    );

  }


  updateStats();

}


function renderWatchlist(){

  const container =
    document.getElementById(
      "watchlistContent"
    );


  const list =
    getData("nimoWatchlist");


  document.getElementById(
    "watchCount"
  ).textContent =
    list.length + " saved";


  if(list.length===0){

    container.innerHTML = `
      <div class="small-card">
        <div class="icon">💾</div>
        <h3>Your watchlist is empty</h3>
        <p>Save anime or manga to see them here.</p>
      </div>
    `;

    return;

  }


  container.innerHTML =
    list.map(function(title){

      return `
        <div class="small-card">

          <div class="icon">
            🎬
          </div>

          <h3>
            ${escapeHTML(title)}
          </h3>

          <p>
            Saved to your NIMO+ collection.
          </p>

          <br>

          <button
            class="btn primary"
            onclick="removeWatchlist('${escapeJS(title)}')">
            Remove
          </button>

        </div>
      `;

    }).join("");

}


function removeWatchlist(title){

  let list =
    getData("nimoWatchlist");


  list =
    list.filter(function(item){

      return item !== title;

    });


  saveData(
    "nimoWatchlist",
    list
  );


  renderWatchlist();

  updateStats();

}


/* =========================
   HISTORY
========================= */

function addHistory(title){

  let history =
    getData("nimoHistory");


  history =
    history.filter(function(item){

      return item !== title;

    });


  history.unshift(title);


  if(history.length>20){

    history =
      history.slice(0,20);

  }


  saveData(
    "nimoHistory",
    history
  );


  updateStats();

}


function renderHistory(){

  const container =
    document.getElementById(
      "historyContent"
    );


  const history =
    getData("nimoHistory");


  if(history.length===0){

    container.innerHTML = `
      <div class="small-card">
        <div class="icon">🕘</div>
        <h3>No history yet</h3>
        <p>Watched content will appear here.</p>
      </div>
    `;

    return;

  }


  container.innerHTML =
    history.map(function(title){

      return `
        <div class="small-card">

          <div class="icon">
            ▶️
          </div>

          <h3>
            ${escapeHTML(title)}
          </h3>

          <p>
            Recently watched.
          </p>

        </div>
      `;

    }).join("");

}


function clearHistory(){

  localStorage.removeItem(
    "nimoHistory"
  );

  renderHistory();

  updateStats();

}


/* =========================
   VIDEO PLAYER
========================= */

function openVideo(title,episode){

  document.getElementById(
    "videoTitle"
  ).textContent =
    title;


  document.getElementById(
    "episodeTitle"
  ).textContent =
    episode;


  document.getElementById(
    "videoInfoTitle"
  ).textContent =
    title + " — " + episode;


  addHistory(title);


  showPage(
    "video",
    null
  );

}


function playVideo(){

  const video =
    document.getElementById(
      "videoPlayer"
    );


  video.play();

}


function pauseVideo(){

  const video =
    document.getElementById(
      "videoPlayer"
    );


  video.pause();

}


function changeVideoSpeed(value){

  const video =
    document.getElementById(
      "videoPlayer"
    );


  video.playbackRate =
    Number(value);


  const speed =
    document.getElementById(
      "globalSpeed"
    );


  const videoSpeed =
    document.getElementById(
      "videoSpeed"
    );


  if(speed){
    speed.value = value;
  }


  if(videoSpeed){
    videoSpeed.value = value;
  }

}


/* =========================
   MANGA READER
========================= */

let mangaPage = 1;

let currentManga = "";


function openReader(title){

  currentManga =
    title;

  mangaPage =
    1;


  document.getElementById(
    "readerTitle"
  ).textContent =
    title;


  updateMangaReader();


  showPage(
    "reader",
    null
  );

}


function updateMangaReader(){

  document.getElementById(
    "mangaPage"
  ).textContent =
    "PAGE " + mangaPage;


  document.getElementById(
    "mangaCounter"
  ).textContent =
    mangaPage + " / 5";


  document.getElementById(
    "readerPageNumber"
  ).textContent =
    "Page " + mangaPage;

}


function nextMangaPage(){

  if(mangaPage<5){

    mangaPage++;

    updateMangaReader();

  }

}


function previousMangaPage(){

  if(mangaPage>1){

    mangaPage--;

    updateMangaReader();

  }

}


/* =========================
   LOGIN
========================= */

function loginUser(){

  const name =
    document
      .getElementById("loginName")
      .value
      .trim();


  const email =
    document
      .getElementById("loginEmail")
      .value
      .trim();


  const password =
    document
      .getElementById("loginPassword")
      .value;


  if(!name || !email || !password){

    showModal(
      "Missing information",
      "Please fill all fields."
    );

    return;

  }


  const user = {

    name:name,

    email:email

  };


  localStorage.setItem(
    "nimoUser",
    JSON.stringify(user)
  );


  updateUserUI();


  showModal(
    "Welcome!",
    "You are now logged in as " + name + "."
  );


  showPage(
    "profile",
    null
  );

}


function logoutUser(){

  localStorage.removeItem(
    "nimoUser"
  );


  updateUserUI();


  showModal(
    "Logged out",
    "Your demo account has been logged out."
  );

}


function updateUserUI(){

  const user =
    JSON.parse(
      localStorage.getItem(
        "nimoUser"
      )
    );


  if(user){

    document.getElementById(
      "profileName"
    ).textContent =
      user.name;


    document.getElementById(
      "profileEmail"
    ).textContent =
      user.email;


    document.getElementById(
      "profileAvatar"
    ).textContent =
      user.name.charAt(0).toUpperCase();


    document.getElementById(
      "topAvatar"
    ).textContent =
      user.name.charAt(0).toUpperCase();

  }else{

    document.getElementById(
      "profileName"
    ).textContent =
      "NIMO User";


    document.getElementById(
      "profileEmail"
    ).textContent =
      "Not logged in";


    document.getElementById(
      "profileAvatar"
    ).textContent =
      "N";


    document.getElementById(
      "topAvatar"
    ).textContent =
      "N";

  }

}


/* =========================
   THEME
========================= */

function toggleTheme(){

  document.body.classList.toggle(
    "light"
  );


  const light =
    document.body.classList.contains(
      "light"
    );


  localStorage.setItem(
    "nimoTheme",
    light
    ? "light"
    : "dark"
  );

}


function loadTheme(){

  const theme =
    localStorage.getItem(
      "nimoTheme"
    );


  if(theme==="light"){

    document.body.classList.add(
      "light"
    );

  }

}


/* =========================
   ADMIN CONTENT
========================= */

function addAdminContent(){

  const title =
    document
      .getElementById("adminTitle")
      .value
      .trim();


  const type =
    document
      .getElementById("adminType")
      .value;


  const genre =
    document
      .getElementById("adminGenre")
      .value
      .trim();


  const episode =
    document
      .getElementById("adminEpisode")
      .value
      .trim();


  const description =
    document
      .getElementById("adminDescription")
      .value
      .trim();


  if(!title){

    showModal(
      "Title required",
      "Please enter a title."
    );

    return;

  }


  const item = {

    title:title,

    type:type,

    genre:genre,

    episode:episode,

    description:description,

    createdAt:
      new Date().toLocaleString()

  };


  let content =
    getData("nimoAdminContent");


  content.push(item);


  saveData(
    "nimoAdminContent",
    content
  );


  document.getElementById(
    "adminOutput"
  ).innerHTML = `

    <div class="notice">

      <strong>
        ✅ Content added
      </strong>

      <span>
        ${escapeHTML(title)}
        •
        ${escapeHTML(type)}
        •
        ${escapeHTML(genre)}
      </span>

    </div>

  `;


  document.getElementById(
    "adminTitle"
  ).value = "";


  document.getElementById(
    "adminGenre"
  ).value = "";


  document.getElementById(
    "adminEpisode"
  ).value = "";


  document.getElementById(
    "adminDescription"
  ).value = "";

}


/* =========================
   STATS
========================= */

function updateStats(){

  const history =
    getData("nimoHistory");


  const watchlist =
    getData("nimoWatchlist");


  document.getElementById(
    "episodeStat"
  ).textContent =
    47 + history.length;


  document.getElementById(
    "favoriteStat"
  ).textContent =
    watchlist.length;

}


/* =========================
   MODAL
========================= */

function showModal(title,text){

  document.getElementById(
    "modalTitle"
  ).textContent =
    title;


  document.getElementById(
    "modalText"
  ).textContent =
    text;


  document.getElementById(
    "modal"
  ).classList.add(
    "show"
  );

}


function closeModal(){

  document.getElementById(
    "modal"
  ).classList.remove(
    "show"
  );

}


/* =========================
   SECURITY HELPERS
========================= */

function escapeHTML(text){

  return String(text)

    .replaceAll("&","&amp;")

    .replaceAll("<","&lt;")

    .replaceAll(">","&gt;")

    .replaceAll('"',"&quot;")

    .replaceAll("'","&#039;");

}


function escapeJS(text){

  return String(text)
    .replaceAll("\\","\\\\")
    .replaceAll("'","\\'");

}


/* =========================
   INITIALIZE
========================= */

loadTheme();

updateUserUI();

renderWatchlist();

renderHistory();

updateStats();

</script>

</body>
</html>
