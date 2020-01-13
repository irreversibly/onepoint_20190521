CDM, 어디까지 가봤니?

- CDM에 대한 개괄적 소개
  - 미국의 sentinel CDM
    - 한국과 서로 다른 의료시스템
    - CDM에 들어와 있는 데이터파트너 들 중에서는 보험회사가 포함되어 있음. 
    - 병원이 데이터 파트너로 들어와 있는 경우도 있음
    - Sentinel Initiative에서는 데이터파트너들에게 데이터 유지 비용을 지급하고 있음.
  - OMOP CDM
    - ATLAS라는 web-tool을 통해 클릭클릭하면 코호트 추출 및 분석이 가능하도록 만들었음
    - User friendly
    - 이후 분석 등도 R packages 등에 대한 일부의 수정 등을 통해 복잡한 통계적 분석이 가능
    - 연구 욕심이 있는, bio-informatics에 익숙하지 않은 medical experties 들에게 환상적으로 보임
      Sentinel CDM과 대비되는 특징
    - Cohort를 추출하기 위한 특성들. 최상위 값들로 설정해야 loss되는 부분이 적을 수 있음

- 2016년... 
  - CDM 관련 과제를 시작
  - CDM model을 design하는 과정.. 사실은 미국 sentinel CDM copy
  - 각각 table 및 field 값들을 어떻게 구성하면 되는지 define
  - CDM에 맞출려면 우리 병원 어느 데이터 값을 mapping하면 되는지 확인
    - EMR을 뒤져가면서 어디에 있는지 확인
    - 전산팀에 문의
    
  - CBNUH CDM 구축... 처음에는 타원 의료정보학 교실 도움으로 CDM을 구축
  - CBNUH -> CDM 자료 conversion을 하기 위한 data mapping 작업
  - 이후 과정에는 수동적으로 참여하게 됨
  
- 2017년
  - 의료정보팀으로 부터 받은 자료를 CDM 모델에 맞춰 SQL 등을 통해 converting을 시도.
  - 한계가 많았음
  
- 2019년
  - 한국의약품안전관리원 수의계약 과제 진행
  - CDM을 재구축
  - 전산팀으로 부터 자료를 받았고
  - Python으로 데이터 cleasing을 하고
  - CDM format에 맞춰 postgresql로 loading하고
  - 중간중간 안되는 부분들을 googling하면서 바꾸고
  - 잘안되는 것들은 psql 등 command 등을 통해서 upload 진행
  - R 코드를 짜고,
  - 중간에 cohort 추출이 안되는 부분들은 다시 데이터를 들여다 보고, 오류가 어디에 있는지 확인해서 자료 추출을 처음부터 다시 하게 됨
  - distributed analysis를 위해 타원 담당자들과의 communication
    - 나는 의료전문가 + 초급 프로그래머 vs. 상대방은 중급 프로그래머 but 의료지식-
    - 데이터를 실제 들어다보지 않으면 왜 오류가 났는지 확인하기 어려움
    - 실제로 오류 코드는 상당히 많이 남
     
 
- 아직 못가본 부분들
  - OMOP CDM Atlas install 
  - 건보 data OMOP CDM 변환 및 atlas installation
  - 약물부작용 관련 CDM 구축 및 다기관 확장 (아직 없음)
  - 약물 유전체 관련 CDM 구축 현황 (아직 없음)
  - 비정형 데이터를 CDM 기준에 맞춰 converting (이미 하고 있음)
  
- 내가 한 삽질들이 어떤 의미가 있을까?
  - 잘 돌아가는 것 같지만.. 각 부문들끼리 연결고리가 약함. 과제 책임자 - data sceientist - 연구자.. 이건 이전부터 있어왔던 문제고 CDM을 구축했다고 해결되는 문제는 아님
  - 아주 perfect하게 구축을 하고 각 영역의 사람들은 자기가 할일만 정확히 하면 되도록 구축이 되면 좋겠지만.. 실제로 이렇게 구축된 기관이 있을지 잘 모그렜음
  - 적어도 나는 어느 부분이 안될 것인지.. 필요할 경우 어느 부분을 수정하면 될지 알고 있음 ㅋㅋ
  - 천천히 programming skill이 늘고 있음
  
  
  
- CDM 관련 논쟁 point

  - CDM의 효용성에 대한 논의는 해당 국가의 의료정보시스템에 많은 영향을 받을 수 있음
  

  - CDM은 infra임. infra 위에 훌륭한 집을 짓기 위한 tool이 필요
    - OMOP CDM + ATLAS web 분석 tool
    - Sentinel CDM + SAS 기반 analytic tool + 지속적인 질관리
  
  - Data quality assessment를 위한 tool이 필요
    - OMOP CDM: Achilles
    - Sentinel CDM: 기관별 data Q&A tool 제공 및 모니터링을 통한 feedback
    - 최근 CDM이 양적 팽창을 많이 했는데, 질적인 level에서 적절한지 확인 필요
    
  - 어떤시긍로 
CDM은 only infra
다음 문제는 어떻게 data clearing을 할 것인지?
데이터 관리를 어떻게 할 것인지?
데이터 분석을 어떻게 할 것인지?




