<!DOCTYPE html>
<html>
<head>
  <link rel="canonical" href="https://peaplant.github.io/biocalculator/mole"/>
  <meta charset="utf-8">
  <title>Biology calculator</title>
  <link rel="stylesheet" href="style.css" />
  <script src="jquery-3.5.1.min.js"></script>
  <script src="javafile.js"></script>

</head>

<body>
<script src="javafile.js"></script>
  <!-- !!dark mode code!!
    <input type="button" value="Dark" onclick="
      DarkMode(this)">
  -->
  <header class="ib">
  <h1 class="ib">Biology Calculator&ensp;&nbsp;&nbsp;</h1>
  </header>

  <div class="blueborder ib">
    <div class="flex_container">
    <h3 style="margin-left: 0.5vw; ">Timer 1</h3>
    <button onclick="timer1_reset()" id="button_reset1" style="height: 2vw; width: 5vw; margin-left: 0.45vw; font-size: 1vw; margin-right :0.5vw; position: relative; left:3vw;" class=inputclass_timer>Reset</button>
  </div>
  <div class="flex_container">
      <input id="timer1_h" style="margin-left: 0.5vw; " class="inputclass_timer" placeholder="Hour">
      <input id="timer1_m" class="inputclass_timer" placeholder="Min.">
      <input id="timer1_s" style="margin-right: 0.5vw; "class="inputclass_timer" placeholder="Sec.">
  </div>
      <div class="flex_container">
      <button onclick="stopwatch_1()" id="button_timer1" style="height: 2.5vw; width: 6.5vw; margin-left: 0.45vw; margin-right :0.5vw;" class="inputclass_timer">Start</button>
      <textarea id="result_timer1" style="width : 8vw; font-size: 1.6vw;"class="inputclass_timer" placeholder="hh:mm:ss" readonly></textarea>
  </div>
</div><div class="blueborder ib">
  <div class="flex_container">
  <h3 style="margin-left: 0.5vw; ">Timer 2</h3>
  <button onclick="timer2_reset" id="button_reset2" style="height: 2vw; width: 5vw; margin-left: 0.45vw; font-size: 1vw; margin-right :0.5vw; position: relative; left:3vw;" class=inputclass_timer>Reset</button>
</div>
  <div class="flex_container">
    <input id="timer2_h" style="margin-left: 0.5vw; " class="inputclass_timer" placeholder="Hour">
    <input id="timer2_m" class="inputclass_timer" placeholder="Min.">
    <input id="timer2_s" style="margin-right: 0.5vw; "class="inputclass_timer" placeholder="Sec.">
  </div>
    <div class="flex_container">
    <button onclick="stopwatch_2()" id="button_timer2" style="height: 2.5vw; width: 6.5vw; margin-left: 0.45vw; margin-right :0.5vw;" class="inputclass_timer">Start</button>
    <textarea id="result_timer2" style="width : 8vw; font-size: 1.6vw;"class="inputclass_timer" placeholder="hh:mm:ss"></textarea>
</div>
</div>
<p style="text-align: right; margin: 0vw; position:relative; right:7vw; font-size: 1.5vw;"> *Please allow pop-ups to get the timer alarm </p>
<nav>
  <div class="grid">
    <a href="mole.html">
      <div class="shape blue1" id="touch">Mole</div></a>
    <a href="seeding.html">
      <div class="shape blue2" id="touch">Seeding</div></a>
    <a href="cell_stock.html">
      <div class="shape blue3" id="touch">Cell Stock</div></a>
      <a href="cell_counting.html">
        <div style="font-size: 2.7vw; padding-top: 1vw;" class="shape blue5" id="touch" >Cell Counting</div></a>
    <a href="DNA.html">
      <div class="shape blue4" id="touch">DNA Tm</div></a>

  </div>
</nav>
<div class="sidenav">
<div class="comments" id="touch">
  <a href="comments.html">&nbsp;&nbsp;&nbsp;Comments&nbsp;&nbsp;&nbsp;</a>
</div><!-- forum
  <div class="qa" id="touch">
  <a href="qa.html">&nbsp;Experiment Q&A&nbsp;</a>
</div> -->
</div>
  <div class="backcolor back1">
<article>
    <div class="position1">
      <h2 id="t">How much salt should be put to make solution</h2>

        <h3>M.W.</h3>
        <input id="mtog_value" class="inputclass" placeholder="Molecular Weight">
      <div>
        <h3>Concentration</h3>
        <input id="mtog_concentration" class="inputclass"  placeholder="Concentration">
        <span>
          <select name ="mol" class="inputclass"  id="select_mol">
            <option value ="1">M</option>
            <option value="1000" selected="selected">mM</option>
            <option value="1000000">µM</option>
            <option value="1000000000">nM</option>
          </select>
        </span>
      </div>
      <div>
        <h3>Volume of solution</h3>
        <input id="mtog_liquid" class="inputclass"  placeholder="Volume of solvent">
        <span>
          <select name ="volume" class="inputclass"  id="select_vol">
            <option value ="1">L</option>
            <option value="1000" selected="selected">mL</option>
            <option value="1000000">µL</option>
            <option value="1000000000">nL</option>
          </select>
        </span>
      </div>
      <span class="flex_container">
        <button onclick="MtoG()" class="button inputclass">calculate</button>
        <textarea id="mtog_result" class ="result_left inputclass" placeholder="Weight of salt" readonly></textarea>
      </span>
    </div>
    <br>
    <div class="position1">
    <h2 id="t">How much stock should be put to make solution of lower concentration</h2>
    <div>
      <h3>Stock concentration</h3>
        <input id="stos_stock" class="inputclass"  placeholder="Stock concentration">
        <span>
          <select name ="mol" class="inputclass"  id="stos_select_mol_stock">
            <option value ="1">M</option>
            <option value="1000" selected="selected">mM</option>
            <option value="1000000">µM</option>
            <option value="1000000000">nM</option>
          </select>
        </span>
      </div>
      <div>
        <h3>Solution concentration</h3>
        <input id="stos_solution" class="inputclass"  placeholder="Solution conc. you want">
        <span>
          <select name ="mol" class="inputclass"  id="stos_select_mol_sol">
            <option value ="1">M</option>
            <option value="1000" selected="selected">mM</option>
            <option value="1000000">µM</option>
            <option value="1000000000">nM</option>
          </select>
        </span>
      </div>
      <div>
        <h3>Volume of solution</h3>
        <input id="stos_solvent" class="inputclass"  placeholder="Volume of solution">
        <span>
          <select name ="volume" class="inputclass"  id="stos_select_sov">
            <option value ="1">L</option>
            <option value="1000" selected="selected">mL</option>
            <option value="1000000">µL</option>
            <option value="1000000000">nL</option>
          </select>
        </span>
      </div>
      <div>
        <div class="flex_container">
            <button onclick="StoS()" class="button inputclass">calculate</button>
            <textarea id="stos_result" class ="result_left inputclass" placeholder="Volume of stock" readonly></textarea>
            <textarea id="stos_result2" class ="result_middle inputclass" placeholder="Volume of solvent" readonly></textarea>
        </div>
      </div>
   </div>
   <textarea id="hidden_1" hidden style="width: 1px; height: 1px"></textarea>
   <textarea id="hidden_2" hidden style="width: 1px; height: 1px"></textarea>



 </article>
 <footer>
   <div class="position1">
   <p><br><br>Feedback & ad request : baneling200@gmail.com <br>
      Copyright ⓒ 2020. Logan Go. All Rights Reserved. </p>
    </div>
 </footer>
 </div>


  <!--<div>
    <input type="button" value="Javacheck" onclick="msg()"/>
  </div> -->


</body>


</html>
