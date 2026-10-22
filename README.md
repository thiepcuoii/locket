# README – Locket Gold Only

---

## Cấu trúc thư mục

```
testlk_locket/
├── js/
│   ├── Locket_VanTrung.js      ← Script unlock Gold qua RevenueCat (Locket-specific, response)
│   ├── Locket_Unlocked.js       ← Script unlock Gold + tính năng qua Firebase Remote Config (response)
│   ├── Locket_rc_us.js          ← Script giả vùng US qua Firebase Remote Config (request) – tuỳ chọn
│   ├── revenuecat.js            ← Script generic RevenueCat – có mapping 'Locket': ['Gold'] dòng 109
│   └── deleteHeader.js          ← Script xoá header X-RevenueCat-ETag (request) – dùng chung
├── modules/
│   └── Locket_vantrung.sgmodule  ← Module Surge/Shadowrocket chỉ cho Locket
├── assets/
│   ├── locket.mobileconfig       ← Hồ sơ DNS (Cloudflare + chặn Sentry/Amplitude/AppsFlyer)
│   └── LocketGold.mobileconfig   ← Hồ sơ DNS đơn giản (ublockdns) chặn thu hồi Gold
├── Locket_Only.conf              ← Shadowrocket Configuration chỉ Locket
├── Locket_Only.sgmodule          ← Shadowrocket Module chỉ Locket
└── Egern_LocketGold_Only.yaml    ← Egern config chỉ Locket
```

## Cách dùng nhanh (Shadowrocket)

1. Cài `.mobileconfig` tương ứng (vào Safari → tải → Cài đặt → Hồ sơ)
2. Import `Locket_Only.sgmodule` vào Shadowrocket (tab Cấu Hình → Module)
3. Bật VPN

> **Lưu ý:** Chỉ dùng cho mục đích học tập, không thương mại. Nguồn gốc: @vtrungg