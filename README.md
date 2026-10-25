# 반발계수 충돌 후 속도 계산기

일직선에서 충돌하는 두 물체의 운동량과 반발계수로 첫 물체의 충돌 후 속도를 계산합니다.

- ID: E121
- App: https://nanalab.kr/eng-collision-restitution/
- Repository: https://github.com/NaNaCompany/eng-collision-restitution
- Formula: v₁ = [(m₁ − e m₂)u₁ + (1 + e)m₂u₂] / (m₁ + m₂)

## Model and data

두 물체가 같은 직선에서 충돌하며 충돌 중 외부 충격량을 무시합니다. 첫 물체는 +축 방향으로 둘째 물체의 뒤에 있어 u₁ ≥ u₂로 입력합니다. e는 0~1입니다. 두 속도가 같으면 변화가 없는 극한값을 표시합니다. 비스듬한 충돌·회전·물체 파손은 계산하지 않습니다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
