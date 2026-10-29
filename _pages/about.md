---
permalink: /
layout: home
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="container">
  <div class="left-column">
    <img src="{{ base_path }}/images/headshot.jpg" alt="Hui-Jhong (Hugh) Choi" title="Hui-Jhong (Hugh) Choi"/>
  </div>
  <div class="right-column">
    <p>
      I am a fourth-year Finance PhD student at the University of Rochester (Simon Business School). Prior to joining Simon, I received my master's and bachelor's degrees in economics from Korea University. During my undergraduate studies, I interned at J.P. Morgan as a credit risk specialist.<br>
      <br>
      My research focuses on asset pricing, especially investor beliefs and disagreement.<br>
      <br>
      <a href="{{ base_path }}/files/Hui_Jhong_Choi_CV.pdf" target="_blank">
        <i class="fas fa-file icon-pad-right"></i>Curriculum Vitae
      </a><br>
      <a href="mailto:hchoi43@simon.rochester.edu">
        <i class="fas fa-envelope icon-pad-right"></i>hchoi43@simon.rochester.edu
      </a>
    </p>
  </div>
</div>

<div id="research" class="home-section">
  <h1 class="adjust-title">Research</h1>

  <!-- Label options: paper-tag--published, paper-tag--working, paper-tag--wip -->
  <!-- Abstract button: data-abstract must match the id of the abstract box below it -->
  <div class="paper">
    <span class="paper-tag paper-tag--working">Working Paper</span><br>
    <span class="paper-title">Model Disagreement and Factor Momentum</span><br>
    <div class="paper-links">
      <button type="button" class="paper-btn" data-abstract="abs-disagreement" aria-expanded="false">Abstract</button>
      <span class="paper-note">Draft coming soon</span>
    </div>
    <div class="abstract" id="abs-disagreement" hidden>
      I study whether disagreement about which characteristics are priced explains factor momentum. In a model where investors hold dogmatic and differing views about the characteristic through which a common factor affects payoffs, equilibrium prices underreact to the true factor loading. Greater disagreement then raises factor return autocorrelation, factor volatility, and time series factor momentum up to a threshold. I construct two novel measures of model disagreement for 152 characteristics, one from I/B/E/S analyst price targets and one from 13F institutional holdings. Both measures are positively related to all three model quantities in Fama–MacBeth predictive regressions. Disagreement predicts both the short-term and the longer-term timing component of factor momentum. Taken together, the results imply that disagreement may drive factor momentum.
    </div>
  </div>

  <div class="paper">
    <span class="paper-tag paper-tag--wip">Work in Progress</span><br>
    <span class="paper-title">The Term Structure of Corporate Required Rates</span><br>
    <i>with Qixiang Gao</i><br>
    <div class="paper-links">
      <button type="button" class="paper-btn" data-abstract="abs-term-structure" aria-expanded="false">Abstract</button>
    </div>
    <div class="abstract" id="abs-term-structure" hidden>
      This paper proposes a systematic approach, combining recent advances in characteristics-based asset pricing with dimensionality-reduction techniques, to estimate the term structure of required equity returns for U.S. stocks. The estimated premium sensitivities to firm characteristics change substantially with the investment horizon, indicating that the composition of priced risk shifts as the holding period lengthens. In an application to corporate investment, we find that longer-horizon required rates are more strongly associated with firm-level investment than short-horizon premia, and that firms with longer asset maturity are especially sensitive to these long-term required rates, consistent with the idea that their investments face longer cash-flow duration.
    </div>
  </div>

  <div class="paper">
    <span class="paper-tag paper-tag--published">Published</span><br>
    <a class="paper-title-link" href="https://academic.oup.com/jfec/article-abstract/23/4/nbaf016/8212035?redirectedFrom=fulltext" target="_blank">
      <span class="paper-title">Finding Inflation Uncertainty Factors: A Sparse Stochastic Volatility Approach</span>
    </a><br>
    <i>with Kyu Ho Kang</i><br>
    <i>Journal of Financial Econometrics</i>, 23(4), July 2025<br>
    <div class="paper-links">
      <a class="paper-btn" href="https://academic.oup.com/jfec/article-abstract/23/4/nbaf016/8212035?redirectedFrom=fulltext" target="_blank">Journal</a>
      <button type="button" class="paper-btn" data-abstract="abs-inflation" aria-expanded="false">Abstract</button>
    </div>
    <div class="abstract" id="abs-inflation" hidden>
      Inflation uncertainty is an undeniable factor in economic decision-making. In this study, we investigate predictive factors that possess information on inflation uncertainty among many observable macroeconomic variables and uncertainty indices. To do this, we estimate several inflation prediction models popular in the literature, allowing for stochastic volatility with predetermined variables. We apply the Dirac spike-and-slab prior to the volatility-explaining variables to detect relevant macroeconomic determinants of the inflation volatility process. Contrary to prior studies suggesting that the inflation level is essentially a unique factor explaining inflation uncertainty, our findings reveal that survey inflation expectations and the capacity utilization rate are significantly more relevant. These results remain robust to different models of inflation.
    </div>
  </div>
</div>


<script>
document.addEventListener('click', function (e) {
  var btn = e.target.closest('.paper-btn[data-abstract]');
  if (!btn) { return; }
  var box = document.getElementById(btn.getAttribute('data-abstract'));
  var opening = box.hidden;
  box.hidden = !opening;
  btn.setAttribute('aria-expanded', opening ? 'true' : 'false');
  btn.classList.toggle('is-open', opening);
});
</script>
