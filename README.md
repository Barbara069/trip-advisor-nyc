# Trip Advisor: NYC Restaurant Explorer

A December 2022 team project combining Yelp ratings and NYC restaurant inspection data to help visitors explore restaurants beyond review scores. Built with Python, SQL, Flask, and geospatial visualization.

## Features

- Search restaurants by name or ZIP code.
- Map matching restaurants across NYC neighborhoods.
- Compare average Yelp ratings across Manhattan cuisines.
- Explore highly rated restaurants with many recorded violations and recommendations with fewer recorded violations.
- Serve JSON results and chart images through Flask endpoints.

## Project materials

- `Trip_Advisor_Website.ipynb`: original Colab notebook with credentials replaced by environment variables and saved outputs removed.
- `Trip_Advisor_Presentation.pdf`: 25-slide project presentation, with slide 11 replaced by a credentials-free summary because its screenshot contained an API key.

Original Google source links are omitted from this public copy because those originals contain embedded credentials.

## Setup and limitations

Open the notebook in Google Colab. Its setup cells install the packages and mount Google Drive. Before the Flask/ngrok and database cells run, set `NGROK_AUTHTOKEN` and `DB_PASSWORD` in the runtime environment. `.env.example` lists the variable names; the notebook does not automatically load an `.env` file.

The notebook references the original course MySQL database at `db.ipeirotis.org`, including `public.TEST2_Group_I_restaurant_yelp` and tables in `doh_restaurants`. Database access and table availability have not been verified. No database dump was supplied.

The website also requires these original HTML templates under `/content/drive/MyDrive/templates`:

- `trip_advisor_home_page.html`
- `list_res_api.html`
- `hotels.html`

Those templates and associated static assets were not included in the supplied notebook or presentation, so this repository is an archive of the available project materials, not a complete standalone web application. The original 2022 dependencies may need updates to run in current Colab environments. The notebook has not been executed as part of this upload.

The presentation discusses broader hotel and crime-analysis ideas. The supplied notebook primarily implements restaurant APIs; its cell titled “Crime Map” actually queries restaurant coordinates and Yelp ratings. Historical analysis should not be interpreted as current restaurant or neighborhood guidance.

## API routes

| Route | Purpose |
| --- | --- |
| `/res_api` | Restaurant search results |
| `/res_map` | Restaurant map image |
| `/traps` | Highly rated restaurants with many recorded violations |
| `/cuisine_rank` | Average ratings by cuisine |
| `/violations` | Violation chart |
| `/res_rank` | Restaurant recommendations |

## Team

Danny Tan, Bruce Teng, Barbara Bai, and Povilas Zinkevicius (Group I), as credited in the original presentation.
