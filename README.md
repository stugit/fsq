<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>README</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">deuces</span> <span class="k">import</span> <span class="n">Card</span>
<span class="kn">from</span> <span class="nn">deuces</span> <span class="k">import</span> <span class="n">Evaluator</span>
<span class="n">evaluator</span> <span class="o">=</span> <span class="n">Evaluator</span><span class="p">()</span>

<span class="kn">from</span> <span class="nn">deuces</span> <span class="k">import</span> <span class="n">Deck</span>
<span class="n">deck</span> <span class="o">=</span> <span class="n">Deck</span><span class="p">()</span>
<span class="n">board</span> <span class="o">=</span> <span class="n">deck</span><span class="o">.</span><span class="n">draw</span><span class="p">(</span><span class="mi">5</span><span class="p">)</span>
<span class="n">player1_hand</span> <span class="o">=</span> <span class="n">deck</span><span class="o">.</span><span class="n">draw</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
<span class="n">player2_hand</span> <span class="o">=</span> <span class="n">deck</span><span class="o">.</span><span class="n">draw</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>

<span class="n">Card</span><span class="o">.</span><span class="n">print_pretty_cards</span><span class="p">(</span><span class="n">board</span><span class="p">)</span>
<span class="n">Card</span><span class="o">.</span><span class="n">print_pretty_cards</span><span class="p">(</span><span class="n">player1_hand</span><span class="p">)</span>
<span class="n">Card</span><span class="o">.</span><span class="n">print_pretty_cards</span><span class="p">(</span><span class="n">player2_hand</span><span class="p">)</span>

<span class="n">p1_score</span> <span class="o">=</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">evaluate</span><span class="p">(</span><span class="n">board</span><span class="p">,</span> <span class="n">player1_hand</span><span class="p">)</span>
<span class="n">p2_score</span> <span class="o">=</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">evaluate</span><span class="p">(</span><span class="n">board</span><span class="p">,</span> <span class="n">player2_hand</span><span class="p">)</span>
<span class="n">p1_class</span> <span class="o">=</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">get_rank_class</span><span class="p">(</span><span class="n">p1_score</span><span class="p">)</span>
<span class="n">p2_class</span> <span class="o">=</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">get_rank_class</span><span class="p">(</span><span class="n">p2_score</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Player 1 hand rank = </span><span class="si">%d</span><span class="s2"> (</span><span class="si">%s</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">p1_score</span><span class="p">,</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">class_to_string</span><span class="p">(</span><span class="n">p1_class</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Player 2 hand rank = </span><span class="si">%d</span><span class="s2"> (</span><span class="si">%s</span><span class="s2">)</span><span class="se">\n</span><span class="s2">&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">p2_score</span><span class="p">,</span> <span class="n">evaluator</span><span class="o">.</span><span class="n">class_to_string</span><span class="p">(</span><span class="n">p2_class</span><span class="p">)))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>  [ A ♠ ] , [ 9 ♣ ] , [ 7 ❤ ] , [ 5 ❤ ] , [ A ❤ ]  
  [ Q ♠ ] , [ 5 ♦ ]  
  [ 2 ❤ ] , [ 2 ♠ ]  
Player 1 hand rank = 2557 (Two Pair)

Player 2 hand rank = 2593 (Two Pair)

</pre>
</div>
</div>

</div>
</div>

</div>
    </div>
  </div>
</body>
</html>
