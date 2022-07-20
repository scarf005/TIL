---
tags:
  - 파이썬
  - 깃허브
  - Git
---

# `actions/setup-python`을 효율적으로 쓰자

## 예제 파일

[.github/workflows/ci.yml](https://github.com/scarf005/til/blob/main/.github/workflows/ci.yml)

```yaml
---8<---- ".github/workflows/ci.yml"
```

## [actions/](https://github.com/actions) 계정은

- 깃허브에서 기본 제공해주는 워크플로우 확장 모음
- 유용하다

## `actions/setup-python`이란

- 파이썬 버전 설치를 쉽게 해준다
- 여러 파이썬 버전 관리를 할 수 있다

## 사실 `github action` 컨테이너에는 파이썬이 이미 깔려있다

- [여기](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#supported-software)서 컨테이너별로 기본 설치된 프로그램 목록을 확인할 수 있다
- [우분투 컨테이너에 설치된 소프트웨어 비교](https://github.com/actions/virtual-environments/issues/5490)

`Ubuntu 20.04 LTS`
: - 기본 버전 `3.8.x`, 캐시 버전 [`2.7`, `3.6`, `3.7`, `3.8`, `3.9`, `3.10`]

`Ubuntu 22.04 LTS`
: 기본 버전 `3.10.x`, 캐시 버전 [`3.7`, `3.8`, `3.9`, `3.10`]

## 파이썬 의존성 캐시해놓기

```yaml
with:
  cache: pip
```

`pip` 의존성을 캐싱할 수 있다! 그밖에도 [`pipenv`나 `poetry`도 가능](https://github.com/actions/setup-python#caching-packages-dependencies)
