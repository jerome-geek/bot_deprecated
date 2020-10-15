# Bot Datbase

1. `daily_craw`: 종목별 일별 금융 거래 데이터를 저장하는 데이터베이스
2. `min_craw`: 종목별 분별 금융 거래 데이터를 저장하는 데이터베이스
3. `daily_buy_list`
   - 일자 별로 상장된 모든 종목들의 금융 데이터를 저장
   - 주식 종목 리스트 저장
      1. `stock_item_all`: 코스피, 코스닥, 코넥스 모든 종목을 저장하는 테이블
      2. `stock_kospi`: 코스피 종목 리스트 테이블
      3. `stock_kosdaq`: 코스닥 종목 리스트 테이블
4. `jackbot1_imi1`: 모의 투자 데이터베이스
   1. `all_item_db`: 종목 거래 이력 테이블
   2. `jango_data`: 일별 수익률 정산 테이블
   3. `possessed_item`: 현재 보유 중인 종목 리스트 테이블
   4. `setting_data`: 봇 옵션 관리 및 DB 업데이트 일자 관리 테이블

- 초기 database 생성 쿼리문 (collector_v3.py를 실행시키면 자동으로 아래 db가 없을 시 생성 되도록 코드가 수정 되었습니다.)

```sql
create database daily_craw;
create database min_craw;
create database daily_buy_list;
```
