# facresults — лёгкая копия Stage1 (json/csv) по хронологии

20 архивов по ~96 фото (~3.8 МБ) — лимит 4 МБ, хронологические группы `1998-01-01 → 2026-05-13`.

Внутри каждого `Архив_XX_YYYY-MM-DD_YYYY-MM-DD.zip`:
- `part_XX/main_timeline_part.csv` — срез `main_timeline.csv` для этого периода (`photo_id,date,pose_bin,pitch/yaw/roll` `app6/stage1/naming.py:30` `config.py:16`)
- `part_XX/00_README_хронология_файлов.md` — описание
- `<photo_id>/info.json, texture.json, validation.json, ldm*_*.csv` — только `json/csv/txt` (`stage1_json_only` `validator.py:110` `complete`)

Источник: `/Volumes/SDCARD/storage/stage1` (39G, 1909 фото) → `stage1_json_only` `00_README_хронология_файлов.md` `app6/stage1/geometry.py:87` `full_pose_correction_v1` — для проверки используйте `ldm*_chronology.csv`.

Сборка: `python3` `zipfile.ZIP_DEFLATED` по `main_timeline.csv` сортировке `chronology_index_global` `app6/CONVENTIONS.py:90`.
