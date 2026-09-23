# iOS/iPad adaptive layout proof

Code: Solvely-Colin/openclaw branch fix/ios-adaptive-layout-20260923, commit d85af18e131e. Reviewed and built against main 0b0777a17057.

All images/recordings are real native simulator captures, not mocked product screens. Black rectangles redact only the model label.

- resize.gif and resize.mp4: entire48.87second connected1032→486→1032 window resize at original speed; draft retained at all3 observed checkpoints. GIF is a lower-resolution preview; MP4 is1032×1376. Sidebar deliberately hidden in this recording.
- before-sizing.png: earlier iteration of this branch, before removing the nested560pt assistant cap. Not a clean-main baseline.
- after-sizing.png: final sizing pass, same real conversation at a different scroll position.
- ipad-portrait-sidebar.png: offline native iPad portrait with the final persistent sidebar policy; no seeded content.
- validation.txt: excerpts from actual test logs. Fresh current-base native72/72 passed. Phone/iPad UI captures and connected proof predate the base refresh; none of the UI implementation paths changed in that refresh.

Limitations: simulator proof, not physical-iPad certification. Earlier connected47second proof establishes selection/focus continuity for the stable shell; the48.87second resize recording here checks sizing and draft retention. Accessibility navigation policy has unit coverage, not a new large-text visual capture. The pre-existing iPhone landscape toolbar clipping is not fixed.
