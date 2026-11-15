# Dr. Byongchoon Park profile page: deployment and linking

Owner: Dr. Byongchoon Park. Prepared 2026-11-15.

## 1. Where to upload

Upload the contents of this folder to `https://liposuction-laprinps.com/dr-park/` and keep the structure as it is:

| Language | File | Public URL |
|---|---|---|
| Korean | `index.html` | https://liposuction-laprinps.com/dr-park/ |
| English | `en/index.html` | https://liposuction-laprinps.com/dr-park/en/ |
| Japanese | `ja/index.html` | https://liposuction-laprinps.com/dr-park/ja/ |
| Traditional Chinese | `zh-tw/index.html` | https://liposuction-laprinps.com/dr-park/zh-tw/ |

Shared folders: `css/`, `fonts/`, `img/`, `video/`. The page uses its own `css/` and `img/` inside `/dr-park/`, so it does not touch the microsite's files.

**Missing file:** put `video/parkbc-interview-ko.mp4` (about 6.2 MB, the interview video) into `video/`. It was too large to include. Dr. Park has the original.

If you use a different folder than `/dr-park/`, find and replace `https://liposuction-laprinps.com/dr-park/` in the four HTML files. It appears in canonical, hreflang, og:url, og:image, twitter:image and the JSON-LD.

## 2. Already done inside the pages

- canonical, hreflang (ko, en, ja, zh-Hant, x-default = en), og:url, absolute og:image and twitter:image
- JSON-LD `@graph`: ProfilePage + MedicalWebPage, Person, MedicalClinic (address, hours, geo 37.5194205 / 127.0495416), FAQPage. The FAQ text on screen and in JSON-LD is identical. Please do not edit one without the other.
- Links from the profile page to the microsite: treatment names link to `abdominal-liposuction.html`, `fat-transfer-detail.html`, `hip-design.html`, `tummy-tuck-detail.html`, `breast-detail.html`, `renuvion-detail.html` in the matching language folder. The E-Lipo section links to the microsite home `#elipo`, and the footer links to the microsite home.

## 3. Please add links on the microsite (so patients can reach the profile)

Add a header navigation item on every microsite page, next to Philosophy:

| Microsite language | Label | Link |
|---|---|---|
| Korean (root) | 원장 소개 | `/dr-park/` |
| en | About Dr. Park | `/dr-park/en/` |
| ja | 院長紹介 | `/dr-park/ja/` |
| zh-tw | 醫師介紹 | `/dr-park/zh-tw/` |
| zh-cn, id, ru | (local label for "About the doctor") | `/dr-park/en/` until those languages exist |

Also add a text link under the director section on each language home page and on each `philosophy.html` page, pointing to the same URL (e.g. "Read Dr. Park's full profile").

## 4. After upload

1. Open each URL and check: images, both videos, language switcher, all messenger buttons.
2. View page source and confirm the JSON-LD block is intact. Test one URL in Google's Rich Results Test.
3. Add the four URLs to `sitemap.xml` and request indexing in Google Search Console.
4. Check `robots.txt` does not block OAI-SearchBot, PerplexityBot or Claude-SearchBot (default `User-agent: *` allow is fine).

## 5. Issues found on the microsite (separate fixes)

- Korean home footer "빠른 전화 연결" uses `tel:02-1899-7812`. It must be `tel:1899-7812` (1899 is a nationwide number with no area code).
- The microsite pages have no `hreflang` tags. Adding them across the language versions would help search engines match languages.

## Contact values (do not change)

KakaoTalk https://pf.kakao.com/_xieNxmV · WhatsApp https://wa.me/821050250858 · LINE https://line.me/R/ti/p/@246vmeej · Phone 1899-7812 (Korean page only)
