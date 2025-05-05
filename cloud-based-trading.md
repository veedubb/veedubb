<h1>Cloud-Based Trading Strategies for Individual Investors</h1>
<p>
  This project required me to sign an NDA, so I am unable to share the repository. However, I can speak to higher level details about the project.
</p>
<h2>Technologies Used:</h2>

- <b>Front End</b>
  - React
  - Node
- <b> Back End </b>
  - Flask
  - MySQL
  - MongoDB
- <b>Critical Libraries</b>
  - yfinance
  - PyMoo
  - backtesting.py

 <h2>Notable Achievement and Roadblocks</h2>
 
- <b>Validation of Backtesting Results</b>
  - Team was tasked with validating results of backtesting.py with those our industry sponsor was able to get from another library.
    - Motivation: backtesting.py offered performance improvements over the tool previously used.
    - Challenges:
      - The team had access to results, but not the source code of the existing backtester.
    - Result:
      - We were able to get reliable results that were consistently within an acceptable margin of the results our sponsor was producing.
      - This was mainly due to the correction of warm-up period problems that were occurring as we neared the edge of historical data that yfinance offers.
- <b>Application Breaking Dependency Issues</b>
  - Team faced significant challenge after Yahoo Finance changed their API, which broke the yfinance library for large swaths of users.
  - Challenges:
    - Upgrading the library (recommended fix) caused dependency errors in other libraries.
    - Leaving the library at the previously working version meant that we could not fetch historical data for any tickers.
  - Result:
    - The team upgraded the library to the latest version in order to correct the data ingestion issues.
    - We worked through each individual error that this caused, refactoring various pieces of the application and upgrading other dependencies to allow the application to continue working.
- <b>Results Display</b>
  - Team was tasked with creating a more modern and valuable view into the results of the optimizations.
    - Motivation:
      - Previous iterations of the application provided very basic charts and output pertaining to the results of running the algorithm/problem against historical data.
      - In addition, this output was generally limited to small subsets of the resultant optimizations
    - Challenges:
      - The existing library that was used by previous teams did not offer all the functionality that the team needed to meet the sponsor's requirements.
    - Result:
      - The team moved to a new library as part of the migration from a monolith to an MVC application and was able to produce output meeting the sponsor's requirements.
- <b>Migration from Monolith to MVC</b>
  - Previous teams had developed the web application as a monolith, our team was tasked with creating a more distributed architecture for the application.
    - Motivation:
      - Since these optimizations can be quite compute intensive, distributing the workload can provide a more responsive experience for users and decrease things like wait time.
      - In addition, our sponsor wanted to transition to a cloud-hosted solution for easy access anywhere.
    - Challenges:
      - Previous teams had built project as a monolith - breaking this apart into various subcomponents required a deep understanding of what the application was doing "under-the-hood".
      - Compartmentalizing various components meant that the team would need to "specialize" in specific areas rather than working on the project more wholly.
    - Result:
      - The project was restructured to an MVC architecture, where the front end communicates with a controller which orchestrates various model operations (database and calculations).
      - Notable performance improvements over the existing monolith, especially concerning compute time for strategy optimization.


<!--
**joshmadakor1/joshmadakor1** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
