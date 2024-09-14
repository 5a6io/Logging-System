# Cloudwave Project
## Use Skill
- kubernetes 1.30.0
- helm 3.15.4

## Use Version
- Fluent-bit:3.1.6➡️helm repo fluent
- Elasticsearch:7.17.0
- Kibana:7.17.0
- Loki➡️helm repo grafana
- Promtail➡️helm repo grafana

## EFK vs. PLG
|| **EFK** | **PLG** |
|:--------:|:---------------:|:---------------:|
| 로그 수집 | Fluent-bit/Fluentd | Promtail |
| 로그 저장 | Elasticsearch | Loki |
| 로그 검색 | Kibana | Grafana |
| 로그 쿼리 언어 | Elasticsearch Query DSL | LogQL |
| 설치 및 구성의 복잡성 | 일부 복잡 | 상대적으로 단순 |
| 분산 아키텍처 지원 | 지원 | 지원 |
| 경고 및 알림 기능 | Watcher(X-Pack) or Third-party Integration | Alermanager (Prometheus) |
| 데이터 볼륨 처리 | 대량 처리 가능 | 대량 처리 가능 |
| 확장성 | 수평적으로 확장 | 수평적으로 확장. 읽기 및 쓰기 경로 분리. MSA에서 사용. |

## Conclusion
### EFK
- 분석, 시각화 및 쿼리를 위한 최고의 유연성과 풍부한 기능을 제공하는 다양한 용도로 사용 가능.
- ML 기능 탑재.
### PLG
- 메타데이터 발견 메커니즘 때문에 Kubernetes 생태계에서 유용.
- 시계열 기반 데이터를 그라파나와 로그로 쉽게 상호 연관시켜 관찰 가능.
