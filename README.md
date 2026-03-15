# 🚀 D-Link DIR-1360 A1 OpenWrt Builder

Custom automated firmware builder for D-Link DIR-1360 A1, providing patched and legacy-compatible OpenWrt builds.

---

### 🤔 Why this when we have Official Support?

Even though official support exists (from 25.12), this repo solves multiple real-world issues:

---

### 🔹 1. Legacy Support (23.x / 24.x)

- Official support starts from 25.12 
- Many users still prefer:
  - ✅ 23.05 (stable)
  - ✅ 24.10 (stable)

This builder provides ready-to-flash images for older stable versions.

---

### 🔹 2. 5GHz Speed Fix (mt76 issue)

Some mt76-based devices suffer from:

- ❌ Poor 5GHz performance 

A community patch exists, but:

- 🚫 Cannot be merged upstream (affects non-external PA devices)

✅ This builder includes the fix for:

- 24.10.6 
- All future 25.12.x builds 

---

### 🔹 3. Deadlock Fix (24.10 only)

Includes:

- 🛠 PHY LED deadlock fix 

Applied only to:

- 24.10.x 
- 23.05.x
---

### 🔹 4. Fully Automated Builds ⚡

- 🤖 GitHub Actions-based pipeline 

Automatically:
- Detects new OpenWrt releases 
- Builds firmware 
- Publishes to Releases 

📌 For 25.12.x: 
New builds will appear automatically within ~6–8 hours after official release.

---

### 📦 Build Behavior

| Version | Status |
|--------|--------|
| 22.03 | 🧊 Built once (legacy support + patched) |
| 23.05 | 🧊 Built once (legacy support + patched) |
| 24.10 | 🧊 Built once (patched) |
| 25.12 | 🔄 Continuous builds (future releases) |

---

### ⚙️ Included Enhancements

- ✅ DIR-1360 A1 backported support (for older versions) 
- ✅ mt76 5GHz performance patch 
- ✅ Deadlock fix (24.10 only) 
- ❌ No unnecessary modifications 

---

### 📥 Download Firmware

👉 [Click Here](https://github.com/aryaman895/D-Link-DIR-1360-OpenWrt-Builder/releases) to go Github Releases section of this repo.

You will find:

- `factory.bin` → for first-time flashing 
- `sysupgrade.bin` → for upgrading existing OpenWrt 

---

# 🔧 Flash Instructions

### 🟢 Method: Recovery Web UI

1. Set static IP on your PC 
   - IP: `192.168.0.10` 
   - Gateway: `192.168.0.1` 

2. Connect PC to router 
   - Use LAN port 

3. Enter recovery mode 
   - Power OFF router 
   - Hold Reset button 
   - Power ON while holding 
   - Keep holding for ~5 seconds 

4. Open recovery page 
   - 🌐 http://192.168.0.1 

5. Upload firmware 
   - Select `factory.bin` 
   - Wait for flashing & reboot 

---

### ⚠️ Important Notes

- ⚡ First boot may take a few minutes 
- 🔌 Do NOT power off during flashing 
- 🔄 Use `sysupgrade.bin` only for upgrades 
- 🧪 22.03 builds use older toolchain (best effort support) 

---

### ❤️ Credits

- OpenWrt Team 
- mt76 contributors 
- Community patch contributors 

---

### ⭐ Support

If this project helps you:

👉 Star ⭐ the repo 
👉 Share with other DIR-1360 users 
