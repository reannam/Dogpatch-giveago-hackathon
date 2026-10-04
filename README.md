# Dublin Budget 2026 civic prototype

A static, single-page proof of concept that makes Dublin City Council's adopted 2026 revenue budget easier to explore. It includes service-area charts, drill-down budget lines, a reorderable priority ranking, and a draft Eircode/TD lookup and anonymous-vote interaction.

## Run locally

Open `index.html` in a modern browser. No build step or package installation is required.

## Data and scope

Budget totals and selected service-line allocations are from Dublin City Council's **Adopted Revenue Budget 2026**:

- Budget page: https://www.dublincity.ie/your-city-council/governance-within-council/making-informed-and-transparent-decisions/annual-revenue-budget
- Adopted budget PDF: https://www.dublincity.ie/sites/default/files/2025-11/dublin-city-council-adopted-revenue-budget-2026.pdf

The prototype covers Dublin City Council's revenue budget, not the budgets of all four Dublin local authorities and not national government spending in Dublin. Drill-downs show selected service lines, not every activity in each division.

## Demo limitations / next implementation steps

- The Eircode form checks the format but does not resolve an address. Use the Electoral Commission's official checker to find a constituency: https://www.electoralcommission.ie/what-constituency-am-i-in/
- The vote button stores a ranking in the current browser's `localStorage`, keyed by the Eircode routing key (first three characters). It is not uploaded, aggregated across residents, or visible to TDs.
- Eircode routing areas do not map one-to-one to Dáil constituencies. A production service should resolve the full Eircode to the constituency, discard the full address/Eircode, and provide TDs only appropriately aggregated results. Current TD and party data should come from the Oireachtas directory/download: https://www.oireachtas.ie/en/members/tds/ and https://www.oireachtas.ie/en/contact-us/
- The ranking is a personal preference exercise; it does not change or predict the council's adopted budget.

## License

Prototype code is provided for evaluation. Confirm data and code licensing before public deployment.
