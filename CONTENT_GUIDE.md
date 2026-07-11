# Portfolio content guide

현재 사이트는 About, Publications, Projects, CV 네 페이지만 노출하는 뼈대입니다.

| 내용                      | 수정할 파일                |
| ------------------------- | -------------------------- |
| 이름, 사이트 주소, 언어   | `_config.yml`              |
| 자기소개와 연구 관심 분야 | `_pages/about.md`          |
| 논문                      | `_bibliography/papers.bib` |
| 프로젝트                  | `_projects/*.md`           |
| 학력, 경력, 기술, 수상    | `_data/cv.yml`             |
| 이메일과 외부 프로필      | `_data/socials.yml`        |

배포 전에 `_config.yml`의 `url`, `baseurl`, `first_name`, `last_name`과 `scholar` 이름을 실제 값으로 바꾸세요.

GitHub에 올릴 때는 본인 저장소를 `origin`으로 추가하세요. 공식 al-folio 저장소는 업데이트 확인용 `upstream`으로 연결되어 있습니다.
