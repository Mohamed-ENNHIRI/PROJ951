# PROJ951: Solar project case study, economic and environmental assessment

Solar Academy, Université Savoie Mont Blanc. Course material, released session
by session.

One rooftop photovoltaic project, 99 kWp on a building near Chambéry. Your group
assesses the project for one building, a school, an office or a supermarket, on
three sides: the energy balance, the business case and the carbon balance,
within the French rules for rooftop PV. Two business models: total sale, and
self-consumption with surplus sale.

Material appears here as the course progresses.

## Format

- **TD1, TD2, TD3**: short notebooks. One line of code per task, a check under
  each task. Everyone works on the school.
- **TP1**: one notebook for the building of your group. Parts 1 to 5: energy
  balance, cash flows, NPV, payback, LCOE. Part 6: size, sensitivity and
  break-even grid price. The note to the owner closes the notebook.
- **Oral**: in the TP2 slot. There is no TP2 notebook. Where the CM2 slides
  mention TP2, read TP1 part 6 for size and sensitivity, and TD3 for the carbon
  balance.

| Your building | Groups | Demand per year |
|---|---|---|
| School | 1, 4, 7 | 140 MWh |
| Office building | 2, 5 | 220 MWh |
| Supermarket | 3, 6 | 650 MWh |

## Project

Hand in the evening before the oral, in one message to the teacher:

1. **Slides**: five slides plus a title slide, in English, as a PDF. 10 minutes,
   every member speaks.
2. **Note to the owner**: one page, 300 words at most, for a reader with no
   technical training. Every number with its unit.
3. **TP1 notebook**: executed from top to bottom, record sheet and answers
   filled in. The carbon values come from TD3.

Grade out of 20: 18 points for the group, 2 individual points from the answers
to the questions. Questions cover the whole course.

## Slides

| Session | Slides |
|---|---|
| CM2 | [cm2_slides.pdf](03_cm2/cm2_slides.pdf) |

## Notebooks

| Session | Notebook | Exercises | Correction |
|---|---|---|---|
| CM1 | Notebook 0: Python introduction | [python_intro.ipynb](https://colab.research.google.com/github/Mohamed-ENNHIRI/PROJ951/blob/main/notebooks/python_intro.ipynb) | [python_intro.ipynb](https://colab.research.google.com/github/Mohamed-ENNHIRI/PROJ951/blob/main/notebooks/corrections/python_intro.ipynb) |
| TD1 | The bill and the energy balance, school case | [td1_bill_and_balance.ipynb](https://colab.research.google.com/github/Mohamed-ENNHIRI/PROJ951/blob/main/notebooks/td1_bill_and_balance.ipynb) | [td1_bill_and_balance.ipynb](https://colab.research.google.com/github/Mohamed-ENNHIRI/PROJ951/blob/main/notebooks/corrections/td1_bill_and_balance.ipynb) |
| TD2 | Time value of money | [td2_time_value.ipynb](https://colab.research.google.com/github/Mohamed-ENNHIRI/PROJ951/blob/main/notebooks/td2_time_value.ipynb) | after the session |

Before running anything: **File, Save a copy in Drive**. Without a copy, your
work is lost when the tab closes.

## Python resources

- W3Schools Python tutorial, short lessons with exercises in the browser:
  https://www.w3schools.com/python/default.asp
- Python documentation: https://docs.python.org/3/
- NumPy documentation: https://numpy.org/doc/
- pandas, "10 minutes to pandas": https://pandas.pydata.org/docs/user_guide/10min.html

## Data

`data/proj951_case_data.csv` holds one row per hour of 2019, in local standard
time (UTC+1):

- `pv_kwh_per_kwp`: output of 1 kWp on the roof, 30° tilt, south, 14 % losses,
  from PVGIS 5.3 (SARAH3 and ERA5), 45.57° N, 5.92° E. 1334 kWh/kWp per year.
- `temp_c`: air temperature, same source.
- `load_school_kwh`, `load_office_kwh`, `load_supermarket_kwh`: demand of the
  three buildings, 140, 220 and 650 MWh per year. Synthetic profiles built for
  the course: the shapes follow the opening hours and holidays, the values are
  not measured.

Every price, tariff and carbon factor in the notebooks is a course value, set
for teaching. None of them is a tariff in force.
