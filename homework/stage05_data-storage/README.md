## Formats Used

- **CSV (raw)**
  - Human-readable and widely supported.
  - Used for storing original raw data.
- **Parquet (processed)**
  - Compressed, efficient, preserves dtypes.
  - Used for validated and processed data.

---

## Environment-Driven Paths

Paths are configured via `.env` file:

```env
DATA_DIR_RAW=data/raw
DATA_DIR_PROCESSED=data/processed