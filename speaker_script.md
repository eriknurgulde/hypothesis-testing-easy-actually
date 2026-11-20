# Speaker script: "hypothesis testing is easy, actually" (16 slides)

For two presenters, **A** and **B**. Swap the letters for your names. Target: about 15–18 minutes: 1 minute per slide, plus 1–2 minutes per Kapchagay problem.

## Driving the deck
- **→ / Space / wheel / click** = next slide. **←** = back. **G** = grid of all slides. Type a number + **Enter** to jump. **R** replays a slide's animation. **F** = fullscreen.
- Each slide builds itself over 2–4 seconds. Start talking about the first item while the rest pops in, and let the meme or stamp at the end land on its own.

**Split:** A does 1–6, B does 7–13, and you share the Kapchagay problems (A does 14, B does 15, both do 16). The handover line is marked ➜. On slides 14–16, the **show answer** button reveals the solution without changing the slide.

---

## A (slides 1–6)

**1 · Title.** "Hypothesis testing. Your textbook says you need Z-tables, t-tables and four Greek letters. All you actually need is a coin and trust issues."

**2 · Suspicious coin.** "Your friend's coin, 10 flips. Nine heads? Kinda sus. Zero heads? Definitely rigged. Three? Eh, could be luck. *(meme pops in)* That's your brain at 9 heads. Hypothesis testing is just that feeling, with math."

**3 · The courtroom.** "Every test is a tiny trial. H₀, the null hypothesis, is 'innocent until proven guilty': the coin is fair. H_A, the alternative, is the accusation: it's rigged. X, the test statistic, is the evidence: the number of heads. The null distribution is how an innocent coin behaves, here Binomial(10, 0.5). *(gavel slams)* Order. The coin never has to prove it's innocent. We only convict if the evidence is overwhelming."

**4 · What a fair coin does.** "Exactly 5 heads only happens 24.6% of the time, so fair coins are a bit weird. Say we call ≤ 2 or ≥ 8 heads suspicious. Add up the red bars: 0.11. So we'd jail an innocent coin 11% of the time. *(bars drop)* That 11% is the significance level, alpha: the probability of rejecting H₀ when it's actually true. Our false-alarm rate, picked before we look at the data."

**5 · Two ways to mess up.** "Two mistakes. Type I: convict an innocent coin, a false positive. Smoke-alarm version: it beeps but it was just toast. Type II: a rigged coin walks free, a false negative: real fire, no alarm. *(this is fine)* That's Type II. Make alpha smaller and you get fewer false alarms but more missed fires."

**6 · The recipe.** "Three steps. One: pick H₀. Two: one-sided or two-sided, meaning which direction makes you suspicious. *(two buttons)* One-sided puts the red zone on one end. Two-sided splits it across both ends. Three: pick alpha and find the rejection region."

➜ **A:** "How do you actually find that region? B?"

---

## B (slides 7–13), then both (14–16)

**7 · Alpha is a budget.** "Treat alpha like a budget. Add the most extreme results to the red zone one at a time and stop before the total goes over alpha. Two-sided at 0.05: 0, 1, 9, 10 cost 0.021. Adding 2 and 8 makes it 0.109, over budget. So the region is {0, 1, 9, 10}. The table has all four versions. Piece of cake."

**8 · Real life.** "Brawl Stars. Say a Mega Box gives a legendary 1% of the time, and these odds are made up. 100 boxes, zero legendaries: 0.99 to the 100th is 0.366, so 37% of honest players get this. Fail to reject, you're just unlucky. 300 boxes, still zero: 0.049. That's under 0.05, so reject. Now you can write the angry Reddit post.
Casino. In 1913, at Monte Carlo, a fair wheel hit black 26 times in a row, about 1 in 137 million. At a new casino you see 9 reds in 10 spins. Red is 18/37. One-sided at 0.05, the region is {8, 9, 10}, so we reject. But 1913 is the reminder: fair wheels fail tests sometimes too. That's a Type I error, and alpha is how often it happens."

**9 · Are CityU students smarter?** "Population IQ has mean 100 and SD 15. H₀: μ = 100, H_A: μ > 100, one-sided, alpha 0.05. Nine students average 110. The key fact: an average of 9 wobbles less than one person. Its SD is σ / √n = 15 / 3 = 5. *(bell-curve meme)* By the end of the next slide you'll be the guy on the right."

**10 · Verdicts.** "If H₀ is true, the average sits on a bell at 100 with SD 5. The top 5% starts at 108.22, and 110 is past it, so we reject. But look at the table. With alpha 0.01 the fence moves to 111.63 and we don't reject. Two-sided at 0.01, we don't reject. Two-sided at 0.05, we reject, by 0.2 IQ points. *(Pikachu)* Same data, four verdicts. That's why you pick alpha and the sides before you look at the data."

**11 · Plot twist: unknown σ.** "In real life nobody gives you σ. You estimate it from your 9 scores. *(Drake)* Don't divide by n. Divide by n − 1, because the sample sits closer to its own average than to the truth. That gives s = 21.35, so the SE is 21.35 / 3 = 7.12. Since we guessed σ, we use the t-distribution: the normal after it found out it doesn't know σ. It has fatter tails, with df = n − 1 = 8. *(Spider-Man)* The fence becomes ±2.306 instead of ±1.96. Our t is (110 − 100) / 7.12 = 1.40, which is inside, so we fail to reject. Fun fact: Gosset invented it at the Guinness brewery and published as 'Student'."

**12 · Recap.** "Assume innocent. Collect evidence. Ask whether an innocent party would do this. Convict only in the red zone. And 'not guilty' isn't 'innocent': failing to reject H₀ doesn't prove it. Next: the formulas, then we go to Kapchagay."

**13 · Formulas.** "Every formula from today on one card. Binomial for counts. Standard error is σ/√n, or s/√n if you had to estimate σ. z when σ is known, t with n − 1 degrees of freedom when it isn't. Fence = μ₀ ± critical value × SE. Screenshot it, because the next three slides use all of it."

**14 · Kapchagay problem 1: stingy slot machine.** *(Lever pulls, reels spin, it lands 7-7-₸. So close.)* "The sign says you win on 20% of spins. You play 20 and win once. Tighter than advertised? Give the class ~20 seconds, then click **show answer**. H₀: p = 0.2, H_A: p < 0.2. Zero wins has probability 0.8²⁰ = 0.012, under budget. Adding one win brings it to 0.069, over. So the rejection region is {0}, and one win isn't in it. You're not cursed, just broke."

**15 · Kapchagay problem 2: '95% payback'.** "The casino says slots pay back 950₸ per 1000₸ on average, σ = 200. Your 25 sessions average 870. *(pause, show answer)* SE = 200/5 = 40, z = −2. At α = 0.05 the fence is 884.2, 870 is below it, reject. At α = 0.01 the fence is 857, 870 is above it, fail to reject. Suspicious at 5%, not proven at 1%. Same data, different α, different verdict, just like the IQ slide."

**16 · Kapchagay problem 3: the blackjack 'system'.** "Your friend's 9 nights: +5, −4, +8, −6, +6, +4, −3, +7, +1 (thousand ₸). Does it make money? *(pause, show answer)* Mean 2. σ is unknown, so we use s: s² = 216/8 = 27, s = 5.20, SE = 1.73, t = 1.15 with 8 df. The one-sided fence is 1.860, so we fail to reject. His system is pure luck, and those are only the nights he told you about.
**A:** Moral: the house always wins.
**B:** We're collecting donations in the form of correct exam answers."

> Tip: open the deck with `?answers` at the end of the address (before the `#`) to show all three answers at once while you prep.

---

## If someone asks
- **Why 0.05?** It's a convention: a 1-in-20 false-alarm rate.
- **Can I "accept" H₀?** No, only fail to reject it.
- **t or z?** Use t when σ is estimated by s. With big n they're almost the same.
- **Corrections to the original PDF** (in case someone compares): two-sided α = 0.05 uses ±1.96, not ±2.57. At one-sided α = 0.01, 110 is *not* rejected (110 < 111.63). 2.306 is a t-score, not a Z-score. Binomial(10, 0.5) has variance 2.5, not 1.25.
