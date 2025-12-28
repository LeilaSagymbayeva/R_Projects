<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.6.42">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>Visualizations Sample</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1em; /* quarto-specific, see https://github.com/quarto-dev/quarto-cli/issues/4556 */ 
  vertical-align: middle;
}
/* CSS for syntax highlighting */
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { display: inline-block; text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
  }
pre.numberSource { margin-left: 3em;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
</style>


<script src="Visualizations Sample_files/libs/clipboard/clipboard.min.js"></script>
<script src="Visualizations Sample_files/libs/quarto-html/quarto.js"></script>
<script src="Visualizations Sample_files/libs/quarto-html/popper.min.js"></script>
<script src="Visualizations Sample_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="Visualizations Sample_files/libs/quarto-html/anchor.min.js"></script>
<link href="Visualizations Sample_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="Visualizations Sample_files/libs/quarto-html/quarto-syntax-highlighting-2f5df379a58b258e96c21c0638c20c03.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="Visualizations Sample_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="Visualizations Sample_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="Visualizations Sample_files/libs/bootstrap/bootstrap-c0367b04c37547644fece4185067e4a7.min.css" rel="stylesheet" append-hash="true" id="quarto-bootstrap" data-mode="light">


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">

<header id="title-block-header" class="quarto-title-block default">
<div class="quarto-title">
<h1 class="title">Visualizations Sample</h1>
</div>



<div class="quarto-title-meta">

    
  
    
  </div>
  


</header>


<p>Sample 1: Bar Chart</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(tidyverse)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
✔ dplyr     1.1.4     ✔ readr     2.1.5
✔ forcats   1.0.0     ✔ stringr   1.5.1
✔ ggplot2   3.5.2     ✔ tibble    3.3.0
✔ lubridate 1.9.4     ✔ tidyr     1.3.1
✔ purrr     1.1.0     
── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
✖ dplyr::filter() masks stats::filter()
✖ dplyr::lag()    masks stats::lag()
ℹ Use the conflicted package (&lt;http://conflicted.r-lib.org/&gt;) to force all conflicts to become errors</code></pre>
</div>
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>venezuela <span class="ot">&lt;-</span> <span class="fu">read_csv</span>(<span class="st">"https://www.dropbox.com/scl/fi/6k0rgp4h504f9s06vanl3/RESULTADOS_2024_CSV_V2.csv?rlkey=tkcbyqja4bk0cka6uh7cqfgcy&amp;dl=1"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Rows: 25073 Columns: 21
── Column specification ────────────────────────────────────────────────────────
Delimiter: ","
chr  (4): EDO, MUN, PAR, URL
dbl (17): COD_EDO, COD_MUN, COD_PAR, CENTRO, MESA, VOTOS_VALIDOS, VOTOS_NULO...

ℹ Use `spec()` to retrieve the full column specification for this data.
ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.</code></pre>
</div>
<div class="sourceCode cell-code" id="cb5"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(venezuela)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 6 × 21
  COD_EDO EDO           COD_MUN MUN     COD_PAR PAR   CENTRO  MESA VOTOS_VALIDOS
    &lt;dbl&gt; &lt;chr&gt;           &lt;dbl&gt; &lt;chr&gt;     &lt;dbl&gt; &lt;chr&gt;  &lt;dbl&gt; &lt;dbl&gt;         &lt;dbl&gt;
1       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     1           449
2       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     2           416
3       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     3           468
4       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     1           448
5       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     2           455
6       1 DTTO. CAPITAL       1 MP. BL…       1 PQ. … 1.01e7     3           444
# ℹ 12 more variables: VOTOS_NULOS &lt;dbl&gt;, EG &lt;dbl&gt;, NM &lt;dbl&gt;, LM &lt;dbl&gt;,
#   JABE &lt;dbl&gt;, JOBR &lt;dbl&gt;, AE &lt;dbl&gt;, CF &lt;dbl&gt;, DC &lt;dbl&gt;, EM &lt;dbl&gt;, BERA &lt;dbl&gt;,
#   URL &lt;chr&gt;</code></pre>
</div>
<div class="sourceCode cell-code" id="cb7"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb7-1"><a href="#cb7-1" aria-hidden="true" tabindex="-1"></a><span class="fu">view</span>(venezuela)</span>
<span id="cb7-2"><a href="#cb7-2" aria-hidden="true" tabindex="-1"></a><span class="co"># Your code here:</span></span>
<span id="cb7-3"><a href="#cb7-3" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(venezuela<span class="sc">$</span>VOTOS_VALIDOS, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 10887262</code></pre>
</div>
<div class="sourceCode cell-code" id="cb9"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb9-1"><a href="#cb9-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Your code here:</span></span>
<span id="cb9-2"><a href="#cb9-2" aria-hidden="true" tabindex="-1"></a>venezuela <span class="ot">&lt;-</span> venezuela <span class="sc">|&gt;</span></span>
<span id="cb9-3"><a href="#cb9-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">Other =</span> <span class="fu">rowSums</span>(<span class="fu">across</span>(LM<span class="sc">:</span>BERA))) <span class="sc">|&gt;</span></span>
<span id="cb9-4"><a href="#cb9-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">relocate</span>(Other, <span class="at">.before =</span> URL)</span>
<span id="cb9-5"><a href="#cb9-5" aria-hidden="true" tabindex="-1"></a><span class="fu">view</span>(venezuela)</span>
<span id="cb9-6"><a href="#cb9-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb9-7"><a href="#cb9-7" aria-hidden="true" tabindex="-1"></a><span class="co"># percentage won by Gonzalez = 67.0828</span></span>
<span id="cb9-8"><a href="#cb9-8" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(venezuela<span class="sc">$</span>EG)<span class="sc">/</span><span class="dv">10887262</span><span class="sc">*</span><span class="dv">100</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 67.0828</code></pre>
</div>
<div class="sourceCode cell-code" id="cb11"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb11-1"><a href="#cb11-1" aria-hidden="true" tabindex="-1"></a><span class="co"># percentage won by Maduro = 30.45892</span></span>
<span id="cb11-2"><a href="#cb11-2" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(venezuela<span class="sc">$</span>NM)<span class="sc">/</span><span class="dv">10887262</span><span class="sc">*</span><span class="dv">100</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 30.45892</code></pre>
</div>
<div class="sourceCode cell-code" id="cb13"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb13-1"><a href="#cb13-1" aria-hidden="true" tabindex="-1"></a><span class="co"># percentage won by others in total = 2.458286</span></span>
<span id="cb13-2"><a href="#cb13-2" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(venezuela<span class="sc">$</span>Other)<span class="sc">/</span><span class="dv">10887262</span><span class="sc">*</span><span class="dv">100</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 2.458286</code></pre>
</div>
<div class="sourceCode cell-code" id="cb15"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(venezuela<span class="sc">$</span>NM)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 3316142</code></pre>
</div>
<div class="sourceCode cell-code" id="cb17"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb17-1"><a href="#cb17-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Your Code Here</span></span>
<span id="cb17-2"><a href="#cb17-2" aria-hidden="true" tabindex="-1"></a><span class="co"># In the first step I created the "gap" variable. </span></span>
<span id="cb17-3"><a href="#cb17-3" aria-hidden="true" tabindex="-1"></a>venezuela_summary <span class="ot">&lt;-</span> venezuela <span class="sc">|&gt;</span></span>
<span id="cb17-4"><a href="#cb17-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(EDO) <span class="sc">|&gt;</span></span>
<span id="cb17-5"><a href="#cb17-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(</span>
<span id="cb17-6"><a href="#cb17-6" aria-hidden="true" tabindex="-1"></a>    <span class="at">state_total =</span> <span class="fu">sum</span>(VOTOS_VALIDOS, <span class="at">na.rm =</span> <span class="cn">TRUE</span>),</span>
<span id="cb17-7"><a href="#cb17-7" aria-hidden="true" tabindex="-1"></a>    <span class="at">EG_total =</span> <span class="fu">sum</span>(EG, <span class="at">na.rm =</span> <span class="cn">TRUE</span>),</span>
<span id="cb17-8"><a href="#cb17-8" aria-hidden="true" tabindex="-1"></a>    <span class="at">NM_total =</span> <span class="fu">sum</span>(NM, <span class="at">na.rm =</span> <span class="cn">TRUE</span>),</span>
<span id="cb17-9"><a href="#cb17-9" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb17-10"><a href="#cb17-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">gap =</span> (EG_total <span class="sc">-</span> NM_total)<span class="sc">/</span>state_total<span class="sc">*</span><span class="dv">100</span>)</span>
<span id="cb17-11"><a href="#cb17-11" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb17-12"><a href="#cb17-12" aria-hidden="true" tabindex="-1"></a><span class="co"># Then I made a table as a beginner-friendly format, which I then used to plot the graph.</span></span>
<span id="cb17-13"><a href="#cb17-13" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb17-14"><a href="#cb17-14" aria-hidden="true" tabindex="-1"></a>venezuela_table <span class="ot">&lt;-</span> venezuela_summary <span class="sc">|&gt;</span></span>
<span id="cb17-15"><a href="#cb17-15" aria-hidden="true" tabindex="-1"></a>   <span class="fu">arrange</span>(<span class="fu">desc</span>(gap))<span class="sc">|&gt;</span></span>
<span id="cb17-16"><a href="#cb17-16" aria-hidden="true" tabindex="-1"></a>  <span class="fu">relocate</span>(gap, <span class="at">.before =</span> state_total)</span>
<span id="cb17-17"><a href="#cb17-17" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(venezuela_table)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code># A tibble: 6 × 5
  EDO             gap state_total EG_total NM_total
  &lt;chr&gt;         &lt;dbl&gt;       &lt;dbl&gt;    &lt;dbl&gt;    &lt;dbl&gt;
1 EDO. TACHIRA   65.6      486851   398690    79224
2 EDO. MERIDA    55.5      395027   303767    84482
3 EDO. BARINAS   50.7      379383   282585    90236
4 EDO. BOLIVAR   45.0      482762   343845   126557
5 EDO. CARABOBO  44.1      661107   466744   175133
6 EDO. FALCON    43.8      425682   301236   114586</code></pre>
</div>
<div class="sourceCode cell-code" id="cb19"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb19-1"><a href="#cb19-1" aria-hidden="true" tabindex="-1"></a>venezuela_graph1 <span class="ot">&lt;-</span> venezuela_table <span class="sc">|&gt;</span></span>
<span id="cb19-2"><a href="#cb19-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>() <span class="sc">+</span></span>
<span id="cb19-3"><a href="#cb19-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(<span class="at">x =</span> <span class="fu">reorder</span>(EDO, gap), <span class="at">y =</span> gap) <span class="sc">+</span></span>
<span id="cb19-4"><a href="#cb19-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_col</span>()<span class="sc">+</span></span>
<span id="cb19-5"><a href="#cb19-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_flip</span>() <span class="sc">+</span></span>
<span id="cb19-6"><a href="#cb19-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span> ( <span class="at">title =</span> <span class="st">"Presidential Election Results in Venezuela in 2024"</span>,</span>
<span id="cb19-7"><a href="#cb19-7" aria-hidden="true" tabindex="-1"></a>         <span class="at">x =</span> <span class="st">"State"</span>,</span>
<span id="cb19-8"><a href="#cb19-8" aria-hidden="true" tabindex="-1"></a>         <span class="at">y =</span> <span class="st">"Percentage Gap between Votes for E. Gonzales vs N. Maduro"</span>,</span>
<span id="cb19-9"><a href="#cb19-9" aria-hidden="true" tabindex="-1"></a>         <span class="at">caption =</span> <span class="st">"Based on 83% of ballots records"</span>) </span>
<span id="cb19-10"><a href="#cb19-10" aria-hidden="true" tabindex="-1"></a>venezuela_graph1</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<div>
<figure class="figure">
<p><img src="Visualizations-Sample_files/figure-html/unnamed-chunk-1-1.png" class="img-fluid figure-img" width="672"></p>
</figure>
</div>
</div>
<div class="sourceCode cell-code" id="cb20"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Your code here:</span></span>
<span id="cb20-2"><a href="#cb20-2" aria-hidden="true" tabindex="-1"></a>barinas <span class="ot">&lt;-</span> venezuela <span class="sc">|&gt;</span></span>
<span id="cb20-3"><a href="#cb20-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(EDO <span class="sc">==</span> <span class="st">"EDO. BARINAS"</span>) <span class="sc">|&gt;</span></span>
<span id="cb20-4"><a href="#cb20-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">GW =</span> <span class="fu">if_else</span>(EG<span class="sc">&gt;</span>NM, <span class="cn">TRUE</span>, <span class="cn">FALSE</span>))  <span class="sc">|&gt;</span></span>
<span id="cb20-5"><a href="#cb20-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">relocate</span>(GW, <span class="at">.before =</span> LM)</span>
<span id="cb20-6"><a href="#cb20-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-7"><a href="#cb20-7" aria-hidden="true" tabindex="-1"></a>barinas1 <span class="ot">&lt;-</span> barinas <span class="sc">|&gt;</span></span>
<span id="cb20-8"><a href="#cb20-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(GW <span class="sc">==</span> <span class="cn">TRUE</span>) </span>
<span id="cb20-9"><a href="#cb20-9" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-10"><a href="#cb20-10" aria-hidden="true" tabindex="-1"></a>centers_total <span class="ot">&lt;-</span> <span class="fu">n_distinct</span>(barinas<span class="sc">$</span>CENTRO) <span class="co">#612 voting centers in total</span></span>
<span id="cb20-11"><a href="#cb20-11" aria-hidden="true" tabindex="-1"></a>centers_won <span class="ot">&lt;-</span> <span class="fu">n_distinct</span>(barinas1<span class="sc">$</span>CENTRO) <span class="co">#546 voting centers </span></span>
<span id="cb20-12"><a href="#cb20-12" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-13"><a href="#cb20-13" aria-hidden="true" tabindex="-1"></a>gonzalez_won_barinas <span class="ot">&lt;-</span> centers_won<span class="sc">/</span>centers_total <span class="sc">*</span><span class="dv">100</span> </span>
<span id="cb20-14"><a href="#cb20-14" aria-hidden="true" tabindex="-1"></a><span class="fu">view</span>(gonzalez_won_barinas)</span>
<span id="cb20-15"><a href="#cb20-15" aria-hidden="true" tabindex="-1"></a><span class="co"># Gonzalez won in 89.2% of the voting centers in Barinas</span></span>
<span id="cb20-16"><a href="#cb20-16" aria-hidden="true" tabindex="-1"></a>venezuela_rural <span class="ot">&lt;-</span> venezuela <span class="sc">|&gt;</span></span>
<span id="cb20-17"><a href="#cb20-17" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">URBAN =</span> <span class="fu">if_else</span>(EDO <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">"DTTO. CAPITAL"</span>, <span class="st">"EDO. MIRANDA"</span>, <span class="st">"EDO. ZULIA"</span>,<span class="st">"EDO. CARABOBO"</span>, <span class="st">"EDO. LARA"</span>, <span class="st">"EDO. ANZOATEGUI"</span>, <span class="st">"EDO. ARAGUA"</span>,<span class="st">"EDO. BOLIVAR"</span>, <span class="st">"EDO. MONAGAS"</span>, <span class="st">"EDO. SUCRE"</span>, <span class="st">"EDO. MERIDA"</span>, <span class="st">"EDO. TACHIRA"</span>, <span class="st">"EDO. PORTUGUESA"</span>, <span class="st">"EDO. FALCON"</span>),</span>
<span id="cb20-18"><a href="#cb20-18" aria-hidden="true" tabindex="-1"></a>                         <span class="st">"URBAN"</span>, <span class="st">"RURAL"</span>)) <span class="sc">|&gt;</span></span>
<span id="cb20-19"><a href="#cb20-19" aria-hidden="true" tabindex="-1"></a>  <span class="fu">relocate</span>(URBAN, <span class="at">.before =</span> COD_MUN)</span>
<span id="cb20-20"><a href="#cb20-20" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-21"><a href="#cb20-21" aria-hidden="true" tabindex="-1"></a>venezuela_rural <span class="ot">&lt;-</span> venezuela_rural <span class="sc">|&gt;</span></span>
<span id="cb20-22"><a href="#cb20-22" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">Maduro_won =</span> <span class="fu">if_else</span>(NM<span class="sc">&gt;</span>EG, <span class="st">"TRUE"</span>, <span class="st">"FAlSE"</span>)) <span class="sc">|&gt;</span></span>
<span id="cb20-23"><a href="#cb20-23" aria-hidden="true" tabindex="-1"></a>  <span class="fu">relocate</span>(Maduro_won, <span class="at">.before =</span> COD_MUN)</span>
<span id="cb20-24"><a href="#cb20-24" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-25"><a href="#cb20-25" aria-hidden="true" tabindex="-1"></a>venezuela_rural <span class="ot">&lt;-</span> venezuela_rural <span class="sc">|&gt;</span></span>
<span id="cb20-26"><a href="#cb20-26" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(URBAN <span class="sc">==</span> <span class="st">"RURAL"</span>)</span>
<span id="cb20-27"><a href="#cb20-27" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb20-28"><a href="#cb20-28" aria-hidden="true" tabindex="-1"></a><span class="fu">n_distinct</span>(venezuela_rural<span class="sc">$</span>EDO) <span class="co">#There are 10 rural states in the data set</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 10</code></pre>
</div>
<div class="sourceCode cell-code" id="cb22"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb22-1"><a href="#cb22-1" aria-hidden="true" tabindex="-1"></a>venezuela_rural_only <span class="ot">&lt;-</span> venezuela_rural <span class="sc">|&gt;</span></span>
<span id="cb22-2"><a href="#cb22-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarize</span>(</span>
<span id="cb22-3"><a href="#cb22-3" aria-hidden="true" tabindex="-1"></a>    <span class="at">n_rows =</span> <span class="fu">n</span>(),</span>
<span id="cb22-4"><a href="#cb22-4" aria-hidden="true" tabindex="-1"></a>    <span class="at">maduro_rural =</span> <span class="fu">sum</span>(Maduro_won <span class="sc">==</span> <span class="st">"TRUE"</span>, <span class="at">na.rm =</span> <span class="cn">TRUE</span>),</span>
<span id="cb22-5"><a href="#cb22-5" aria-hidden="true" tabindex="-1"></a>    <span class="at">maduro_votes_rural =</span> <span class="fu">n</span>()<span class="sc">/</span><span class="fu">sum</span>(Maduro_won <span class="sc">==</span> <span class="st">"TRUE"</span>, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)</span>
<span id="cb22-6"><a href="#cb22-6" aria-hidden="true" tabindex="-1"></a>    )</span>
<span id="cb22-7"><a href="#cb22-7" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb22-8"><a href="#cb22-8" aria-hidden="true" tabindex="-1"></a><span class="co"># There are 5394 parishes in the rural states and Maduro won in 892 of them, which brings his victory rate to a rough approximnate of 6.04%</span></span>
<span id="cb22-9"><a href="#cb22-9" aria-hidden="true" tabindex="-1"></a>  </span>
<span id="cb22-10"><a href="#cb22-10" aria-hidden="true" tabindex="-1"></a><span class="co"># Your code here:</span></span>
<span id="cb22-11"><a href="#cb22-11" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb22-12"><a href="#cb22-12" aria-hidden="true" tabindex="-1"></a>N <span class="ot">&lt;-</span> <span class="dv">10058774</span></span>
<span id="cb22-13"><a href="#cb22-13" aria-hidden="true" tabindex="-1"></a>S <span class="ot">&lt;-</span> <span class="fl">1e8</span></span>
<span id="cb22-14"><a href="#cb22-14" aria-hidden="true" tabindex="-1"></a>A <span class="ot">&lt;-</span> <span class="fu">round</span>(N<span class="sc">*</span><span class="fu">runif</span>(S, <span class="fl">0.30</span>, <span class="fl">0.70</span>))</span>
<span id="cb22-15"><a href="#cb22-15" aria-hidden="true" tabindex="-1"></a>C <span class="ot">&lt;-</span> <span class="fu">round</span>(N<span class="sc">*</span><span class="fu">runif</span>(S, <span class="fl">0.01</span>, <span class="fl">0.10</span>))</span>
<span id="cb22-16"><a href="#cb22-16" aria-hidden="true" tabindex="-1"></a>B <span class="ot">&lt;-</span> N <span class="sc">-</span> A <span class="sc">-</span> C</span>
<span id="cb22-17"><a href="#cb22-17" aria-hidden="true" tabindex="-1"></a>A_round <span class="ot">&lt;-</span> <span class="fu">round</span>(<span class="fu">round</span>(A<span class="sc">/</span>N, <span class="dv">3</span>)<span class="sc">*</span>N)</span>
<span id="cb22-18"><a href="#cb22-18" aria-hidden="true" tabindex="-1"></a>B_round <span class="ot">&lt;-</span> <span class="fu">round</span>(<span class="fu">round</span>(B<span class="sc">/</span>N, <span class="dv">3</span>)<span class="sc">*</span>N)</span>
<span id="cb22-19"><a href="#cb22-19" aria-hidden="true" tabindex="-1"></a>C_round <span class="ot">&lt;-</span> <span class="fu">round</span>(<span class="fu">round</span>(C<span class="sc">/</span>N, <span class="dv">3</span>)<span class="sc">*</span>N)</span>
<span id="cb22-20"><a href="#cb22-20" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(A_round<span class="sc">==</span>A <span class="sc">&amp;</span> B_round<span class="sc">==</span>B <span class="sc">&amp;</span> C_round<span class="sc">==</span>C)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0</code></pre>
</div>
</div>
<p>Sample 2</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb24"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb24-1"><a href="#cb24-1" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="at">echo =</span> <span class="cn">TRUE</span>)</span>
<span id="cb24-2"><a href="#cb24-2" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="fu">options</span>(<span class="at">width =</span> <span class="dv">60</span>))</span>
<span id="cb24-3"><a href="#cb24-3" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="at">class.output =</span> <span class="st">"bg-warning"</span>)</span>
<span id="cb24-4"><a href="#cb24-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb24-5"><a href="#cb24-5" aria-hidden="true" tabindex="-1"></a>packages <span class="ot">&lt;-</span> <span class="fu">c</span>(<span class="st">'haven'</span>,<span class="st">'dplyr'</span>, <span class="st">'ggplot2'</span>, <span class="st">'reshape2'</span>, <span class="st">'tidyverse'</span>, <span class="st">'pracma'</span>,</span>
<span id="cb24-6"><a href="#cb24-6" aria-hidden="true" tabindex="-1"></a>              <span class="st">'lubridate'</span>, <span class="st">'scales'</span>, <span class="st">'ggthemes'</span>, <span class="st">'gt'</span>, <span class="st">'dineq'</span>, <span class="st">'gglorenz'</span>)  </span>
<span id="cb24-7"><a href="#cb24-7" aria-hidden="true" tabindex="-1"></a>to_install <span class="ot">&lt;-</span> packages[<span class="sc">!</span>(packages <span class="sc">%in%</span> <span class="fu">installed.packages</span>()[,<span class="st">"Package"</span>])]</span>
<span id="cb24-8"><a href="#cb24-8" aria-hidden="true" tabindex="-1"></a><span class="cf">if</span>(<span class="fu">length</span>(to_install)<span class="sc">&gt;</span><span class="dv">0</span>) <span class="fu">install.packages</span>(to_install, </span>
<span id="cb24-9"><a href="#cb24-9" aria-hidden="true" tabindex="-1"></a>                                          <span class="at">repos=</span><span class="st">'http://cran.us.r-project.org'</span>)</span>
<span id="cb24-10"><a href="#cb24-10" aria-hidden="true" tabindex="-1"></a><span class="fu">lapply</span>(packages, require, <span class="at">character.only=</span><span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: haven</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: reshape2</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'reshape2'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following object is masked from 'package:tidyr':

    smiths</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: pracma</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'pracma'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following object is masked from 'package:purrr':

    cross</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: scales</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'scales'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following object is masked from 'package:purrr':

    discard</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following object is masked from 'package:readr':

    col_factor</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: ggthemes</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: gt</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: dineq</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: gglorenz</code></pre>
</div>
<div class="cell-output cell-output-stdout">
<pre><code>[[1]]
[1] TRUE

[[2]]
[1] TRUE

[[3]]
[1] TRUE

[[4]]
[1] TRUE

[[5]]
[1] TRUE

[[6]]
[1] TRUE

[[7]]
[1] TRUE

[[8]]
[1] TRUE

[[9]]
[1] TRUE

[[10]]
[1] TRUE

[[11]]
[1] TRUE

[[12]]
[1] TRUE</code></pre>
</div>
<div class="sourceCode cell-code" id="cb41"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb41-1"><a href="#cb41-1" aria-hidden="true" tabindex="-1"></a><span class="co">#Import data </span></span>
<span id="cb41-2"><a href="#cb41-2" aria-hidden="true" tabindex="-1"></a>url <span class="ot">&lt;-</span> <span class="st">"https://www.dropbox.com/scl/fi/8rdnb313lfha0c0vxyy1r/taiwan_election_2024_pollingstation.csv?rlkey=okgvk39f7ymjkt7hk0taoqieh&amp;st=ybleflc6&amp;dl=1"</span></span>
<span id="cb41-3"><a href="#cb41-3" aria-hidden="true" tabindex="-1"></a>tmp <span class="ot">&lt;-</span> <span class="fu">tempfile</span>(<span class="at">fileext =</span> <span class="st">".csv"</span>)</span>
<span id="cb41-4"><a href="#cb41-4" aria-hidden="true" tabindex="-1"></a><span class="fu">download.file</span>(url, tmp, <span class="at">mode =</span> <span class="st">"wb"</span>)</span>
<span id="cb41-5"><a href="#cb41-5" aria-hidden="true" tabindex="-1"></a>tai <span class="ot">&lt;-</span> <span class="fu">read.csv</span>(tmp)</span>
<span id="cb41-6"><a href="#cb41-6" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(readr)</span>
<span id="cb41-7"><a href="#cb41-7" aria-hidden="true" tabindex="-1"></a>taiwan_election_2024_pollingstation <span class="ot">&lt;-</span> <span class="fu">read_csv</span>(<span class="st">"/Users/leilasagymbayeva/Desktop/1 Semester/API 209//Problem Sets/PSet 2/3 - to post ps2/taiwan_election_2024_pollingstation.csv"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Rows: 17795 Columns: 19</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>── Column specification ────────────────────────────────────
Delimiter: ","
chr  (7): county_en, township_en, village_en, county, to...
dbl (12): county_num, votes_tpp_ko_wu, votes_dpp_lai_hsi...

ℹ Use `spec()` to retrieve the full column specification for this data.
ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.</code></pre>
</div>
<div class="sourceCode cell-code" id="cb44"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb44-1"><a href="#cb44-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb44-2"><a href="#cb44-2" aria-hidden="true" tabindex="-1"></a><span class="co">#a Proportion of votes won</span></span>
<span id="cb44-3"><a href="#cb44-3" aria-hidden="true" tabindex="-1"></a>  p_DPP <span class="ot">&lt;-</span> <span class="fu">sum</span>(taiwan_election_2024_pollingstation<span class="sc">$</span>votes_dpp_lai_hsiao)<span class="sc">/</span><span class="fu">sum</span>(taiwan_election_2024_pollingstation<span class="sc">$</span>valid_votes)</span>
<span id="cb44-4"><a href="#cb44-4" aria-hidden="true" tabindex="-1"></a><span class="co">#b Standard deviation of proportion of votes won across polling stations</span></span>
<span id="cb44-5"><a href="#cb44-5" aria-hidden="true" tabindex="-1"></a>station_share <span class="ot">&lt;-</span> <span class="dv">100</span><span class="sc">*</span>(taiwan_election_2024_pollingstation<span class="sc">$</span>votes_dpp_lai_hsiao<span class="sc">/</span>taiwan_election_2024_pollingstation<span class="sc">$</span>valid_votes)</span>
<span id="cb44-6"><a href="#cb44-6" aria-hidden="true" tabindex="-1"></a>sd_DPP_pop <span class="ot">&lt;-</span> <span class="fu">sd</span>(station_share)</span>
<span id="cb44-7"><a href="#cb44-7" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb44-8"><a href="#cb44-8" aria-hidden="true" tabindex="-1"></a><span class="co"># For the question b I used AI to help me understand the difference of standard deviation across individual votes and across polling stations. I initially used the formula sqrt(p*(1-p)), but that gave me a value inconsistent with sampling SD calculated in subsequent questions.</span></span>
<span id="cb44-9"><a href="#cb44-9" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb44-10"><a href="#cb44-10" aria-hidden="true" tabindex="-1"></a><span class="co">#2</span></span>
<span id="cb44-11"><a href="#cb44-11" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">1996</span>)</span>
<span id="cb44-12"><a href="#cb44-12" aria-hidden="true" tabindex="-1"></a>sample5 <span class="ot">&lt;-</span> <span class="fu">slice_sample</span>(taiwan_election_2024_pollingstation, <span class="at">n=</span><span class="dv">5</span>)</span>
<span id="cb44-13"><a href="#cb44-13" aria-hidden="true" tabindex="-1"></a><span class="co">#a</span></span>
<span id="cb44-14"><a href="#cb44-14" aria-hidden="true" tabindex="-1"></a><span class="fu">choose</span>(<span class="dv">17795</span>,<span class="dv">5</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 1.486157e+19</code></pre>
</div>
<div class="sourceCode cell-code" id="cb46"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb46-1"><a href="#cb46-1" aria-hidden="true" tabindex="-1"></a><span class="co">#b</span></span>
<span id="cb46-2"><a href="#cb46-2" aria-hidden="true" tabindex="-1"></a>p_DPP_sample5 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample5<span class="sc">$</span>votes_dpp_lai_hsiao)<span class="sc">/</span><span class="fu">sum</span>(sample5<span class="sc">$</span>valid_votes) <span class="co"># 0.43</span></span>
<span id="cb46-3"><a href="#cb46-3" aria-hidden="true" tabindex="-1"></a><span class="co">#c</span></span>
<span id="cb46-4"><a href="#cb46-4" aria-hidden="true" tabindex="-1"></a>p_TPP_sample5 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample5<span class="sc">$</span>votes_tpp_ko_wu)<span class="sc">/</span><span class="fu">sum</span>(sample5<span class="sc">$</span>valid_votes) <span class="co"># 0.24</span></span>
<span id="cb46-5"><a href="#cb46-5" aria-hidden="true" tabindex="-1"></a>p_KMT_sample5 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample5<span class="sc">$</span>votes_kmt_hou_jaw)<span class="sc">/</span><span class="fu">sum</span>(sample5<span class="sc">$</span>valid_votes) <span class="co"># 0.33</span></span>
<span id="cb46-6"><a href="#cb46-6" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb46-7"><a href="#cb46-7" aria-hidden="true" tabindex="-1"></a><span class="co">#3</span></span>
<span id="cb46-8"><a href="#cb46-8" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">1996</span>)</span>
<span id="cb46-9"><a href="#cb46-9" aria-hidden="true" tabindex="-1"></a>sample100 <span class="ot">&lt;-</span> <span class="fu">slice_sample</span>(taiwan_election_2024_pollingstation, <span class="at">n=</span><span class="dv">100</span>)</span>
<span id="cb46-10"><a href="#cb46-10" aria-hidden="true" tabindex="-1"></a><span class="co">#a</span></span>
<span id="cb46-11"><a href="#cb46-11" aria-hidden="true" tabindex="-1"></a><span class="fu">choose</span>(<span class="dv">17795</span>,<span class="dv">100</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 8.684863e+266</code></pre>
</div>
<div class="sourceCode cell-code" id="cb48"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb48-1"><a href="#cb48-1" aria-hidden="true" tabindex="-1"></a><span class="co">#b</span></span>
<span id="cb48-2"><a href="#cb48-2" aria-hidden="true" tabindex="-1"></a>p_DPP_sample100 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample100<span class="sc">$</span>votes_dpp_lai_hsiao)<span class="sc">/</span><span class="fu">sum</span>(sample100<span class="sc">$</span>valid_votes) <span class="co"># 0.39</span></span>
<span id="cb48-3"><a href="#cb48-3" aria-hidden="true" tabindex="-1"></a><span class="co">#c</span></span>
<span id="cb48-4"><a href="#cb48-4" aria-hidden="true" tabindex="-1"></a>p_TPP_sample100 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample100<span class="sc">$</span>votes_tpp_ko_wu)<span class="sc">/</span><span class="fu">sum</span>(sample100<span class="sc">$</span>valid_votes) <span class="co"># 0.26</span></span>
<span id="cb48-5"><a href="#cb48-5" aria-hidden="true" tabindex="-1"></a>p_KMT_sample100 <span class="ot">&lt;-</span> <span class="fu">sum</span>(sample100<span class="sc">$</span>votes_kmt_hou_jaw)<span class="sc">/</span><span class="fu">sum</span>(sample100<span class="sc">$</span>valid_votes) <span class="co"># 0.34</span></span>
<span id="cb48-6"><a href="#cb48-6" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb48-7"><a href="#cb48-7" aria-hidden="true" tabindex="-1"></a>p_DPP <span class="sc">-</span> p_DPP_sample5 <span class="co"># sample estimate deviates by 0.031</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] -0.03122645</code></pre>
</div>
<div class="sourceCode cell-code" id="cb50"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb50-1"><a href="#cb50-1" aria-hidden="true" tabindex="-1"></a>p_DPP <span class="sc">-</span> p_DPP_sample100 <span class="co"># sample estimate deviates by 0.006</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0.006350364</code></pre>
</div>
<div class="sourceCode cell-code" id="cb52"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb52-1"><a href="#cb52-1" aria-hidden="true" tabindex="-1"></a><span class="co">#For-loop code </span></span>
<span id="cb52-2"><a href="#cb52-2" aria-hidden="true" tabindex="-1"></a>xbar_5 <span class="ot">&lt;-</span> <span class="fu">c</span>() </span>
<span id="cb52-3"><a href="#cb52-3" aria-hidden="true" tabindex="-1"></a>win_5 <span class="ot">&lt;-</span> <span class="fu">c</span>()</span>
<span id="cb52-4"><a href="#cb52-4" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)</span>
<span id="cb52-5"><a href="#cb52-5" aria-hidden="true" tabindex="-1"></a><span class="cf">for</span> (i <span class="cf">in</span> <span class="dv">1</span><span class="sc">:</span><span class="dv">1000</span>) {</span>
<span id="cb52-6"><a href="#cb52-6" aria-hidden="true" tabindex="-1"></a>  samp_5 <span class="ot">&lt;-</span> <span class="fu">slice_sample</span>(taiwan_election_2024_pollingstation, <span class="at">n =</span> <span class="dv">5</span>) </span>
<span id="cb52-7"><a href="#cb52-7" aria-hidden="true" tabindex="-1"></a>  xbar_5[i] <span class="ot">&lt;-</span> <span class="dv">100</span><span class="sc">*</span>(<span class="fu">sum</span>(samp_5<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">/</span> <span class="fu">sum</span>(samp_5<span class="sc">$</span>valid_votes))</span>
<span id="cb52-8"><a href="#cb52-8" aria-hidden="true" tabindex="-1"></a>  win_5[i] <span class="ot">&lt;-</span> (<span class="fu">sum</span>(samp_5<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">&gt;</span> <span class="fu">sum</span>(samp_5<span class="sc">$</span>votes_tpp_ko_wu) <span class="sc">&amp;</span></span>
<span id="cb52-9"><a href="#cb52-9" aria-hidden="true" tabindex="-1"></a>               <span class="fu">sum</span>(samp_5<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">&gt;</span> <span class="fu">sum</span>(samp_5<span class="sc">$</span>votes_kmt_hou_jaw))</span>
<span id="cb52-10"><a href="#cb52-10" aria-hidden="true" tabindex="-1"></a>}</span>
<span id="cb52-11"><a href="#cb52-11" aria-hidden="true" tabindex="-1"></a><span class="fu">mean</span>(xbar_5) <span class="co">#average vote share of DPP in 100 samples of 5</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 39.92888</code></pre>
</div>
<div class="sourceCode cell-code" id="cb54"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb54-1"><a href="#cb54-1" aria-hidden="true" tabindex="-1"></a><span class="fu">sd</span>(xbar_5) <span class="co">#standard deviation of DPP vote share in 1000 samples of size 5 = 4.147%</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 4.147062</code></pre>
</div>
<div class="sourceCode cell-code" id="cb56"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb56-1"><a href="#cb56-1" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(win_5 <span class="sc">==</span> <span class="st">"FALSE"</span>) <span class="co"># Lai Ching-te lost 185 times out of 1000 times/samples.</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 185</code></pre>
</div>
<div class="sourceCode cell-code" id="cb58"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb58-1"><a href="#cb58-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb58-2"><a href="#cb58-2" aria-hidden="true" tabindex="-1"></a>xbar_100 <span class="ot">&lt;-</span> <span class="fu">c</span>() </span>
<span id="cb58-3"><a href="#cb58-3" aria-hidden="true" tabindex="-1"></a>win_100 <span class="ot">&lt;-</span> <span class="fu">c</span>()</span>
<span id="cb58-4"><a href="#cb58-4" aria-hidden="true" tabindex="-1"></a><span class="fu">set.seed</span>(<span class="dv">123</span>)</span>
<span id="cb58-5"><a href="#cb58-5" aria-hidden="true" tabindex="-1"></a><span class="cf">for</span> (i <span class="cf">in</span> <span class="dv">1</span><span class="sc">:</span><span class="dv">1000</span>) {</span>
<span id="cb58-6"><a href="#cb58-6" aria-hidden="true" tabindex="-1"></a>  samp_100 <span class="ot">&lt;-</span> <span class="fu">slice_sample</span>(taiwan_election_2024_pollingstation, <span class="at">n =</span> <span class="dv">100</span>) </span>
<span id="cb58-7"><a href="#cb58-7" aria-hidden="true" tabindex="-1"></a>  xbar_100[i] <span class="ot">&lt;-</span> <span class="dv">100</span><span class="sc">*</span>(<span class="fu">sum</span>(samp_100<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">/</span> <span class="fu">sum</span>(samp_100<span class="sc">$</span>valid_votes))</span>
<span id="cb58-8"><a href="#cb58-8" aria-hidden="true" tabindex="-1"></a>  win_100[i] <span class="ot">&lt;-</span> (<span class="fu">sum</span>(samp_100<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">&gt;</span> <span class="fu">sum</span>(samp_100<span class="sc">$</span>votes_tpp_ko_wu) <span class="sc">&amp;</span></span>
<span id="cb58-9"><a href="#cb58-9" aria-hidden="true" tabindex="-1"></a>               <span class="fu">sum</span>(samp_100<span class="sc">$</span>votes_dpp_lai_hsiao) <span class="sc">&gt;</span> <span class="fu">sum</span>(samp_100<span class="sc">$</span>votes_kmt_hou_jaw))</span>
<span id="cb58-10"><a href="#cb58-10" aria-hidden="true" tabindex="-1"></a>}</span>
<span id="cb58-11"><a href="#cb58-11" aria-hidden="true" tabindex="-1"></a>mu100 <span class="ot">&lt;-</span> <span class="fu">mean</span>(xbar_100) <span class="co">#average vote share of DPP in 1000 samples of 100 = 40.0503%</span></span>
<span id="cb58-12"><a href="#cb58-12" aria-hidden="true" tabindex="-1"></a>xbar_100 <span class="ot">&lt;-</span> <span class="fu">unlist</span>(xbar_100, <span class="at">use.names =</span> <span class="cn">FALSE</span>)</span>
<span id="cb58-13"><a href="#cb58-13" aria-hidden="true" tabindex="-1"></a><span class="fu">sd</span>(xbar_100) <span class="co">#standard deviation of DPP vote share in 1000 samples of size 100 = 0.9323102</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0.9323102</code></pre>
</div>
<div class="sourceCode cell-code" id="cb60"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb60-1"><a href="#cb60-1" aria-hidden="true" tabindex="-1"></a>se100 <span class="ot">&lt;-</span> <span class="fu">sd</span>(xbar_100, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)</span>
<span id="cb60-2"><a href="#cb60-2" aria-hidden="true" tabindex="-1"></a><span class="fu">sum</span>(win_100 <span class="sc">==</span> <span class="st">"FALSE"</span>) <span class="co"># Lai Ching-te lost 0 times out of 1000 times/samples.</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0</code></pre>
</div>
<div class="sourceCode cell-code" id="cb62"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb62-1"><a href="#cb62-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb62-2"><a href="#cb62-2" aria-hidden="true" tabindex="-1"></a>xbar_5 <span class="ot">&lt;-</span> <span class="fu">tibble</span>(<span class="at">val =</span> xbar_5) <span class="co"># histogram in ggplot would not produce a histogram from a vector, only from a data ftrame or a tibble</span></span>
<span id="cb62-3"><a href="#cb62-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb62-4"><a href="#cb62-4" aria-hidden="true" tabindex="-1"></a>xbar_5 <span class="sc">%&gt;%</span> </span>
<span id="cb62-5"><a href="#cb62-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> val, <span class="at">y =</span> <span class="fu">stat</span>(width<span class="sc">*</span>density))) <span class="sc">+</span></span>
<span id="cb62-6"><a href="#cb62-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_histogram</span>(<span class="at">color =</span> <span class="st">"white"</span>, <span class="at">bins =</span> <span class="dv">30</span>) <span class="sc">+</span></span>
<span id="cb62-7"><a href="#cb62-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x =</span> <span class="st">"DPP Vote Share Proportion Estimates"</span>,</span>
<span id="cb62-8"><a href="#cb62-8" aria-hidden="true" tabindex="-1"></a>       <span class="at">y =</span> <span class="st">"Proportion"</span>) <span class="sc">+</span></span>
<span id="cb62-9"><a href="#cb62-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_y_continuous</span>(<span class="at">labels =</span> percent) <span class="sc">+</span> </span>
<span id="cb62-10"><a href="#cb62-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_clean</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Warning: `stat(width * density)` was deprecated in ggplot2 3.4.0.
ℹ Please use `after_stat(width * density)` instead.</code></pre>
</div>
<div class="cell-output-display">
<div>
<figure class="figure">
<p><img src="Visualizations-Sample_files/figure-html/unnamed-chunk-2-1.png" class="img-fluid figure-img" width="672"></p>
</figure>
</div>
</div>
<div class="sourceCode cell-code" id="cb64"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb64-1"><a href="#cb64-1" aria-hidden="true" tabindex="-1"></a>xbar_100 <span class="ot">&lt;-</span> <span class="fu">tibble</span>(<span class="at">val =</span> xbar_100) </span>
<span id="cb64-2"><a href="#cb64-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb64-3"><a href="#cb64-3" aria-hidden="true" tabindex="-1"></a>xbar_100 <span class="sc">%&gt;%</span> </span>
<span id="cb64-4"><a href="#cb64-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>(<span class="fu">aes</span>(<span class="at">x =</span> val, <span class="at">y =</span> <span class="fu">stat</span>(width<span class="sc">*</span>density))) <span class="sc">+</span></span>
<span id="cb64-5"><a href="#cb64-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_histogram</span>(<span class="at">color =</span> <span class="st">"white"</span>, <span class="at">bins =</span> <span class="dv">30</span>) <span class="sc">+</span></span>
<span id="cb64-6"><a href="#cb64-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x =</span> <span class="st">"DPP Vote Share Proportion Estimates"</span>,</span>
<span id="cb64-7"><a href="#cb64-7" aria-hidden="true" tabindex="-1"></a>       <span class="at">y =</span> <span class="st">"Proportion"</span>) <span class="sc">+</span></span>
<span id="cb64-8"><a href="#cb64-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_y_continuous</span>(<span class="at">labels =</span> percent) <span class="sc">+</span> </span>
<span id="cb64-9"><a href="#cb64-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_clean</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<div>
<figure class="figure">
<p><img src="Visualizations-Sample_files/figure-html/unnamed-chunk-2-2.png" class="img-fluid figure-img" width="672"></p>
</figure>
</div>
</div>
<div class="sourceCode cell-code" id="cb65"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb65-1"><a href="#cb65-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb65-2"><a href="#cb65-2" aria-hidden="true" tabindex="-1"></a>xbar_100 <span class="ot">&lt;-</span> <span class="fu">unlist</span>(xbar_100)</span>
<span id="cb65-3"><a href="#cb65-3" aria-hidden="true" tabindex="-1"></a>x_lb <span class="ot">&lt;-</span> xbar_100 <span class="sc">-</span> <span class="fl">1.64</span><span class="sc">*</span>se100        </span>
<span id="cb65-4"><a href="#cb65-4" aria-hidden="true" tabindex="-1"></a>x_ub <span class="ot">&lt;-</span> xbar_100 <span class="sc">+</span> <span class="fl">1.64</span><span class="sc">*</span>se100        </span>
<span id="cb65-5"><a href="#cb65-5" aria-hidden="true" tabindex="-1"></a>samp_ci <span class="ot">&lt;-</span> <span class="fu">tibble</span>(x_lb, x_ub)</span>
<span id="cb65-6"><a href="#cb65-6" aria-hidden="true" tabindex="-1"></a>samp_ci <span class="ot">&lt;-</span> samp_ci <span class="sc">|&gt;</span></span>
<span id="cb65-7"><a href="#cb65-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">true_p =</span> <span class="fu">if_else</span>(x_lb<span class="sc">&lt;=</span><span class="dv">40</span> <span class="sc">&amp;</span> x_ub<span class="sc">&gt;=</span><span class="dv">40</span>, <span class="cn">TRUE</span>, <span class="cn">FALSE</span>))</span>
<span id="cb65-8"><a href="#cb65-8" aria-hidden="true" tabindex="-1"></a>true_n <span class="ot">&lt;-</span> <span class="fu">filter</span>(samp_ci, true_p <span class="sc">==</span> <span class="st">"TRUE"</span>)</span>
<span id="cb65-9"><a href="#cb65-9" aria-hidden="true" tabindex="-1"></a><span class="fu">nrow</span>(true_n) </span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 891</code></pre>
</div>
<div class="sourceCode cell-code" id="cb67"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb67-1"><a href="#cb67-1" aria-hidden="true" tabindex="-1"></a><span class="fu">class</span>(xbar_100)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] "numeric"</code></pre>
</div>
<div class="sourceCode cell-code" id="cb69"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb69-1"><a href="#cb69-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Feel free to calculate by R or hand</span></span>
<span id="cb69-2"><a href="#cb69-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb69-3"><a href="#cb69-3" aria-hidden="true" tabindex="-1"></a><span class="co">#H_o: proportion of 7 being the last digit is equal to 10%</span></span>
<span id="cb69-4"><a href="#cb69-4" aria-hidden="true" tabindex="-1"></a><span class="co"># Estimate = 17.24%</span></span>
<span id="cb69-5"><a href="#cb69-5" aria-hidden="true" tabindex="-1"></a><span class="co"># Shape: approx. normal</span></span>
<span id="cb69-6"><a href="#cb69-6" aria-hidden="true" tabindex="-1"></a><span class="co"># Mean: p = 0.10</span></span>
<span id="cb69-7"><a href="#cb69-7" aria-hidden="true" tabindex="-1"></a><span class="co"># Standard deviation = 0.0278543</span></span>
<span id="cb69-8"><a href="#cb69-8" aria-hidden="true" tabindex="-1"></a>sd <span class="ot">&lt;-</span> <span class="fu">sqrt</span>((<span class="fl">0.10</span><span class="sc">*</span><span class="fl">0.90</span>)<span class="sc">/</span><span class="dv">116</span>)</span>
<span id="cb69-9"><a href="#cb69-9" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb69-10"><a href="#cb69-10" aria-hidden="true" tabindex="-1"></a><span class="co"># (1) Method of the estimator sampling distribution</span></span>
<span id="cb69-11"><a href="#cb69-11" aria-hidden="true" tabindex="-1"></a>p_sample <span class="ot">&lt;-</span> <span class="fl">0.1724</span></span>
<span id="cb69-12"><a href="#cb69-12" aria-hidden="true" tabindex="-1"></a>p_norm <span class="ot">&lt;-</span> <span class="fu">pnorm</span>(<span class="fl">0.0276</span>, <span class="fl">0.10</span>, sd)</span>
<span id="cb69-13"><a href="#cb69-13" aria-hidden="true" tabindex="-1"></a>p_value <span class="ot">&lt;-</span> <span class="dv">2</span><span class="sc">*</span>p_norm</span>
<span id="cb69-14"><a href="#cb69-14" aria-hidden="true" tabindex="-1"></a><span class="fu">print</span>(p_value)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 0.009343055</code></pre>
</div>
<div class="sourceCode cell-code" id="cb71"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb71-1"><a href="#cb71-1" aria-hidden="true" tabindex="-1"></a><span class="co"># P-value is equal to 0.00934, which is less than 0.05 and 0.01, so we can reject the null hypothesis both at 5% and 1% alpha.</span></span>
<span id="cb71-2"><a href="#cb71-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb71-3"><a href="#cb71-3" aria-hidden="true" tabindex="-1"></a><span class="co"># (2) Method using the Test Statistic</span></span>
<span id="cb71-4"><a href="#cb71-4" aria-hidden="true" tabindex="-1"></a>z <span class="ot">&lt;-</span> (p_sample <span class="sc">-</span> <span class="fl">0.10</span>)<span class="sc">/</span>sd</span>
<span id="cb71-5"><a href="#cb71-5" aria-hidden="true" tabindex="-1"></a><span class="fu">print</span>(z)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 2.59924</code></pre>
</div>
<div class="sourceCode cell-code" id="cb73"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb73-1"><a href="#cb73-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Test Statistic is equal to 2.599 which is greater than 1.96 and 2.58. Therefore, we can reject the null hypothesis at both 95% and 99% confidence levels.</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>Sample 3</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb74"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb74-1"><a href="#cb74-1" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="at">echo =</span> <span class="cn">TRUE</span>)</span>
<span id="cb74-2"><a href="#cb74-2" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="fu">options</span>(<span class="at">width =</span> <span class="dv">60</span>))</span>
<span id="cb74-3"><a href="#cb74-3" aria-hidden="true" tabindex="-1"></a>knitr<span class="sc">::</span>opts_chunk<span class="sc">$</span><span class="fu">set</span>(<span class="at">class.output =</span> <span class="st">"bg-warning"</span>)</span>
<span id="cb74-4"><a href="#cb74-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb74-5"><a href="#cb74-5" aria-hidden="true" tabindex="-1"></a>packages <span class="ot">&lt;-</span> <span class="fu">c</span>(<span class="st">'haven'</span>,<span class="st">'dplyr'</span>, <span class="st">'ggplot2'</span>, <span class="st">'reshape2'</span>, <span class="st">'tidyverse'</span>, <span class="st">'pracma'</span>,</span>
<span id="cb74-6"><a href="#cb74-6" aria-hidden="true" tabindex="-1"></a>              <span class="st">'lubridate'</span>, <span class="st">'scales'</span>, <span class="st">'ggthemes'</span>, <span class="st">'gt'</span>, <span class="st">'dineq'</span>, <span class="st">'gglorenz'</span>)  </span>
<span id="cb74-7"><a href="#cb74-7" aria-hidden="true" tabindex="-1"></a>to_install <span class="ot">&lt;-</span> packages[<span class="sc">!</span>(packages <span class="sc">%in%</span> <span class="fu">installed.packages</span>()[,<span class="st">"Package"</span>])]</span>
<span id="cb74-8"><a href="#cb74-8" aria-hidden="true" tabindex="-1"></a><span class="cf">if</span>(<span class="fu">length</span>(to_install)<span class="sc">&gt;</span><span class="dv">0</span>) <span class="fu">install.packages</span>(to_install, </span>
<span id="cb74-9"><a href="#cb74-9" aria-hidden="true" tabindex="-1"></a>                                          <span class="at">repos=</span><span class="st">'http://cran.us.r-project.org'</span>)</span>
<span id="cb74-10"><a href="#cb74-10" aria-hidden="true" tabindex="-1"></a><span class="fu">lapply</span>(packages, require, <span class="at">character.only=</span><span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>[[1]]
[1] TRUE

[[2]]
[1] TRUE

[[3]]
[1] TRUE

[[4]]
[1] TRUE

[[5]]
[1] TRUE

[[6]]
[1] TRUE

[[7]]
[1] TRUE

[[8]]
[1] TRUE

[[9]]
[1] TRUE

[[10]]
[1] TRUE

[[11]]
[1] TRUE

[[12]]
[1] TRUE</code></pre>
</div>
<div class="sourceCode cell-code" id="cb76"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb76-1"><a href="#cb76-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Enter only code here. No need to print out the table</span></span>
<span id="cb76-2"><a href="#cb76-2" aria-hidden="true" tabindex="-1"></a>palms_clean <span class="ot">&lt;-</span> <span class="fu">read_csv</span>(<span class="st">"/Users/leilasagymbayeva/Desktop/1 Semester/API 209//Problem Sets/PSet 3/palms_clean.csv"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Rows: 191020 Columns: 7
── Column specification ────────────────────────────────────
Delimiter: ","
dbl (7): year, popgroup, gender, age, empstat1, yrseduc,...

ℹ Use `spec()` to retrieve the full column specification for this data.
ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.</code></pre>
</div>
<div class="sourceCode cell-code" id="cb78"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb78-1"><a href="#cb78-1" aria-hidden="true" tabindex="-1"></a>palms_clean <span class="ot">&lt;-</span> palms_clean <span class="sc">|&gt;</span> </span>
<span id="cb78-2"><a href="#cb78-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(</span>
<span id="cb78-3"><a href="#cb78-3" aria-hidden="true" tabindex="-1"></a>    <span class="at">gender =</span> <span class="fu">factor</span>(gender, <span class="at">levels =</span> <span class="fu">c</span>(<span class="dv">1</span>, <span class="dv">2</span>, <span class="dv">9</span>), <span class="at">labels =</span> <span class="fu">c</span>(<span class="st">"Male"</span>, <span class="st">"Female"</span>, <span class="st">"Unspecified"</span>)),</span>
<span id="cb78-4"><a href="#cb78-4" aria-hidden="true" tabindex="-1"></a>    <span class="at">popgroup =</span> <span class="fu">factor</span>(popgroup, <span class="at">levels =</span> <span class="fu">c</span>(<span class="dv">1</span>, <span class="dv">2</span>, <span class="dv">3</span>, <span class="dv">4</span>, <span class="dv">5</span>,<span class="dv">9</span>), <span class="at">labels =</span> <span class="fu">c</span>(<span class="st">"African/Black"</span>, <span class="st">"Coloured"</span>, <span class="st">"Indian/Asian"</span>, <span class="st">"White"</span>, <span class="st">"Other"</span>, <span class="st">"Unspecified"</span>)),</span>
<span id="cb78-5"><a href="#cb78-5" aria-hidden="true" tabindex="-1"></a>    <span class="at">empstat1 =</span> <span class="fu">factor</span>(empstat1, <span class="at">levels =</span> <span class="fu">c</span>(<span class="dv">1</span>, <span class="dv">2</span>, <span class="dv">0</span>), <span class="at">labels =</span> <span class="fu">c</span>(<span class="st">"employed"</span>, <span class="st">"unemployed"</span>, <span class="st">"not economically active"</span>))</span>
<span id="cb78-6"><a href="#cb78-6" aria-hidden="true" tabindex="-1"></a>  )</span>
<span id="cb78-7"><a href="#cb78-7" aria-hidden="true" tabindex="-1"></a>palms <span class="ot">&lt;-</span> palms_clean <span class="sc">|&gt;</span></span>
<span id="cb78-8"><a href="#cb78-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">education =</span> <span class="fu">case_when</span>(</span>
<span id="cb78-9"><a href="#cb78-9" aria-hidden="true" tabindex="-1"></a>    yrseduc <span class="sc">&lt;</span> <span class="dv">6</span> <span class="sc">~</span> <span class="st">"Primary"</span>,</span>
<span id="cb78-10"><a href="#cb78-10" aria-hidden="true" tabindex="-1"></a>    yrseduc <span class="sc">&gt;=</span><span class="dv">6</span> <span class="sc">&amp;</span> yrseduc <span class="sc">&lt;=</span><span class="dv">8</span> <span class="sc">~</span> <span class="st">"Lower Secondary"</span>,</span>
<span id="cb78-11"><a href="#cb78-11" aria-hidden="true" tabindex="-1"></a>    yrseduc <span class="sc">&gt;=</span><span class="dv">9</span> <span class="sc">&amp;</span> yrseduc <span class="sc">&lt;=</span><span class="dv">12</span> <span class="sc">~</span> <span class="st">"Upper Secondary"</span>,</span>
<span id="cb78-12"><a href="#cb78-12" aria-hidden="true" tabindex="-1"></a>    yrseduc <span class="sc">&gt;</span> <span class="dv">12</span> <span class="sc">~</span> <span class="st">"Bachelor or Above"</span>,</span>
<span id="cb78-13"><a href="#cb78-13" aria-hidden="true" tabindex="-1"></a>  ))</span>
<span id="cb78-14"><a href="#cb78-14" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb78-15"><a href="#cb78-15" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb78-16"><a href="#cb78-16" aria-hidden="true" tabindex="-1"></a>ur_race <span class="ot">&lt;-</span> palms <span class="sc">|&gt;</span></span>
<span id="cb78-17"><a href="#cb78-17" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(empstat1 <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">"employed"</span>,<span class="st">"unemployed"</span>)) <span class="sc">|&gt;</span></span>
<span id="cb78-18"><a href="#cb78-18" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(popgroup) <span class="sc">|&gt;</span></span>
<span id="cb78-19"><a href="#cb78-19" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(</span>
<span id="cb78-20"><a href="#cb78-20" aria-hidden="true" tabindex="-1"></a>    <span class="at">n_lf     =</span> <span class="fu">n</span>(),</span>
<span id="cb78-21"><a href="#cb78-21" aria-hidden="true" tabindex="-1"></a>    <span class="at">n_unemp  =</span> <span class="fu">sum</span>(empstat1 <span class="sc">==</span> <span class="st">"unemployed"</span>),</span>
<span id="cb78-22"><a href="#cb78-22" aria-hidden="true" tabindex="-1"></a>    <span class="at">unemp_rate =</span> n_unemp <span class="sc">/</span> n_lf</span>
<span id="cb78-23"><a href="#cb78-23" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb78-24"><a href="#cb78-24" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(<span class="fu">desc</span>(unemp_rate))</span>
<span id="cb78-25"><a href="#cb78-25" aria-hidden="true" tabindex="-1"></a>  </span>
<span id="cb78-26"><a href="#cb78-26" aria-hidden="true" tabindex="-1"></a>ur_race <span class="sc">|&gt;</span> </span>
<span id="cb78-27"><a href="#cb78-27" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>()<span class="sc">+</span></span>
<span id="cb78-28"><a href="#cb78-28" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(<span class="at">x =</span> popgroup, <span class="at">y =</span> unemp_rate, <span class="at">fill =</span> popgroup) <span class="sc">+</span></span>
<span id="cb78-29"><a href="#cb78-29" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_col</span>(<span class="at">color =</span> <span class="cn">NA</span>)<span class="sc">+</span></span>
<span id="cb78-30"><a href="#cb78-30" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span> (<span class="at">x =</span> <span class="st">"Ethnic Group"</span>, <span class="at">y =</span> <span class="st">"Unemployment Rate"</span>)<span class="sc">+</span></span>
<span id="cb78-31"><a href="#cb78-31" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_classic</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<div>
<figure class="figure">
<p><img src="Visualizations-Sample_files/figure-html/unnamed-chunk-3-1.png" class="img-fluid figure-img" width="672"></p>
</figure>
</div>
</div>
<div class="sourceCode cell-code" id="cb79"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb79-1"><a href="#cb79-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb79-2"><a href="#cb79-2" aria-hidden="true" tabindex="-1"></a>ur_race_education <span class="ot">&lt;-</span> palms <span class="sc">|&gt;</span></span>
<span id="cb79-3"><a href="#cb79-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(empstat1 <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">"employed"</span>,<span class="st">"unemployed"</span>), <span class="sc">!</span><span class="fu">is.na</span>(education)) <span class="sc">|&gt;</span></span>
<span id="cb79-4"><a href="#cb79-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(popgroup, education) <span class="sc">|&gt;</span></span>
<span id="cb79-5"><a href="#cb79-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(</span>
<span id="cb79-6"><a href="#cb79-6" aria-hidden="true" tabindex="-1"></a>    <span class="at">n_lf     =</span> <span class="fu">n</span>(),</span>
<span id="cb79-7"><a href="#cb79-7" aria-hidden="true" tabindex="-1"></a>    <span class="at">n_unemp  =</span> <span class="fu">sum</span>(empstat1 <span class="sc">==</span> <span class="st">"unemployed"</span>),</span>
<span id="cb79-8"><a href="#cb79-8" aria-hidden="true" tabindex="-1"></a>    <span class="at">unemp_rate =</span> n_unemp <span class="sc">/</span> n_lf</span>
<span id="cb79-9"><a href="#cb79-9" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb79-10"><a href="#cb79-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(<span class="fu">desc</span>(unemp_rate))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>`summarise()` has grouped output by 'popgroup'. You can
override using the `.groups` argument.</code></pre>
</div>
<div class="sourceCode cell-code" id="cb81"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb81-1"><a href="#cb81-1" aria-hidden="true" tabindex="-1"></a>ur_race_education <span class="sc">|&gt;</span> </span>
<span id="cb81-2"><a href="#cb81-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>()<span class="sc">+</span></span>
<span id="cb81-3"><a href="#cb81-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(<span class="at">x =</span> popgroup, <span class="at">y =</span> unemp_rate, <span class="at">fill =</span> popgroup) <span class="sc">+</span></span>
<span id="cb81-4"><a href="#cb81-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_text</span>(<span class="fu">aes</span>(<span class="at">label =</span> <span class="fu">percent</span>(unemp_rate, <span class="at">accuracy =</span> <span class="fl">0.1</span>)),</span>
<span id="cb81-5"><a href="#cb81-5" aria-hidden="true" tabindex="-1"></a>            <span class="at">vjust =</span> <span class="sc">-</span><span class="fl">0.3</span>, <span class="at">size =</span> <span class="dv">3</span>)<span class="sc">+</span></span>
<span id="cb81-6"><a href="#cb81-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_col</span>(<span class="at">color =</span> <span class="cn">NA</span>)<span class="sc">+</span></span>
<span id="cb81-7"><a href="#cb81-7" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span> (<span class="at">x =</span> <span class="st">"Ethnic Group"</span>, <span class="at">y =</span> <span class="st">"Unemployment Rate"</span>, <span class="at">fill =</span> <span class="st">"Ethnic Group"</span>)<span class="sc">+</span></span>
<span id="cb81-8"><a href="#cb81-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_grid</span>(<span class="sc">~</span> education)<span class="sc">+</span></span>
<span id="cb81-9"><a href="#cb81-9" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_classic</span>()<span class="sc">+</span></span>
<span id="cb81-10"><a href="#cb81-10" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme</span>(</span>
<span id="cb81-11"><a href="#cb81-11" aria-hidden="true" tabindex="-1"></a>    <span class="at">axis.text.x  =</span> <span class="fu">element_blank</span>(),   </span>
<span id="cb81-12"><a href="#cb81-12" aria-hidden="true" tabindex="-1"></a>    <span class="at">axis.ticks.x =</span> <span class="fu">element_blank</span>()    </span>
<span id="cb81-13"><a href="#cb81-13" aria-hidden="true" tabindex="-1"></a>  )</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<div>
<figure class="figure">
<p><img src="Visualizations-Sample_files/figure-html/unnamed-chunk-3-2.png" class="img-fluid figure-img" width="672"></p>
</figure>
</div>
</div>
<div class="sourceCode cell-code" id="cb82"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb82-1"><a href="#cb82-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb82-2"><a href="#cb82-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb82-3"><a href="#cb82-3" aria-hidden="true" tabindex="-1"></a><span class="co">#0 Recode NAs as zeroes</span></span>
<span id="cb82-4"><a href="#cb82-4" aria-hidden="true" tabindex="-1"></a>palms <span class="ot">&lt;-</span> palms<span class="sc">|&gt;</span></span>
<span id="cb82-5"><a href="#cb82-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">imputed_real =</span> <span class="fu">replace_na</span>(<span class="fu">as.numeric</span>(imputed_real), <span class="dv">0</span>))</span>
<span id="cb82-6"><a href="#cb82-6" aria-hidden="true" tabindex="-1"></a><span class="co">#1 mu_w - mu_b = 5807.827</span></span>
<span id="cb82-7"><a href="#cb82-7" aria-hidden="true" tabindex="-1"></a><span class="fu">mean</span>(palms<span class="sc">$</span>imputed_real[palms<span class="sc">$</span>popgroup <span class="sc">==</span> <span class="st">"White"</span>], <span class="at">na.rm =</span> <span class="cn">TRUE</span>) <span class="sc">-</span></span>
<span id="cb82-8"><a href="#cb82-8" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mean</span>(palms<span class="sc">$</span>imputed_real[palms<span class="sc">$</span>popgroup <span class="sc">==</span> <span class="st">"African/Black"</span>], <span class="at">na.rm =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>[1] 5807.827</code></pre>
</div>
<div class="sourceCode cell-code" id="cb84"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb84-1"><a href="#cb84-1" aria-hidden="true" tabindex="-1"></a><span class="co">#2 sigma_w = 23943.573, sigma_b = 9569.209</span></span>
<span id="cb84-2"><a href="#cb84-2" aria-hidden="true" tabindex="-1"></a>palms <span class="sc">|&gt;</span></span>
<span id="cb84-3"><a href="#cb84-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(popgroup <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">"White"</span>,<span class="st">"African/Black"</span>)) <span class="sc">|&gt;</span></span>
<span id="cb84-4"><a href="#cb84-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(popgroup) <span class="sc">|&gt;</span></span>
<span id="cb84-5"><a href="#cb84-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarise</span>(<span class="at">sigma =</span> <span class="fu">sqrt</span>(<span class="fu">mean</span>((imputed_real <span class="sc">-</span> <span class="fu">mean</span>(imputed_real, <span class="at">na.rm =</span> <span class="cn">TRUE</span>))<span class="sc">^</span><span class="dv">2</span>, <span class="at">na.rm =</span> <span class="cn">TRUE</span>)))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code># A tibble: 2 × 2
  popgroup       sigma
  &lt;fct&gt;          &lt;dbl&gt;
1 African/Black  9569.
2 White         23944.</code></pre>
</div>
<div class="sourceCode cell-code" id="cb86"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb86-1"><a href="#cb86-1" aria-hidden="true" tabindex="-1"></a><span class="co">#3 n_w = 7192, n_b = 56338</span></span>
<span id="cb86-2"><a href="#cb86-2" aria-hidden="true" tabindex="-1"></a>n <span class="ot">&lt;-</span> palms <span class="sc">|&gt;</span></span>
<span id="cb86-3"><a href="#cb86-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(empstat1 <span class="sc">==</span> <span class="st">"employed"</span>,</span>
<span id="cb86-4"><a href="#cb86-4" aria-hidden="true" tabindex="-1"></a>         popgroup <span class="sc">%in%</span> <span class="fu">c</span>(<span class="st">"White"</span>,<span class="st">"African/Black"</span>)) <span class="sc">|&gt;</span></span>
<span id="cb86-5"><a href="#cb86-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">count</span>(popgroup)</span>
<span id="cb86-6"><a href="#cb86-6" aria-hidden="true" tabindex="-1"></a><span class="co">#4 sd = 285.1985</span></span>
<span id="cb86-7"><a href="#cb86-7" aria-hidden="true" tabindex="-1"></a><span class="fu">sqrt</span>(<span class="fl">23943.573</span><span class="sc">^</span><span class="dv">2</span><span class="sc">/</span><span class="dv">7192</span> <span class="sc">+</span> <span class="fl">9569.209</span><span class="sc">^</span><span class="dv">2</span><span class="sc">/</span><span class="dv">56338</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>[1] 285.1985</code></pre>
</div>
<div class="sourceCode cell-code" id="cb88"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb88-1"><a href="#cb88-1" aria-hidden="true" tabindex="-1"></a><span class="co">#5 z = 20.36416</span></span>
<span id="cb88-2"><a href="#cb88-2" aria-hidden="true" tabindex="-1"></a>(<span class="fl">5807.827</span> <span class="sc">-</span> <span class="dv">0</span>)<span class="sc">/</span><span class="fl">285.1985</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>[1] 20.36416</code></pre>
</div>
<div class="sourceCode cell-code" id="cb90"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb90-1"><a href="#cb90-1" aria-hidden="true" tabindex="-1"></a><span class="co">#6 p-value = 3.477652e-92</span></span>
<span id="cb90-2"><a href="#cb90-2" aria-hidden="true" tabindex="-1"></a>p_value <span class="ot">&lt;-</span> <span class="dv">2</span> <span class="sc">*</span> <span class="fu">pnorm</span>(<span class="sc">-</span><span class="fu">abs</span>(<span class="fl">20.36416</span>))</span>
<span id="cb90-3"><a href="#cb90-3" aria-hidden="true" tabindex="-1"></a><span class="fu">print</span>(p_value)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>[1] 3.477652e-92</code></pre>
</div>
<div class="sourceCode cell-code" id="cb92"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb92-1"><a href="#cb92-1" aria-hidden="true" tabindex="-1"></a><span class="co">#7 confidence interval = [5248.83794, 6366.81606]</span></span>
<span id="cb92-2"><a href="#cb92-2" aria-hidden="true" tabindex="-1"></a>ci_left <span class="ot">&lt;-</span> <span class="fl">5807.827</span> <span class="sc">-</span> <span class="fl">1.96</span><span class="sc">*</span><span class="fl">285.1985</span></span>
<span id="cb92-3"><a href="#cb92-3" aria-hidden="true" tabindex="-1"></a>ci_right <span class="ot">&lt;-</span> <span class="fl">5807.827</span> <span class="sc">+</span> <span class="fl">1.96</span><span class="sc">*</span><span class="fl">285.1985</span></span>
<span id="cb92-4"><a href="#cb92-4" aria-hidden="true" tabindex="-1"></a><span class="co"># Insert only code here.</span></span>
<span id="cb92-5"><a href="#cb92-5" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb92-6"><a href="#cb92-6" aria-hidden="true" tabindex="-1"></a>white <span class="ot">&lt;-</span> <span class="fu">with</span>(palms, imputed_real[popgroup <span class="sc">==</span> <span class="st">"White"</span>])</span>
<span id="cb92-7"><a href="#cb92-7" aria-hidden="true" tabindex="-1"></a>black <span class="ot">&lt;-</span> <span class="fu">with</span>(palms, imputed_real[popgroup <span class="sc">==</span> <span class="st">"African/Black"</span>])</span>
<span id="cb92-8"><a href="#cb92-8" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb92-9"><a href="#cb92-9" aria-hidden="true" tabindex="-1"></a><span class="fu">t.test</span>(white, black, <span class="at">var.equal =</span> <span class="cn">FALSE</span>, <span class="at">alternative =</span> <span class="st">"two.sided"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre class="bg-warning"><code>
    Welch Two Sample t-test

data:  white and black
t = 28.124, df = 14020, p-value &lt; 2.2e-16
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 5403.048 6212.607
sample estimates:
mean of x mean of y 
 7974.177  2166.350 </code></pre>
</div>
</div>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const isCodeAnnotation = (el) => {
    for (const clz of el.classList) {
      if (clz.startsWith('code-annotation-')) {                     
        return true;
      }
    }
    return false;
  }
  const onCopySuccess = function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  }
  const getTextToCopy = function(trigger) {
      const codeEl = trigger.previousElementSibling.cloneNode(true);
      for (const childEl of codeEl.children) {
        if (isCodeAnnotation(childEl)) {
          childEl.remove();
        }
      }
      return codeEl.innerText;
  }
  const clipboard = new window.ClipboardJS('.code-copy-button:not([data-in-quarto-modal])', {
    text: getTextToCopy
  });
  clipboard.on('success', onCopySuccess);
  if (window.document.getElementById('quarto-embedded-source-code-modal')) {
    const clipboardModal = new window.ClipboardJS('.code-copy-button[data-in-quarto-modal]', {
      text: getTextToCopy,
      container: window.document.getElementById('quarto-embedded-source-code-modal')
    });
    clipboardModal.on('success', onCopySuccess);
  }
    var localhostRegex = new RegExp(/^(?:http|https):\/\/localhost\:?[0-9]*\//);
    var mailtoRegex = new RegExp(/^mailto:/);
      var filterRegex = new RegExp('/' + window.location.host + '/');
    var isInternal = (href) => {
        return filterRegex.test(href) || localhostRegex.test(href) || mailtoRegex.test(href);
    }
    // Inspect non-navigation links and adorn them if external
 	var links = window.document.querySelectorAll('a[href]:not(.nav-link):not(.navbar-brand):not(.toc-action):not(.sidebar-link):not(.sidebar-item-toggle):not(.pagination-link):not(.no-external):not([aria-hidden]):not(.dropdown-item):not(.quarto-navigation-tool):not(.about-link)');
    for (var i=0; i<links.length; i++) {
      const link = links[i];
      if (!isInternal(link.href)) {
        // undo the damage that might have been done by quarto-nav.js in the case of
        // links that we want to consider external
        if (link.dataset.originalHref !== undefined) {
          link.href = link.dataset.originalHref;
        }
      }
    }
  function tippyHover(el, contentFn, onTriggerFn, onUntriggerFn) {
    const config = {
      allowHTML: true,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start',
    };
    if (contentFn) {
      config.content = contentFn;
    }
    if (onTriggerFn) {
      config.onTrigger = onTriggerFn;
    }
    if (onUntriggerFn) {
      config.onUntrigger = onUntriggerFn;
    }
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      if (note) {
        return note.innerHTML;
      } else {
        return "";
      }
    });
  }
  const xrefs = window.document.querySelectorAll('a.quarto-xref');
  const processXRef = (id, note) => {
    // Strip column container classes
    const stripColumnClz = (el) => {
      el.classList.remove("page-full", "page-columns");
      if (el.children) {
        for (const child of el.children) {
          stripColumnClz(child);
        }
      }
    }
    stripColumnClz(note)
    if (id === null || id.startsWith('sec-')) {
      // Special case sections, only their first couple elements
      const container = document.createElement("div");
      if (note.children && note.children.length > 2) {
        container.appendChild(note.children[0].cloneNode(true));
        for (let i = 1; i < note.children.length; i++) {
          const child = note.children[i];
          if (child.tagName === "P" && child.innerText === "") {
            continue;
          } else {
            container.appendChild(child.cloneNode(true));
            break;
          }
        }
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(container);
        }
        return container.innerHTML
      } else {
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(note);
        }
        return note.innerHTML;
      }
    } else {
      // Remove any anchor links if they are present
      const anchorLink = note.querySelector('a.anchorjs-link');
      if (anchorLink) {
        anchorLink.remove();
      }
      if (window.Quarto?.typesetMath) {
        window.Quarto.typesetMath(note);
      }
      if (note.classList.contains("callout")) {
        return note.outerHTML;
      } else {
        return note.innerHTML;
      }
    }
  }
  for (var i=0; i<xrefs.length; i++) {
    const xref = xrefs[i];
    tippyHover(xref, undefined, function(instance) {
      instance.disable();
      let url = xref.getAttribute('href');
      let hash = undefined; 
      if (url.startsWith('#')) {
        hash = url;
      } else {
        try { hash = new URL(url).hash; } catch {}
      }
      if (hash) {
        const id = hash.replace(/^#\/?/, "");
        const note = window.document.getElementById(id);
        if (note !== null) {
          try {
            const html = processXRef(id, note.cloneNode(true));
            instance.setContent(html);
          } finally {
            instance.enable();
            instance.show();
          }
        } else {
          // See if we can fetch this
          fetch(url.split('#')[0])
          .then(res => res.text())
          .then(html => {
            const parser = new DOMParser();
            const htmlDoc = parser.parseFromString(html, "text/html");
            const note = htmlDoc.getElementById(id);
            if (note !== null) {
              const html = processXRef(id, note);
              instance.setContent(html);
            } 
          }).finally(() => {
            instance.enable();
            instance.show();
          });
        }
      } else {
        // See if we can fetch a full url (with no hash to target)
        // This is a special case and we should probably do some content thinning / targeting
        fetch(url)
        .then(res => res.text())
        .then(html => {
          const parser = new DOMParser();
          const htmlDoc = parser.parseFromString(html, "text/html");
          const note = htmlDoc.querySelector('main.content');
          if (note !== null) {
            // This should only happen for chapter cross references
            // (since there is no id in the URL)
            // remove the first header
            if (note.children.length > 0 && note.children[0].tagName === "HEADER") {
              note.children[0].remove();
            }
            const html = processXRef(null, note);
            instance.setContent(html);
          } 
        }).finally(() => {
          instance.enable();
          instance.show();
        });
      }
    }, function(instance) {
    });
  }
      let selectedAnnoteEl;
      const selectorForAnnotation = ( cell, annotation) => {
        let cellAttr = 'data-code-cell="' + cell + '"';
        let lineAttr = 'data-code-annotation="' +  annotation + '"';
        const selector = 'span[' + cellAttr + '][' + lineAttr + ']';
        return selector;
      }
      const selectCodeLines = (annoteEl) => {
        const doc = window.document;
        const targetCell = annoteEl.getAttribute("data-target-cell");
        const targetAnnotation = annoteEl.getAttribute("data-target-annotation");
        const annoteSpan = window.document.querySelector(selectorForAnnotation(targetCell, targetAnnotation));
        const lines = annoteSpan.getAttribute("data-code-lines").split(",");
        const lineIds = lines.map((line) => {
          return targetCell + "-" + line;
        })
        let top = null;
        let height = null;
        let parent = null;
        if (lineIds.length > 0) {
            //compute the position of the single el (top and bottom and make a div)
            const el = window.document.getElementById(lineIds[0]);
            top = el.offsetTop;
            height = el.offsetHeight;
            parent = el.parentElement.parentElement;
          if (lineIds.length > 1) {
            const lastEl = window.document.getElementById(lineIds[lineIds.length - 1]);
            const bottom = lastEl.offsetTop + lastEl.offsetHeight;
            height = bottom - top;
          }
          if (top !== null && height !== null && parent !== null) {
            // cook up a div (if necessary) and position it 
            let div = window.document.getElementById("code-annotation-line-highlight");
            if (div === null) {
              div = window.document.createElement("div");
              div.setAttribute("id", "code-annotation-line-highlight");
              div.style.position = 'absolute';
              parent.appendChild(div);
            }
            div.style.top = top - 2 + "px";
            div.style.height = height + 4 + "px";
            div.style.left = 0;
            let gutterDiv = window.document.getElementById("code-annotation-line-highlight-gutter");
            if (gutterDiv === null) {
              gutterDiv = window.document.createElement("div");
              gutterDiv.setAttribute("id", "code-annotation-line-highlight-gutter");
              gutterDiv.style.position = 'absolute';
              const codeCell = window.document.getElementById(targetCell);
              const gutter = codeCell.querySelector('.code-annotation-gutter');
              gutter.appendChild(gutterDiv);
            }
            gutterDiv.style.top = top - 2 + "px";
            gutterDiv.style.height = height + 4 + "px";
          }
          selectedAnnoteEl = annoteEl;
        }
      };
      const unselectCodeLines = () => {
        const elementsIds = ["code-annotation-line-highlight", "code-annotation-line-highlight-gutter"];
        elementsIds.forEach((elId) => {
          const div = window.document.getElementById(elId);
          if (div) {
            div.remove();
          }
        });
        selectedAnnoteEl = undefined;
      };
        // Handle positioning of the toggle
    window.addEventListener(
      "resize",
      throttle(() => {
        elRect = undefined;
        if (selectedAnnoteEl) {
          selectCodeLines(selectedAnnoteEl);
        }
      }, 10)
    );
    function throttle(fn, ms) {
    let throttle = false;
    let timer;
      return (...args) => {
        if(!throttle) { // first call gets through
            fn.apply(this, args);
            throttle = true;
        } else { // all the others get throttled
            if(timer) clearTimeout(timer); // cancel #2
            timer = setTimeout(() => {
              fn.apply(this, args);
              timer = throttle = false;
            }, ms);
        }
      };
    }
      // Attach click handler to the DT
      const annoteDls = window.document.querySelectorAll('dt[data-target-cell]');
      for (const annoteDlNode of annoteDls) {
        annoteDlNode.addEventListener('click', (event) => {
          const clickedEl = event.target;
          if (clickedEl !== selectedAnnoteEl) {
            unselectCodeLines();
            const activeEl = window.document.querySelector('dt[data-target-cell].code-annotation-active');
            if (activeEl) {
              activeEl.classList.remove('code-annotation-active');
            }
            selectCodeLines(clickedEl);
            clickedEl.classList.add('code-annotation-active');
          } else {
            // Unselect the line
            unselectCodeLines();
            clickedEl.classList.remove('code-annotation-active');
          }
        });
      }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->




</body></html>
