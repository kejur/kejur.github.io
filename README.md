# kejur.github.io

> [!WARNING]\
> By default, the stats card only shows statistics like stars, commits and pull requests from public repositories. To show private statistics on the stats card, you should [deploy your own instance](#deploy-on-your-own) using your own GitHub API token.

> [!NOTE]\
> Available ranks are S (top 1%), A+ (12.5%), A (25%), A- (37.5%), B+ (50%), B (62.5%), B- (75%), C+ (87.5%) and C (everyone). This ranking scheme is based on the [Japanese academic grading](https://wikipedia.org/wiki/Academic_grading_in_Japan) system. The global percentile is calculated as a weighted sum of percentiles for each statistic (number of commits, pull requests, reviews, issues, stars and followers), based on the cumulative distribution function of the [exponential](https://wikipedia.org/wiki/exponential_distribution) and the [log-normal](https://wikipedia.org/wiki/Log-normal_distribution) distributions. The implementation can be investigated at [src/calculateRank.js](./src/calculateRank.js). The circle around the rank shows 100 minus the global percentile.

> [!IMPORTANT]\
> By default, the stats card only shows statistics like stars, commits and pull requests from public repositories. To show private statistics on the stats card, you should [deploy your own instance](#deploy-on-your-own) using your own GitHub API token.


[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/kejur/kejur.github.io)
