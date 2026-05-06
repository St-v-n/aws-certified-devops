# Falco EKS Add-on

## What is Falco?
Kernel 이벤트와 시스템 활동을 실시간으로 분석해, 비정상 행위나 보안 위반으로 즉각 탐지할 수 있는 Opensource Solution.

25년 6월부터 EKS Add-on으로 무료 설치 가능.

## Expected Effect
Kubernetes 행위 탐지로 불필요한 작업 발생 시 Alert을 통한 작업 통제 및 작업 이력은 확인이 가능하지만 가시성이 떨어져 이슈 발생 시 해당 부분을 참조하기 어려움

컨테이너 내 eBPF 감시

kubectl 이상 작업(예상하지 않은 작업)에 대한 Noti로 팀원에게 작업 공유가 원할해짐

## How it works

 - Parsing the Linux syscalls from the kernel at runtime
 - Asserting the stream against a powerful rules engine
 - Alerting when a rule is violated

### Architecture

## Procedure
