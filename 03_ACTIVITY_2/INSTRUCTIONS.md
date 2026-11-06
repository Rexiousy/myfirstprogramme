# Activity 2 - The $5 Snack Corner challenge

17 minutes after the setup check. Work in the SAME cloned repository as Activity 1.

## Your goal

- Buy at least 3 items in total.
- Include at least 1 drink (water or tea).
- Spend $5.00 or less. Exactly $5.00 is allowed.
- Aim as close to $5.00 as possible. Quantities count, so 2 bananas and 1 drink are 3 items.

Read MENU.md for the fixed prices. You choose quantities; you do not change prices or checker code.
You do not need to install Python locally for the GitHub-hosted check.

## Before the timer

1. Open your own cloned repository in VS Code, not this extracted pack.
2. Finish pending work, exit PR review mode if active, choose main using the bottom-left branch picker and use Source Control > ... > Pull.
3. If an old receipt-check workflow was already added, disable it on GitHub or remove its .yml file from .github/workflows on the branch you will use. It is no longer part of Activity 2. Keep unrelated workflows. Your Activity 1 reciept.py can stay in the repository.

## 0-5 minutes - Set up and choose your order

1. Click the branch label > Create new branch... and enter snack-challenge.
2. From 03_ACTIVITY_2/COPY_INTO_YOUR_REPO, copy ALL CONTENTS into the ROOT of your clone, beside README.md. Copy the contents, not the enclosing folder.
3. Merge existing .github and scripts folders rather than replacing them. Do not overwrite unrelated files. The four supplied files must end up at:
   - order.csv
   - MENU.md
   - scripts/check_order.py
   - .github/workflows/snack-check.yml
4. Check the dot folder copied too. If it is hidden in your file browser, create .github and workflows using VS Code Explorer and copy snack-check.yml into workflows.
5. Read MENU.md. Open order.csv in the VS Code text editor.
6. Change only the numbers in the quantity column. 0 means none; use whole numbers such as 1 or 2 for selected items. Keep item,quantity and all six item IDs unchanged.
7. The starter contains all zeros so you can choose your own order. Make your choices BEFORE your first push; there is no required failing baseline.

## 5-10 minutes - Publish your order

1. Press Ctrl+S (Cmd+S on Mac) to save order.csv.
2. Open Source Control. Review the four supplied files, including your quantities.
3. Click + beside each intended file (or beside Changes if these four are the only pending files).
4. Enter Add my snack order and click Commit.
5. Click Publish Branch, choosing origin if asked. Finish browser sign-in if requested. For an already-published branch, use ... > Push.
6. In your GitHub repository, choose Actions > Snack order check. Open the run for Add my snack order on snack-challenge. Wait while it queues and runs.

## 10-17 minutes - Read and improve

1. Read the order summary on the run page. For the detailed log, open check-order > Check snack order.
2. Check your total cost, total number of items, number of drinks and remaining budget.
3. PASS means your order meets all three rules. If you have budget left, try improving the order so it is closer to $5.00. You do not need to make it fail first.
4. NEEDS CHANGES means the report names an unmet rule or an input problem. For example, an order may cost too much or contain no drink. Change your real choices or correct the input, rather than breaking Python on purpose.
5. To try again, edit quantity numbers in order.csv, save, inspect the diff, stage ONLY order.csv, commit Improve my snack order and use ... > Push.
6. Open the NEW run matching your latest commit. Re-running an old run checks the old order; it does not pick up uncommitted edits.

## Show your facilitator

- A PASS for your own order on snack-challenge.
- Your total cost and remaining budget.
- At least 3 items and at least 1 drink in the report.
- The commit containing your chosen quantities.

If you reach exactly $5.00, try finding a different valid combination or help explain the result to a neighbour. Do not edit MENU.md, scripts/check_order.py or the workflow to change the rules.

No PR merge is required for this checkpoint. You may open and merge a PR into main after completing it; switch to local main and Pull after a merge.

## Troubleshooting

- No run: confirm all four files were copied and committed, the .github path is correct and the commit reached GitHub. A disabled Actions setting or a repository policy can also block a run.
- Cannot find order.csv: it must be beside README.md, not inside COPY_INTO_YOUR_REPO.
- Wrong header or unknown item: restore the supplied header and item IDs; edit quantities only.
- Quantity error: use 0, 1, 2 and other non-negative whole numbers, without currency symbols or decimals.
- Over budget: reduce quantities or choose cheaper items. Prices are per item.
- No drink or too few items: include water or tea and count all quantities together.
