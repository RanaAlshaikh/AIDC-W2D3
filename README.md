## W2D3: Container Optimization Results

### Image Size Comparison

| Stage | Image | Image Size |
|---|---|---|
| Naive build (full base, cached pip) | `aidc-serving:naive` | 1.6 GB |
| Optimized build (slim base, CPU PyTorch, no pip cache) | `ranaalshaikh/aidc-serving:cpu-v1` | 1.26 GB |

By adopting `python:3.11-slim`, omitting pip cache with `--no-cache-dir`, and pulling CPU-only PyTorch wheels, the final image size was reduced by 340 MB (a 21% decrease).

---

### Verification

- **Image:** `ranaalshaikh/aidc-serving:cpu-v1`
- **Health Check:** `200 OK`
- **Inference Test:** `OK`
- **Result:** `GREEN CHECK: PASS`

<img width="675" height="81" alt="s4" src="https://github.com/user-attachments/assets/4515f7a4-86f2-4459-ab38-3741f05e8204" />
