# Overview

This is a small project that aimed at scraping the results of a league in Music League. 

Music League is a website where you participate in submitting songs for a weekly thematic with other people, followed by voting and commenting the best song for each round. There you have leagues, which are groups of people that have their own rounds and submissions. 

Process steps:
- Run `0_init.ipynb`;
- Run `1_scrape.ipynb` (an overview of this process can be seen in `scraping_demo.mp4`). Scraped data is saved to `output/1_scraped_data`;
- Run `2_data_proc.ipynb` to process the scraped data. The final processed data is saved to `output/2_processed_data/260321_proc_data_3.xlsx`.

# Why it is interesting

To me it was interesting to do this project, because I addressed the following challenges:
- Combined manual action (receiving and submitting a login token on the website authorisation page) and automatic parts (all the rest of the steps - pressing buttons, choosing the league of interest, scraping every round's results in that league);
- Data analysis was also an interesting part. It's not perfect, but using heuristic rules I managed to do a good-enough job
  - ⚠️ One thing to improve: right now, I am scraping processed text (without html tags) to one csv file and then process it, extracting name of round, song name, comments, etc., primarily based on newlines. This is a heuristic rule that works well, but not perfectly, e.g. if someone comments the username of another user in their comment. This can be improved by saving complete data (with html) and working on that;
- I can reuse the code for when I finish the future leagues in Music League. 

