# Log-Periodic Option Pricing with Monte Carlo Simulation

**Undergraduate Thesis (B.Sc. in Physics)**  
**Henrique Alves de Lima** | University of Brasília (UnB), Institute of Physics  
**Advisor:** Leonardo Luíz e Castro | **November 2019**

[![Physics](https://img.shields.io/badge/Field-Physics%20%26%20Econophysics-254875)](#research-context)
[![Quantitative%20Finance](https://img.shields.io/badge/Focus-Quantitative%20Finance-117b85)](#research-context)
[![Monte%20Carlo](https://img.shields.io/badge/Method-Monte%20Carlo-62408d)](#methodology)
[![Research](https://img.shields.io/badge/Year-2019-596579)](#citation)

> **Research question:** Can a log-periodic model of financial bubbles be incorporated into a Monte Carlo option-pricing framework to study option prices during unusually rapid market movements?

## Overview

This repository contains my undergraduate thesis in Physics, completed at the **University of Brasília (UnB)** in 2019. The project lies at the intersection of **statistical physics, stochastic processes, quantitative finance, and computational modeling**. It investigates the pricing of European options in markets exhibiting speculative bubbles and sharp corrections, and explores a modification to a conventional Monte Carlo simulation informed by **log-periodic power-law fitting**.

The work compares standard **Black–Scholes pricing** with Monte Carlo estimates and then introduces a log-periodic adjustment to the simulated price dynamics. A historical Bitcoin episode serves as an illustrative case study for the adjusted model.

## Thesis files

| Document | Description |
| --- | --- |
| [English edition](TCC_LogPeriodic_Option_Pricing_EN.pdf) | English translation of the thesis for international readers. |
| [Original thesis (Portuguese)](Monografia___Instituto_de_F_sica___Universidade_de_Bras_lia__1_.pdf) | Original 2019 monograph submitted to UnB. |

## Research context

The thesis considers four historical financial time series: **Bitcoin (BTC-USD), Nikkei 225, NASDAQ Composite, and S&P 500**. It examines episodes associated with bubble formation and market corrections, studies the distribution of normalized absolute log returns, and fits price trajectories with a log-periodic model.

The log-periodic power-law function used in the study has the form

$$
L(t) = A + B(t_c-t)^z + C(t_c-t)^z\cos\bigl[\omega\log(t_c-t)+\phi\bigr].
$$

Here, $t_c$ is the critical time parameter; the other coefficients govern the shape of the fitted trajectory. The model is used to explore how a hypothesized market trajectory could modify simulated underlying-asset prices.

## Methodology

1. **Historical market analysis** — examine price evolution during selected bubble and crash intervals; characterize normalized absolute log-return distributions.
2. **Log-periodic fitting** — estimate the parameters of a log-periodic power-law model for selected market series.
3. **Pricing baseline** — introduce the Black–Scholes framework and estimate European option values using standard Monte Carlo simulation under a geometric Brownian motion assumption.
4. **Numerical evaluation** — study the convergence of the simulation, historical volatility, and antithetic-variable variance reduction.
5. **Adjusted Monte Carlo model** — incorporate a fitted log-periodic trajectory into the simulated underlying price dynamics and explore sensitivity to volatility and strike prices.

The thesis includes mathematical derivations, figures, historical comparisons, numerical experiments, and an appendix with a C-language Monte Carlo pricing algorithm.

## Main observations

- Log-periodic fitting provides a useful descriptive approximation for several bubble-period trajectories considered in the thesis, although the **Bitcoin fit presented difficulties** during particularly rapid price increases.
- Conventional Monte Carlo estimates can be compared with the Black–Scholes benchmark and improved by increasing the number of simulation paths; antithetic variates are discussed as a variance-reduction technique.
- The proposed adjusted simulation generates price paths influenced by the fitted log-periodic trend while retaining stochastic fluctuations.
- The resulting option valuations are sensitive to **historical volatility** and **strike selection**. The Bitcoin case study explores how the pricing estimate changes when the strike is informed by the fitted trajectory.

These are **exploratory findings from a 2019 undergraduate research project**, not a claim that financial crises can be forecast reliably or that the proposed pricing rule is arbitrage-free or suitable for live trading without further validation.

## Academic structure

The monograph is organized into three parts:

| Part | Topics |
| --- | --- |
| I. Financial market dynamics | Options and derivatives; market crashes; log-periodicity; historical indices and Bitcoin; log-periodic fits. |
| II. Option-pricing methods | Black–Scholes equation; Monte Carlo valuation; simulation design; antithetic variables; historical volatility; historical tests. |
| III. Adjusted Monte Carlo | Log-periodic correction to Monte Carlo trajectories; Bitcoin case study; interpretation and limitations. |

The document concludes with references and an appendix describing the original C implementation.

## Rebuilding the English PDF (optional)

The translated edition was typeset in LaTeX. The editable source and the 34 original research figures are included in the repository:

```bash
cd source
xelatex -interaction=nonstopmode English_Translation.tex
xelatex -interaction=nonstopmode English_Translation.tex
```

This requires a XeLaTeX installation with the Noto Serif, Lato, and Asana Math fonts and the LaTeX packages used by the source. The document is already available as a finished PDF, so compiling it is optional.

## Technical topics

`Econophysics` · `Quantitative Finance` · `Option Pricing` · `Black–Scholes` · `Monte Carlo` · `Stochastic Processes` · `Geometric Brownian Motion` · `Financial Bubbles` · `Log-Periodic Power Laws` · `Historical Volatility` · `C Programming`

## Citation

If referring to the original academic work, cite:

> Lima, Henrique Alves de. (2019). *Ajuste log-periódico aplicado à precificação de opções por método de Monte-Carlo* [Undergraduate thesis, Institute of Physics, University of Brasília]. Brasília, Brazil.

Suggested English rendering of the title: *Log-Periodic Fitting Applied to Option Pricing Using Monte Carlo Methods*.

## Notes

The research was written and submitted in **2019**. The English edition is provided as a reader-friendly translation; the **Portuguese original remains the authoritative academic version**. The original results and parameters reflect the historical windows examined in the thesis and should not be interpreted as contemporary market estimates or investment advice.

---

**Author:** Henrique Alves de Lima  
**Institution:** [University of Brasília (UnB)](https://www.unb.br/) — Institute of Physics
