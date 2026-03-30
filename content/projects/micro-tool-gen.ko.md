---
title: "마이크로 도구 생성기"
date: 2026-03-01
summary: "자연어 설명으로 단일 목적 웹 도구를 자동 생성하는 AI 도구."
tags: ["AI", "Claude API", "Python", "HTML"]
categories: ["AI 도구"]
weight: 1
---

## 개요

자연어 설명을 입력하면 독립적인 단일 목적 웹 도구를 생성하는 AI 도구입니다. 각 도구는 독립형 HTML 파일로 출력되며, 서버나 의존성 없이 바로 사용할 수 있습니다.

## 작동 방식

1. 필요한 도구를 자연어로 설명
2. AI가 CSS, JavaScript가 포함된 완전한 HTML 도구를 생성
3. 브라우저에서 파일을 열면 바로 작동

## 기술 스택

- **백엔드:** Python, FastAPI
- **AI:** Claude API
- **출력:** 독립형 HTML/CSS/JS 파일
