[ร้านขายไอเทม.html](https://github.com/user-attachments/files/33364562/default.html)
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>ร้านขายไอเทม</title>
<style>
:root{--bg:#f6efe6;--card:#fff;--tx:#2b1d12;--mu:#8a7766;--ac:#c4571a;--bd:#e4d6c6;--ok:#2e7d32;--no:#9e9e9e;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#1b130d;--card:#2a1d13;--tx:#f3e6d6;--mu:#a8927c;--ac:#ee8a3c;--bd:#442f20;--ok:#7bd37f;--no:#777}}
:root[data-theme="dark"]{--bg:#1b130d;--card:#2a1d13;--tx:#f3e6d6;--mu:#a8927c;--ac:#ee8a3c;--bd:#442f20;--ok:#7bd37f;--no:#777}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--tx);font-family:"Noto Sans Thai",system-ui,sans-serif;line-height:1.5}
.w{max-width:960px;margin:0 auto;padding:16px}
h1{margin:8px 0 2px;font-size:1.6rem}
.sub{color:var(--mu);margin:0 0 14px}
.promo{display:grid;gap:8px;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));margin-bottom:14px}
.pb{background:var(--card);border:1px dashed var(--ac);border-radius:12px;padding:10px 12px;font-size:.92rem}
.pb b{color:var(--ac)}
input[type=search]{width:100%;padding:10px 12px;border-radius:10px;border:1px solid var(--bd);background:var(--card);color:var(--tx);font:inherit;margin-bottom:12px}
.g{display:grid;gap:10px;grid-template-columns:repeat(auto-fill,minmax(210px,1fr))}
.c{background:var(--card);border:1px solid var(--bd);border-radius:12px;padding:12px;display:flex;flex-direction:column;gap:6px}
.c.so{opacity:.55}
.h{grid-column:1/-1;margin:10px 0 0;font-size:1.05rem;color:var(--ac);border-bottom:1px solid var(--bd);padding-bottom:4px}
.n{font-weight:600}
.p{font-size:1.25rem;color:var(--ac);font-weight:700}
.st{font-size:.82rem;color:var(--ok)}.so .st{color:var(--no)}
.q{display:flex;align-items:center;gap:8px;margin-top:auto}
button{font:inherit;border:0;border-radius:8px;cursor:pointer}
.q button{width:32px;height:32px;background:var(--bd);color:var(--tx);font-weight:700}
.q span{min-width:24px;text-align:center}
.cart{position:sticky;bottom:0;margin-top:16px;background:var(--card);border:1px solid var(--ac);border-radius:14px;padding:12px;box-shadow:0 -4px 16px rgba(0,0,0,.12)}
.cart pre{white-space:pre-wrap;margin:6px 0;font:inherit;font-size:.9rem;color:var(--mu)}
.row{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap}
.go{background:var(--ac);color:#fff;padding:9px 16px;font-weight:600}
.ghost{background:var(--bd);color:var(--tx);padding:9px 12px}
.ft{color:var(--mu);font-size:.85rem;text-align:center;margin:18px 0 8px}
</style>
</head>
<body>
<div class="w">
<h1>🛒 ร้านขายไอเทม</h1>
<p class="sub">เลือกของ กดสั่ง แล้วคัดลอกรายการไปทักแชทได้เลย</p>
<div class="promo">
<div class="pb"><b>เซ็ต</b> Vampiric Talisman + Lucky Coin = <b>150฿</b></div>
<div class="pb"><b>เซ็ต</b> Halo + Sanctifying Luminousness = <b>170฿</b></div>
<div class="pb"><b>เซ็ต</b> Chaos Stone + Nightglass Staff = <b>90฿</b></div>
<div class="pb"><b>เหมา</b> อย่างละ 1 ชิ้น = <b>700฿</b></div>
<div class="pb"><b>🎁 แถมฟรี</b> ไอเทม Veil-O-Ween ระดับ Elite 1 ชิ้น เมื่อซื้อแบบเซ็ตและเหมา</div>
</div>
<input type="search" id="s" placeholder="ค้นหาไอเทม...">
<div class="g" id="g"></div>
<div class="cart">
<div class="row"><b>รายการสั่งซื้อ</b><b id="t">0฿</b></div>
<pre id="o">ยังไม่ได้เลือกของ</pre>
<div class="row"><span style="color:var(--mu);font-size:.85rem">ต่อรองได้ ทักถามได้เลย</span>
<span><button class="ghost" id="r">ล้าง</button> <button class="go" id="cp">คัดลอกรายการ</button></span></div>
</div>
<p class="ft">สนใจเม้นใต้โพสต์ หรือทักแชทเฟซบุ๊กได้เลยครับ</p>
</div>
<script>
// name, price, stock (0 = sold out, null = in stock, count unknown), category
const M='Mythic',L='Legendary',E='Elite',V='Veil-O-Ween',X='Misc';
const items=[
["The Convergence",150,1,M],["Omniwarp",100,4,M],["Halo",150,null,M],
["Vampiric Talisman",120,2,L],["Rampaging Ribcage",70,null,L],["Chaos Stone",60,2,L],["The Weightless Crown",80,3,L],
["Lucky Coin",70,6,L],["Soul Shroud",35,2,L],["Unyielding Darkness",0,0,L],["Armageddon",0,0,L],
["Sanctifying Luminousness",35,null,L],["Scourge of Disease",50,null,L],["Staff of Voidrending",0,0,L],
["Shadowbeam Staff",30,4,E],["Extraterrestrial Transmitter",30,4,E],
["Pumpking",50,null,V],["Wicked Boom",40,null,V],["Spine of Dread",50,null,V],["Nightglass Staff",40,null,V],
["Witch Hat",25,null,V],["Vampire Cape",25,null,V],["Devil Horns",25,null,V],["Bat Wings",40,null,V],
["Gallow's Perch",35,null,V],["Gourdkeeper",35,null,V],
["Stone Accord",1,60,X],["Idol of Hatred",1,74,X]
].map(([n,p,s,c])=>({n,p,s:s??9,u:s==null,c,q:0}));
const g=document.getElementById('g');
function render(){
 const f=document.getElementById('s').value.toLowerCase();
 g.innerHTML='';let last='';
 items.forEach((it,i)=>{
  if(!it.n.toLowerCase().includes(f))return;
  if(it.c!==last){last=it.c;const h=document.createElement('h2');h.className='h';h.textContent=it.c;g.appendChild(h);}
  const so=it.s===0,d=document.createElement('div');
  d.className='c'+(so?' so':'');
  d.innerHTML=`<div class="n">${it.n}</div><div class="p">${so?'หมด':it.p+'฿'+(it.p===1?' / ชิ้น':'')}</div><div class="st">${so?'สินค้าหมด':it.u?'มีของ':'เหลือ '+it.s+' ชิ้น'}</div>`;
  if(!so){const q=document.createElement('div');q.className='q';
   q.innerHTML=`<button data-i="${i}" data-d="-1">−</button><span>${it.q}</span><button data-i="${i}" data-d="1">+</button>`;d.appendChild(q);}
  g.appendChild(d);
 });
 const sel=items.filter(x=>x.q>0);
 const tot=sel.reduce((a,x)=>a+x.p*x.q,0);
 document.getElementById('t').textContent=tot+'฿';
 document.getElementById('o').textContent=sel.length?sel.map(x=>`• ${x.n} x${x.q} = ${x.p*x.q}฿`).join('\n')+`\nรวม ${tot}฿`:'ยังไม่ได้เลือกของ';
}
g.addEventListener('click',e=>{
 const b=e.target.closest('button');if(!b)return;
 const it=items[b.dataset.i];it.q=Math.max(0,Math.min(it.s,it.q+Number(b.dataset.d)));render();
});
document.getElementById('s').addEventListener('input',render);
document.getElementById('r').onclick=()=>{items.forEach(x=>x.q=0);render()};
document.getElementById('cp').onclick=async()=>{
 const txt='สนใจสั่งซื้อครับ\n'+document.getElementById('o').textContent,b=document.getElementById('cp');
 try{await navigator.clipboard.writeText(txt)}catch(e){const a=document.createElement('textarea');a.value=txt;document.body.appendChild(a);a.select();try{document.execCommand('copy')}catch(_){}a.remove()}
 b.textContent='คัดลอกแล้ว ✓';setTimeout(()=>b.textContent='คัดลอกรายการ',1500);
};
render();
</script>
</body>
</html>
