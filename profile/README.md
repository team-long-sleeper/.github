![title](../images/title.png)

한 해를 함께한 소중한 순간들을 기록하고, 연말에 친구·장소·태그별 통계로 회고할 수 있는 에피소드 기록 웹 앱 <br/>
새해를 맞아 다가올 일들을 기대하면서도 지난 한 해를 곱씹어볼 수 있길 바라는 마음에서 시작했습니다. <br/>
(그래서 happy ~~new year~~ last year closing 입니다, 추억 연말결산! 🌅)

### fe tech stack
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query_v5-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-FF8400?style=for-the-badge&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![NextAuth.js](https://img.shields.io/badge/NextAuth-000000?style=for-the-badge&logo=auth0&logoColor=white)
![kakao_login](https://img.shields.io/badge/kakao-login-FFCD00?style=for-the-badge&logo=kakao&logoColor=FFCD00)
![kakao_map](https://img.shields.io/badge/kakao-map-FFCD00?style=for-the-badge&logo=kakao&logoColor=FFCD00)

### be tech stack
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white)


### infra
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)
![AWS_EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logoColor=white)
![github_actions](https://img.shields.io/badge/github_actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)


<br/>
<br/>

# features

- 사용자는 날짜<span style="color: orangered;">&ast;</span>, 장소<span style="color: orangered;">&ast;</span>, 제목<span style="color: orangered;">&ast;</span>, 설명, 태그, 사진<span style="color: orangered;">&ast;</span>, 친구 정보로 '에피소드'를 작성할 수 있습니다. (<span style="color: orangered;">&ast;</span>필수 항목)
- 메인 페이지의 'episodes' 탭에서는 작성된 에피소드들을 카드 형태로 볼 수 있고,
- 'sum up' 탭에서는 에피소드들의 통계를 확인할 수 있습니다.
- 하루에 하나의 에피소드 작성을 best practice로 보고있습니다.
<br/>
<br/>

# architecture

![architecture](../images/architecture.png)


<br/>
<br/>

# database

```mermaid
  erDiagram
      User ||--o{ OAuthAccount : "has"
      User ||--o{ Contact : "owns"
      User ||--o{ Contact : "linkedUser"
      User ||--o{ Friendship : "user"
      User ||--o{ Friendship : "friend"
      User ||--o{ RefreshSession : "has"
      User ||--o{ Episode : "owns"
      User ||--o{ PlaceFavorite : "has"
      User ||--o{ Tag : "owns"

      Episode ||--o{ EpisodeMate : "has"
      Contact ||--o{ EpisodeMate : "in"

      Episode ||--o{ EpisodePicture : "has"
      Episode ||--o{ EpisodeTag : "tagged"
      Tag ||--o{ EpisodeTag : "tags"

      Place ||--o{ Episode : "location"
      Place ||--o{ PlaceFavorite : "favorited"
```

<br/>
<br/>

# screenshots 

### main page
<img src="../images/main-episodes.png" width="48%" />
<img src="../images/main-sumup.png" width="48%" />

<br/>

### write page
<img src="../images/write-page.png" width="48%" />
<img src="../images/kakao-map.png" width="48%" />
<img src="../images/add-friends.png" width="48%" />


