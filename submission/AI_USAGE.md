# AI_USAGE — K4-Track02-Day18

## Cong cu

- OpenCode (Muse Spark 1.3), chay trong moi truong lab offline.

## Pham vi ho tro

- Giai thich khai niem: transaction log / enforcement vs evolution, Z-order va file
  pruning, hidden partitioning va field ID, 5 job maintenance, vector lifecycle,
  version pin va provenance.
- Ho tro doc code notebook (`notebooks/*.py`) va ghi chu truc tiep theo dong code
  khi tra loi cau hoi giang.
- Giu loi moi truong Windows: tao `.venv`, cai `requirements.txt`, `jupytext` +
  `jupyter nbconvert --execute` de luu output vao `.ipynb`.
- Tao khung `submission/` va render PNG cho `screenshots/`.
- **Khong** viet lai logic trong bat ky notebook nao. Code goc khong doi dong nao
  (`git diff` tren file nguon = rong); chi co `submission/` la file moi.

## Tu chay va tu kiem chung

Toan bo so lieu trong `INFO.md` va `screenshots/` do chay tren may nay:

| Buoc | Lenh | Ket qua |
|---|---|---|
| Smoke | `scripts/verify_lite.py` | 9/9 PASS |
| Pytest | `python -m pytest -q` | 24/24 PASS |
| Runner | `scripts/run_all.py` | 8/8 PASS (41.9s) |
| Tung notebook | `jupyter nbconvert --execute` x8 | output luu trong `submission/notebooks/` |

Kiem tra them truc tiep tren dia: doc `_lakehouse/scratch/users_delta/_delta_log/*.json`,
dem lai Gold/Silver tren bang Delta, dung chinh xac nhung gi da in trong notebook.
NB2, NB6, NB7 da chay lai nhieu lan de kiem tra so do on dinh (chi khac o wall-clock).

## Bao ca o

- Mot so trong `AI_USAGE.md` (dong "Cong cu") va ban phat thao cua `REFLECTION.md` do
  AI phat sinh. **Hoc vien can doc lai va viet lai bang tu ngon ngu rieng** truocc khi
  nop; `RULES.md` yeu cau nguoi nop tu giai thich duoc ma nguon va ket qua cua minh.
- Anh trong `screenshots/` la **PNG render tu output that cua lan chay** (van ban +
  bang bang), khong phai anh chup man hinh Jupyter UI. Noi dung lay truc tiep tu
  Delta/Iceberg va tu stdout cua notebook, khong sua so lieu.

## Khong lam

- Khong tao so lieu gia, khong ha nguong, khong bo assertion, khong viet ket luan cho
  lan chay chua thuc hien.
- Khong gui secret hay du lieu rieng tu vao prompt.
