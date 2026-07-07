[title]: <> (VBlog + Custom CSS)
[date]: <> (2026/07/07)
[category]: <> (general)

<style>
body { --color-bg: #fff; --color-text: #333; --color-anchor: #337ab7; --color-heading: #111; --color-divider: #cdcdcd; --color-code-bg: #f7f7f7; --color-code-text: #333; --color-table-border: #c2c2c2; --color-table-row-even: #f0f0f0; --color-table-row-odd: #fff; --color-toggle-accent: #c3a554; }
body table { width: 100%; border-collapse: collapse; margin: 1em 0px; }
body blockquote { margin: 0px 0px 1em; padding: 0px 1em; border-left: 4px solid var(--color-divider); color: var(--color-text); opacity: 0.8; }
body table tr:nth-child(2n) { background: var(--color-table-row-even); }
body code { background: var(--color-code-bg); color: var(--color-code-text); padding: 0.2em 0.4em; border-radius: 4px; }
body h1, body h2, body h3, body h4, body h5, body h6 { color: var(--color-heading); line-height: 1.25; margin-top: 1.2em; margin-bottom: 0.6em; }
body h1 { font-size: 2rem; }
body h2 { font-size: 1.6rem; }
body h3 { font-size: 1.3rem; }
body a { color: var(--color-anchor); text-decoration: none; }
body a:hover, body a:focus { text-decoration: underline; }
body img, body svg { max-width: 100%; height: auto; }
</style>

# <span style="font-family: Georgia, serif">Some ways to use ZK-SNARKs for privacy</span>

ZK-SNARKs are a powerful cryptographic tool, and an increasingly important part of the applications that people are building both in the blockchain space and beyond. But they are complicated, both in terms of _how they work_, and in terms of _how you can use them_.

## What does a ZK-SNARK do?

Suppose that you have a public input x, a private input w, and a (public) function <span style="font-family: MJXc-TeX-math-Iw">f(x,w)→{True,False}</span> that performs some kind of verification on the inputs. With a ZK-SNARK, you can prove that you know an w such that <span style="font-family: MJXc-TeX-math-Iw">f(x,w)=True</span> for some given <span style="font-family: MJXc-TeX-math-Iw">f</span> and <span style="font-family: MJXc-TeX-math-Iw">x</span>, without revealing what <span style="font-family: MJXc-TeX-math-Iw">w</span> is. Additionally, the verifier can verify the proof much faster than it would take for them to compute <span style="font-family: MJXc-TeX-math-Iw">f(x,w)</span> themselves, even if they know <span style="font-family: MJXc-TeX-math-Iw">w</span>.

![](https://vitalik.eth.limo/images/using_snarks/definition.png)

This gives the ZK-SNARK its two properties: **privacy** and **scalability**. As mentioned above, in this post our examples will focus on privacy.

## Holding centralized parties accountable

Sometimes, you need to build a scheme that has a central "operator" of some kind. This could be for many reasons: sometimes it's for scalability, and sometimes it's for privacy - specifically, the privacy of data held by the operator.

<iframe src="https://www.youtube.com/embed/9kT0oLBPiOw" width="640" height="360"></iframe>

Thanks to blockchains and ZK-SNARKs, the amount of trust in the operator can be kept very low. A malicious operator could still break coercion resistance, but because votes are published on the blockchain, the operator cannot cheat by censoring votes, and because the operator must provide a ZK-SNARK, they cannot cheat by mis-calculating the result.

## Combining ZK-SNARKs with MPC

A more advanced use of ZK-SNARKs involves making proofs over computations where the inputs are split between two or more parties, and we don't want each party to learn the other parties' inputs. You can satisfy the privacy requirement with [garbled circuits](https://vitalik.eth.limo/general/2020/03/21/garbled.html) in the 2-party case, and more complicated multi-party computation protocols in the N-party case. ZK-SNARKs can be combined with these protocols to do verifiable multi-party computation.

> Read the full article by [Vitalik Buterin](https://vitalik.eth.limo/general/2021/01/26/snarks.html)

| Custom CSS      | Vblog            |
| --------------- | ---------------- |
| jflksdfjds dfsd | sdfdsf dsfsdf    |
| sdfdsf dsfdsf   | sdfsdf dsfsdfdsf |

> what the helllyyyyyyy?

We added new shortcut for `subscript`: Cmd + Shift + 6