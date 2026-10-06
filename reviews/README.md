# Home @REVIEW

Cafe24 EYES OPEN `index_test.html`에서 사용하는 고객 스타일링 사진 목록입니다. 운영 `index.html`에는 아직 연결하지 않았습니다.

## 사진 등록

1. GitHub에서 `reviews/photos/` 안에 사용 허락을 받은 사진을 업로드합니다. Instagram 링크만으로는 사진이 자동 수집되지 않습니다.
2. `reviews/reviews.json`의 `items`에 사진 한 건을 추가합니다. 목록 순서대로 표시됩니다.
3. 커밋한 뒤 테스트 홈을 새로고침합니다. 실제 사진이 0건이면 등록 대기 시안을 표시합니다.

사진 원본 링크는 선택 사항입니다. `instagramUrl`은 Instagram 게시물/릴스의 HTTPS 링크만 받습니다. 비워 두면 사진은 클릭 링크 없이 표시됩니다. 상품 태그는 `tags`에 여러 개 넣을 수 있습니다. `x`, `y`는 사진 왼쪽/위에서부터 백분율 좌표이고 생략하면 하단에 순서대로 배치됩니다. `url`에는 실제 상품 페이지 링크를 넣습니다.

## 한 건의 형식 예시

다음은 등록 형식만 보여주는 예시입니다. 실제 고객 사진이나 후기 데이터가 아닙니다. 파일명, 설명, 링크, 상품명은 등록할 실제 자료로 바꿉니다.

```json
{
  "id": "review-001",
  "image": "photos/review-001.jpg",
  "alt": "고객 스타일링 사진",
  "instagramUrl": "",
  "tags": [
    {
      "name": "PIGMENT LOOSE HOOD ZIP-UP",
      "url": "https://bergwerk.cafe24.com/skin-skin2/product/pigment-loose-hood-zip-up/4844/category/1/display/3/",
      "x": 8,
      "y": 76
    }
  ]
}
```

`image`는 이 JSON 파일을 기준으로 한 상대 경로 또는 공개 HTTPS 이미지 URL입니다. 태그가 필요 없으면 `tags: []`로 둡니다. 개인정보, 비공개 계정 사진, 허락받지 않은 사진을 공개 저장소에 올리지 않습니다. 인스타그램 링크 자체는 임베드나 자동 동기화가 아닙니다.

Feed: https://raw.githubusercontent.com/seoraksanredcrayfish/bergwerk-web-assets/main/reviews/reviews.json
Test Home: https://bergwerk.cafe24.com/skin-skin2/index_test.html
