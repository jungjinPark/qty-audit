# qty-audit

조경 시설물 수량산출서(XLSX)에서 일부 항목을 점검하는 도구입니다.
할증률 확인 / 할증률 적용 정확도 / 단위중량 / 계산식 결과값

## 파일 구성
- `rules.yml`: 할증/계산/단위중량 검토 룰
- `audit.py`: 감사 실행 스크립트
- `input/`: 입력 엑셀 파일 폴더
- `output/`: 결과 리포트 폴더

## 설치
```bash
pip install openpyxl pandas pyyaml
```

## 실행
```bash
python audit.py input/파일.xlsx --rules rules.yml --outdir output
```

## 출력 결과
- `output/report.csv`: 오류 상세 목록
- `output/report.xlsx`
  - `Summary`: 오류 건수 집계
  - `Errors`: 오류 상세(행/셀/원인/severity/관련수식/차이)
