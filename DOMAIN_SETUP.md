# aiwith.kr 연결 체크리스트

## 현재 연결 구조

이 저장소는 멘토K 프롬프트랩만 독립적으로 서비스합니다.

- https://aiwith.kr/ → 멘토K 프롬프트랩
- https://aiwith.kr/admin.html → 관리자 대시보드
- https://www.aiwith.kr/ → aiwith.kr로 정규화

저장소 루트에 CNAME 파일(aiwith.kr)을 포함했습니다.

## hosting.kr DNS

호스팅.kr DNS 관리에서 다음 레코드를 사용합니다.

- @ A 185.199.108.153
- @ A 185.199.109.153
- @ A 185.199.110.153
- @ A 185.199.111.153
- www CNAME mentor-k.github.io

중복 A·CNAME·리다이렉트 레코드는 제거하고, AAAA 레코드는 사용하지 않습니다.

## GitHub Pages

저장소 Settings → Pages → Build and deployment에서 다음을 확인합니다.

1. Source: Deploy from a branch
2. Branch: main
3. Folder: /(root)
4. Custom domain: aiwith.kr
5. 인증서 발급 후 Enforce HTTPS 활성화

인증서 발급과 DNS 전파에는 수 분에서 최대 24시간이 걸릴 수 있습니다. 발급 전에는 502 또는 hostname mismatch가 나타날 수 있습니다.

## 검증

    dig aiwith.kr A
    dig www.aiwith.kr CNAME
    curl -I https://aiwith.kr/

Google Search Console에는 https://aiwith.kr/sitemap.xml을 제출합니다. AdSense 승인 후 발급받은 실제 publisher ID로만 ads.txt와 광고 코드를 연결합니다.
