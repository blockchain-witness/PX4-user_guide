# 실리콘 에라타

이 페이지에는 Pixhawk 보드 시리즈에 사용된 타사 부품(마이크로 컨트롤러, 센서 등)의 실리콘(하드웨어) 에라타에서 알려진 문제가 나열되어 있습니다. 실리콘 오류의 유형에 따라, 이러한 오류들은 소프트웨어에서 수정될 수 없으며 특정한 제한을 가할 수 있다.

## FMUV2/ 픽쇼크 실리콘 에라타

### STM32F427VIT6 (errata) 

플래시 뱅크 2 및 최대 속도 USB 장치 전용.

USB 데이터 라인 중 하나인 PA12에서 작업이 진행되는 동안 2차 플래시 뱅크에 액세스할 때 최대 2차 개정판(리비전 3은 영향을 받지 않음)은 오류/데이터 손상을 일으킬 수 있습니다. 플래시 뱅크 #2를 사용하지 않는 것 외에는 이에 대한 해결 방법/소프트웨어 해결 방법이 없습니다. 장치를 프로그래밍하려면 USB가 필요하기 때문에 실리콘 리비전 < rv3으로 제작된 픽사는 마이크로프로세서의 2MB 플래시 중 최대 1MB만 사용할 수 있습니다

:::tip
The errata is fixed in later versions, but this may not be detected if you are using an older bootloader. See [Firmware > FMUv2 Bootloader Update](../config/firmware.md#bootloader) for more information.
:::

## FMU- 픽쇼크 실리콘 얼라타

No known issues.