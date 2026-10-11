# The human evaluation Tinder 📱

### The bright idea

Human evaluations are really tiring to obtain. So let’s turn language-generation evaluation into a swipe-based mobile experience: the human evaluation Tinder. Instead of dragging annotators into a spreadsheet or a clunky web form, present them with one comparison at a time (e.g., two model outputs, or one output + a specific quality dimension) and let them swipe: right for "better/pass," left for "worse/fail," up for "flag/uncertain," etc. Sessions are short, async, and mobile-native, so people can knock out evaluations in idle moments (waiting for coffee, on the bus) instead of sitting down for a dedicated labeling session. Layer in gamification (streaks, levels, leaderboards, "taste badges" (e.g., "Readability Referee," "Fact-Checker Tier 3"), …) to turn a tedious annotation chore into something people actually want to open. 

### The goal

Lower the friction and boredom of human evaluation enough to get more labels, more often, from a more diverse pool of evaluators.

### Data to use

- Model outputs to evaluate: generate pairs/sets of responses from several LLMs (varying sizes or prompting strategies) on a shared prompt set — could draw from existing open benchmarks like MT-Bench, Chatbot Arena prompts, or HELM tasks, so you can later sanity-check your crowd-sourced results against established leaderboards.
- Dimensions: helpfulness, readability, factual correctness, conciseness, tone. Each has its own swipe deck or a dimension-selector before swiping.
- Ground truth / calibration set: a small subset with known "gold" quality labels (from existing benchmark annotations) to measure how well the swipe data agrees with expert/reference judgments.
- Evaluator metadata: anonymized swipe timestamps, response latency, streaks, and self-reported expertise. These are useful for analyzing whether gamification incentives introduce bias (e.g., speed-swiping for streaks at the cost of quality) and can be used as a secondary metric (long reading time = low readability)
