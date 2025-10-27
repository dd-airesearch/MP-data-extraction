# MP-data-extraction
This code provde download of Materials Project via API
# Detailed guidalines can be see below
End-to-end Li–O–X pipeline (robust to mp_api variants).

Outputs (under --out_dir, default: out_li_o_x):
  - mp_li_o_x_ids.txt /.csv
  - mp_li_o_x_summary.jsonl (all fields)
  - per_mpid/<mpid>/
      summary.json\
      structures/POSCAR.summary.vasp\
      structures/POSCAR.task-<task_id>.vasp (when available)\
      tasks/task_ids.json\
      tasks/<task_id>.json\
      thermo.json\
      magnetism.json\
      dielectric.json\
      phonon.json\
      elasticity.json\
      bandstructure.json\
      CHGCAR.vasp (if available)\
      xrd_cuka.csv

Usage:
  MP_API_KEY=... python li_o_x_pipeline_v2.py --procs 40 --resume
"""
