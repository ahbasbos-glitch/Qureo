<!doctype html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#020604">
<title>ZENTRIX — حل كورساتك</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800&family=JetBrains+Mono:wght@400;600;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
<style>
/* ================= ZENTRIX — hacker theme ================= */
:root{
  --ink:#020604;--ink2:#04120b;--ink3:#061a10;
  --line:rgba(0,255,156,.12);--line2:rgba(0,255,156,.28);
  --text:#c8ffe0;--soft:#9effc4;--muted:#4f8f6d;
  --red:#00ff9c;--red2:#00d4ff;--deep:#006b3c;
  --ok:#00ff9c;--warn:#ffd23f;--info:#00d4ff;
  --radius:12px;
  --glow:0 0 0 1px rgba(0,255,156,.35),0 10px 40px rgba(0,255,156,.18);
}
*{box-sizing:border-box}
html{-webkit-text-size-adjust:100%;overflow-x:hidden;scroll-behavior:smooth}
body{margin:0;min-height:100vh;overflow-x:hidden;background:var(--ink);color:var(--text);font-family:"JetBrains Mono","Cairo",ui-monospace,monospace;line-height:1.7}
body::before{content:"";position:fixed;inset:0;z-index:-2;background:
  radial-gradient(900px 520px at 88% -8%,rgba(0,255,156,.16),transparent 62%),
  radial-gradient(700px 480px at -6% 100%,rgba(0,212,255,.10),transparent 60%),
  repeating-linear-gradient(0deg,rgba(0,255,156,.035) 0 1px,transparent 1px 3px),
  repeating-linear-gradient(90deg,rgba(0,255,156,.02) 0 1px,transparent 1px 60px)}
body::after{content:"";position:fixed;inset:0;z-index:-1;pointer-events:none;background:linear-gradient(180deg,transparent 0%,rgba(0,255,156,.05) 50%,transparent 100%);animation:scan 7s linear infinite}
@keyframes scan{0%{transform:translateY(-100%)}100%{transform:translateY(100vh)}}
#fx{position:fixed;inset:0;width:100%;height:100%;z-index:-1;pointer-events:none;opacity:.7}
button,input,select,textarea{font:inherit;color:inherit}
button{cursor:pointer}button:disabled{cursor:not-allowed;opacity:.5}
a{color:var(--red)}
:focus-visible{outline:2px solid var(--red);outline-offset:2px}
.hidden{display:none!important}
.num{font-family:"JetBrains Mono","Space Grotesk",monospace;direction:ltr;unicode-bidi:isolate}
.mono{font-family:"JetBrains Mono",ui-monospace,Consolas,monospace}
.shell{width:min(1200px,calc(100% - 32px));margin:0 auto;padding:14px 0 44px}
.disp{font-family:"JetBrains Mono","Cairo",monospace;font-weight:700;letter-spacing:.05em}

.ann{position:relative;display:flex;align-items:center;justify-content:center;gap:12px;flex-wrap:wrap;padding:9px 16px;background:linear-gradient(90deg,var(--deep),var(--red) 50%,var(--red2));color:#020604;font-size:13px;font-weight:700;text-align:center;letter-spacing:.04em}
.ann small{opacity:.85;font-weight:700}
.ann button{border:0;background:rgba(0,0,0,.35);color:#020604;border-radius:6px;padding:2px 9px;font-size:12px}

.topbar{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:12px 0 18px}
.brand{display:flex;align-items:center;gap:11px;text-decoration:none;color:var(--text)}
.brand svg{width:42px;height:42px;filter:drop-shadow(0 0 14px rgba(0,255,156,.7))}
.brand strong{display:block;font-family:"JetBrains Mono","Cairo",monospace;font-size:22px;font-weight:700;letter-spacing:.15em;color:var(--red);text-shadow:0 0 12px rgba(0,255,156,.8)}
.brand small{display:block;color:var(--muted);font-size:10px;letter-spacing:.25em;text-transform:uppercase}
.top-actions{display:flex;gap:8px;align-items:center;flex-wrap:wrap;justify-content:flex-end}
.pill{display:inline-flex;align-items:center;gap:8px;min-height:38px;padding:0 14px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,255,156,.04);color:var(--soft);font-family:"JetBrains Mono","Cairo",monospace;font-size:12.5px;font-weight:600;letter-spacing:.05em;text-decoration:none;text-transform:uppercase}
.pill i{width:8px;height:8px;border-radius:50%;background:var(--ok);box-shadow:0 0 12px var(--ok);animation:blink 1.8s infinite}
.pill.off i{background:#ff5a7a;box-shadow:0 0 10px #ff5a7a;animation:none}
a.pill:hover,button.pill:hover{border-color:var(--red);color:var(--red);background:rgba(0,255,156,.08)}
@keyframes blink{50%{opacity:.35}}
.pill.shiny{border:1px solid var(--red);color:var(--red);background:rgba(0,255,156,.08);box-shadow:0 0 18px rgba(0,255,156,.35);animation:glowp 2.4s ease-in-out infinite;font-weight:700;text-shadow:0 0 8px rgba(0,255,156,.8)}
.pill.shiny:hover{filter:brightness(1.2);color:var(--red)}
@keyframes glowp{50%{box-shadow:0 0 34px rgba(0,255,156,.8)}}

.btn{min-height:48px;display:inline-flex;align-items:center;justify-content:center;gap:9px;padding:0 22px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,255,156,.04);color:var(--text);font-family:"JetBrains Mono","Cairo",monospace;font-weight:700;letter-spacing:.04em;text-transform:uppercase;text-decoration:none;transition:transform .15s,filter .15s,border-color .15s,background .15s,box-shadow .15s;font-size:13px}
.btn:hover:not(:disabled){transform:translateY(-1px);border-color:var(--red);background:rgba(0,255,156,.10);box-shadow:0 0 20px rgba(0,255,156,.35)}
.btn.primary{border:1px solid var(--red);background:linear-gradient(135deg,rgba(0,255,156,.18),rgba(0,212,255,.18));color:#eafff5;box-shadow:0 0 0 1px rgba(0,255,156,.4),0 0 24px rgba(0,255,156,.35),inset 0 0 20px rgba(0,255,156,.08);text-shadow:0 0 8px rgba(0,255,156,.8)}
.btn.primary:hover:not(:disabled){filter:brightness(1.2);box-shadow:0 0 0 1px rgba(0,255,156,.6),0 0 32px rgba(0,255,156,.6)}
.btn.danger{color:#ff5a7a;border-color:rgba(255,90,122,.4)}
.btn.sm{min-height:34px;padding:0 13px;font-size:11px;border-radius:6px}
.btn.full{width:100%}.btn.big{min-height:54px;font-size:14px;padding:0 30px}

.hero{display:grid;grid-template-columns:minmax(0,1.25fr) minmax(280px,.75fr);gap:28px;align-items:center;padding:6px 0 14px}
.hero h1{margin:0 0 14px;font-family:"JetBrains Mono","Cairo",monospace;font-weight:700;font-size:clamp(34px,5.6vw,62px);line-height:1.12;letter-spacing:-.02em;text-transform:uppercase}
.hero h1::before{content:"> ";color:var(--red);text-shadow:0 0 12px var(--red)}
.hero h1 em{display:block;font-style:normal;background:linear-gradient(100deg,#00ff9c,#00d4ff 60%,#7cffcb);-webkit-background-clip:text;background-clip:text;color:transparent;filter:drop-shadow(0 0 20px rgba(0,255,156,.5))}
.hero h1 em::after{content:"_";color:var(--red);animation:blink 1s steps(1) infinite;-webkit-text-fill-color:var(--red)}
.hero p{margin:0 0 22px;max-width:56ch;color:var(--soft);font-size:14.5px;opacity:.9}
.hero-cta{display:flex;gap:10px;flex-wrap:wrap}
.board{border:1px solid var(--line2);border-radius:12px;background:linear-gradient(160deg,rgba(0,255,156,.08),rgba(0,0,0,.4) 55%);padding:2px 18px;box-shadow:var(--glow)}
.board-row{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:10px 0;border-bottom:1px dashed var(--line)}
.board-row:last-child{border:0}
.board-row span{color:var(--muted);font-size:12px;font-weight:600;letter-spacing:.03em}
.board-row b{font-family:"JetBrains Mono","Cairo",monospace;font-size:26px;font-weight:700;color:var(--red);text-shadow:0 0 20px rgba(0,255,156,.9),0 0 40px rgba(0,255,156,.4)}
.board-row b small{font-family:"Cairo",sans-serif;font-size:13px;color:var(--muted);margin-inline-start:5px;text-shadow:none;font-weight:600}

.section-head{display:flex;align-items:flex-end;justify-content:space-between;gap:14px;flex-wrap:wrap;margin:14px 0 8px}
.section-head h2{margin:0;font-family:"JetBrains Mono","Cairo",monospace;font-size:26px;font-weight:700;color:var(--red);text-transform:uppercase;letter-spacing:.05em}
.section-head p{margin:2px 0 0;color:var(--muted);font-size:13px}
.group-title{margin:10px 0 7px;color:var(--soft);font-size:12.5px;font-weight:700;display:flex;align-items:center;gap:10px;letter-spacing:.05em;text-transform:uppercase;white-space:nowrap}
.group-title::after{content:"";flex:1;height:1px;background:linear-gradient(90deg,var(--line2),transparent)}
.plans{display:flex;flex-wrap:wrap;gap:9px}
.plan{flex:0 0 146px;width:146px;position:relative;display:flex;flex-direction:column;gap:3px;padding:11px 12px;border:1px solid var(--line2);border-radius:10px;background:linear-gradient(180deg,rgba(6,26,16,.9),rgba(2,6,4,.9));overflow:hidden;transition:transform .2s,border-color .2s,box-shadow .2s;font-family:"JetBrains Mono","Cairo",monospace}
.plan:hover{transform:translateY(-4px);border-color:var(--red);box-shadow:0 0 28px rgba(0,255,156,.3)}
.plan.hot{border:1.5px solid transparent;background:linear-gradient(rgba(6,26,16,.95),rgba(2,6,4,.95)) padding-box,conic-gradient(from var(--ang,0deg),#00ff9c,#00d4ff,#7cffcb,#00ff9c) border-box;animation:spin 5s linear infinite}
@property --ang{syntax:"<angle>";initial-value:0deg;inherits:false}
@keyframes spin{to{--ang:360deg}}
.plan h3{margin:0;font-size:13.5px;color:var(--text);text-transform:uppercase;letter-spacing:.04em}
.plan .d{margin:0;color:var(--muted);font-size:11px;min-height:0}
.plan .price{display:flex;align-items:baseline;gap:8px;margin:2px 0}
.plan .price b{font-family:"JetBrains Mono",monospace;font-size:28px;font-weight:700;color:var(--red);text-shadow:0 0 24px rgba(0,255,156,.8)}
.plan .price span{color:var(--muted);font-size:11px;font-weight:600}
.plan .price s{color:var(--muted);font-family:"JetBrains Mono",monospace;font-size:13px;opacity:.8}
.plan ul{margin:0 0 4px;padding:0;list-style:none;color:var(--soft);font-size:11px;font-weight:600}
.plan ul li{padding:0}
.plan .btn{min-height:30px;font-size:11.5px;padding:0 10px;margin-top:auto}
.ribbon{position:absolute;top:8px;left:8px;padding:1px 9px;border-radius:4px;background:var(--red);color:#020604;font-family:"JetBrains Mono",monospace;font-size:10px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;box-shadow:0 0 16px rgba(0,255,156,.7)}
.how{margin:8px 0 0;color:var(--muted);font-size:11.5px}.how b{color:var(--soft)}

.tabs{display:flex;gap:0;flex-wrap:wrap;margin:16px 0 12px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,0,0,.4);width:fit-content;max-width:100%;overflow:hidden}
.tab{height:42px;padding:0 20px;border:0;background:transparent;color:var(--muted);font-family:"JetBrains Mono","Cairo",monospace;font-size:13px;font-weight:600;letter-spacing:.05em;text-transform:uppercase;border-left:1px solid var(--line)}
.tab:first-child{border-left:0}
.tab:hover{color:var(--red);background:rgba(0,255,156,.05)}
.tab.on{background:rgba(0,255,156,.12);color:var(--red);text-shadow:0 0 10px rgba(0,255,156,.8);box-shadow:inset 0 0 20px rgba(0,255,156,.15)}
.tabs.tight-tabs{margin:0 0 10px;width:100%}.tight-tabs .tab{flex:1}
.tab .badge{margin-inline-start:6px;padding:1px 8px}
.resume{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;margin-bottom:14px;padding:12px 16px;border:1px solid var(--red);border-radius:8px;background:rgba(0,255,156,.08);font-size:13px;font-weight:700;box-shadow:0 0 20px rgba(0,255,156,.2)}

.layout{display:grid;grid-template-columns:minmax(320px,.85fr) minmax(0,1.15fr);gap:16px;align-items:start}
.panel{border:1px solid var(--line2);border-radius:12px;background:linear-gradient(180deg,rgba(6,26,16,.92),rgba(2,6,4,.95));padding:22px;backdrop-filter:blur(14px);position:relative}
.panel::before{content:"● ● ●";position:absolute;top:8px;right:14px;color:var(--red);font-size:9px;letter-spacing:4px;opacity:.55;font-family:"JetBrains Mono",monospace}
.panel-head{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-bottom:16px}
.panel-head h2{margin:0;font-family:"JetBrains Mono","Cairo",monospace;font-size:18px;font-weight:700;color:var(--red);text-transform:uppercase;letter-spacing:.05em}
.panel-head h2::before{content:"$ ";opacity:.6}
.panel-head p{margin:2px 0 0;color:var(--muted);font-size:12px}
.crumbs{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px}
.crumb{padding:5px 13px;border:1px solid var(--red);border-radius:6px;background:rgba(0,255,156,.08);color:var(--soft);font-size:11.5px;font-weight:700;letter-spacing:.03em}
.choices{display:grid;gap:10px;margin-bottom:6px}.choices.two{grid-template-columns:1fr 1fr}
.choice{display:flex;align-items:center;justify-content:space-between;gap:10px;width:100%;padding:16px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,255,156,.02);text-align:right;transition:border-color .15s,background .15s,transform .15s,box-shadow .15s;font-family:"JetBrains Mono","Cairo",monospace}
.choice:hover{border-color:var(--red);background:rgba(0,255,156,.08);transform:translateX(-2px);box-shadow:0 0 20px rgba(0,255,156,.25)}
.choice strong{display:block;font-size:14px}.choice small{display:block;color:var(--muted);font-size:11px}
.choice .tag{flex:none;font-family:"JetBrains Mono",monospace;font-weight:700;font-size:10.5px;color:var(--red);padding:3px 9px;border-radius:4px;background:rgba(0,255,156,.12);border:1px solid rgba(0,255,156,.3)}
.field{display:grid;gap:7px;margin-bottom:14px}
.field label{color:var(--soft);font-family:"JetBrains Mono","Cairo",monospace;font-size:11px;font-weight:600;letter-spacing:.1em;text-transform:uppercase}
.field label::before{content:"[ ";color:var(--red)}
.field label::after{content:" ]";color:var(--red)}
.input,.select,.textarea{width:100%;min-height:48px;padding:0 14px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,0,0,.6);outline:none;color:var(--text);font-family:"JetBrains Mono","Cairo",monospace;transition:border-color .15s,box-shadow .15s}
.textarea{min-height:170px;padding:12px 14px;resize:vertical;font:12.5px/1.9 "JetBrains Mono",ui-monospace,monospace;direction:ltr;text-align:left}
.input:focus,.select:focus,.textarea:focus{border-color:var(--red);box-shadow:0 0 0 3px rgba(0,255,156,.15),0 0 20px rgba(0,255,156,.3)}
.input::placeholder,.textarea::placeholder{color:var(--muted);opacity:.55}
.select option{background:#061a10;color:#c8ffe0}
.hp{position:absolute;top:0;right:0;width:1px;height:1px;opacity:0;pointer-events:none;overflow:hidden}
.msg{min-height:20px;margin:8px 0 0;font-size:12.5px;font-weight:700;color:var(--ok);letter-spacing:.02em}.msg.err{color:#ff5a7a}
.hint{margin:6px 0 0;color:var(--muted);font-size:11.5px}
.empty{padding:40px 16px;border:1px dashed var(--line2);border-radius:10px;color:var(--muted);text-align:center;font-size:12.5px}
.badge{display:inline-flex;align-items:center;gap:5px;padding:3px 10px;border-radius:4px;font-family:"JetBrains Mono",monospace;font-size:10px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;white-space:nowrap;border:1px solid currentColor;background:rgba(0,0,0,.4)}
.badge.queued,.badge.pending,.badge.review{color:var(--warn)}
.badge.running,.badge.approved,.badge.success,.badge.done{color:var(--ok);text-shadow:0 0 8px rgba(0,255,156,.6)}
.badge.partial{color:var(--warn)}
.badge.failed,.badge.rejected{color:#ff5a7a}
.badge.cancelled{color:var(--muted)}

.ticket{position:relative;display:grid;grid-template-columns:auto 1fr;gap:22px;align-items:center;padding:22px;border-radius:12px;background:linear-gradient(135deg,rgba(0,255,156,.14),rgba(0,0,0,.5) 60%);border:1px solid var(--red);box-shadow:var(--glow);margin-bottom:14px}
.ticket::before,.ticket::after{content:"";position:absolute;top:50%;width:18px;height:18px;margin-top:-9px;border-radius:50%;background:var(--ink2);border:1px solid var(--red)}
.ticket::before{right:-10px}.ticket::after{left:-10px}
.ring{position:relative;width:128px;height:128px}
.ring svg{width:128px;height:128px;transform:rotate(-90deg)}
.ring circle{fill:none;stroke-width:8;stroke-linecap:round}
.ring .bg{stroke:rgba(0,255,156,.1)}
.ring .fg{stroke:var(--red);transition:stroke-dashoffset .8s ease;filter:drop-shadow(0 0 8px rgba(0,255,156,.9))}
.ring-n{position:absolute;inset:0;display:grid;place-content:center;text-align:center;line-height:1}
.ring-n b{font-family:"JetBrains Mono",monospace;font-size:46px;font-weight:700;color:var(--red);text-shadow:0 0 26px rgba(0,255,156,.9)}
.ring-n small{margin-top:6px;color:var(--muted);font-size:11px;font-weight:600;letter-spacing:.05em}
.ticket.go .ring .fg{stroke:var(--ok);filter:drop-shadow(0 0 8px rgba(0,255,156,.9))}
.ticket h3{margin:0 0 4px;font-family:"JetBrains Mono","Cairo",monospace;font-size:18px;font-weight:700;color:var(--red);text-transform:uppercase;letter-spacing:.04em}
.ticket p{margin:0;color:var(--soft);font-size:12.5px;opacity:.9}
.ticket .row-actions{margin-top:12px}
.row-actions{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}

.term{border:1px solid var(--line2);border-radius:10px;overflow:hidden;background:#000805;box-shadow:0 0 24px rgba(0,255,156,.15),inset 0 0 60px rgba(0,255,156,.03)}
.term-bar{display:flex;align-items:center;gap:7px;padding:9px 13px;background:linear-gradient(180deg,#04120b,#020604);border-bottom:1px solid var(--line)}
.term-bar i{width:11px;height:11px;border-radius:50%;background:#0a2418}
.term-bar i:nth-child(1){background:#00ff9c}.term-bar i:nth-child(2){background:#00d4ff}.term-bar i:nth-child(3){background:#ffd23f}
.term-title{margin:0 8px;flex:1;color:var(--muted);font-family:"JetBrains Mono",monospace;font-size:11px;letter-spacing:.03em;direction:ltr;text-align:left;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.term-live{display:inline-flex;align-items:center;gap:6px;color:var(--ok);font-family:"JetBrains Mono",monospace;font-weight:700;font-size:10.5px;letter-spacing:.1em}
.term-live::before{content:"";width:7px;height:7px;border-radius:50%;background:currentColor;box-shadow:0 0 10px currentColor;animation:blink 1.2s infinite}
.term-live.off{color:var(--muted)}.term-live.off::before{animation:none;box-shadow:none}
.term-body{max-height:340px;min-height:150px;overflow:auto;padding:12px 4px 12px 12px;font:12px/1.85 "JetBrains Mono",ui-monospace,monospace;direction:rtl;text-align:right;scrollbar-width:thin;scrollbar-color:#0a2418 transparent;color:var(--text)}
.term.mini .term-body{max-height:150px;min-height:0;font-size:11px;padding:8px}
.ln{display:grid;grid-template-columns:62px 16px 1fr;gap:8px;padding:0 6px;border-inline-start:2px solid transparent}
.ln time{color:#2f6b4c;font-size:10.5px;direction:ltr;text-align:left}
.ln .g{color:var(--muted);text-align:center}
.ln .m{color:#b8ffd6;white-space:pre-wrap;overflow-wrap:anywhere}
.ln.ok .g,.ln.ok .m{color:var(--ok);text-shadow:0 0 6px rgba(0,255,156,.5)}.ln.ok{border-color:rgba(0,255,156,.5)}
.ln.err .g,.ln.err .m{color:#ff5a7a}.ln.err{border-color:rgba(255,90,122,.7);background:rgba(255,90,122,.06)}
.ln.wrn .g,.ln.wrn .m{color:var(--warn)}.ln.wrn{border-color:rgba(255,210,63,.5)}
.cursor{display:inline-block;width:8px;height:14px;margin:0 8px;background:var(--red);vertical-align:middle;animation:blink 1s steps(1) infinite;box-shadow:0 0 8px var(--red)}
.term-empty{padding:26px;text-align:center;color:var(--muted);font-size:12px}
.bar{height:9px;border-radius:99px;background:rgba(0,255,156,.08);overflow:hidden;margin:14px 0}
.bar>div{height:100%;width:0;border-radius:99px;background:linear-gradient(90deg,var(--deep),var(--red),var(--red2));box-shadow:0 0 14px rgba(0,255,156,.7);transition:width .6s}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin:12px 0}
.stat{padding:12px 14px;border:1px solid var(--line2);border-radius:8px;background:rgba(0,255,156,.03)}
.stat strong{display:block;font-family:"JetBrains Mono","Cairo",monospace;font-size:22px;font-weight:700;color:var(--red);text-shadow:0 0 12px rgba(0,255,156,.6)}.stat span{color:var(--muted);font-size:11px;letter-spacing:.03em}
.job-head{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-bottom:12px}
.job-head b{font-size:14px;color:var(--red);letter-spacing:.03em}.job-head small{color:var(--muted);display:block;direction:ltr;text-align:right;font-size:11px}
.result{padding:16px 18px;bor# Qureo
