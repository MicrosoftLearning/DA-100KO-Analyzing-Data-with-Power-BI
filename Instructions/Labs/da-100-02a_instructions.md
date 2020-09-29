﻿

### 랩 02A

Power BI Desktop에서 데이터 준비

# 개요

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 Adventure Works 회사를 위한 Power BI Desktop 솔루션 개발을 시작합니다. 여기에는 원본 데이터에 연결하고, 데이터를 미리 보고, 데이터 미리 보기 기술을 사용하여 원본 데이터의 특성과 품질을 이해하는 것이 포함됩니다.

이 랩의 학습 내용은 다음과 같습니다.

* Power BI Desktop 열기

* Power BI Desktop 옵션 설정하기

* 원본 데이터에 연결합니다.

* 원본 데이터 미리 보기

* 데이터 미리 보기 기술을 사용하면 데이터를 더 잘 이해할 수 있습니다.

# 연습1: 데이터 준비

이 연습에서는 8개의 Power BI Desktop 쿼리를 만듭니다. 6개의 쿼리는 SQL Server에서 데이터를 소싱하고 2개는 CSV 파일에서 소싱합니다.

### 작업 1: Power BI Desktop 파일 저장

이 작업에서는 먼저 Power BI Desktop 파일을 저장합니다.

1. Power BI Desktop에서 **파일** 리본 탭을 클릭하여 배경 뷰를 엽니다.

2. **저장**을 선택합니다.

	![그림 13](Linked_image_Files/PowerBI_Lab02A_image1.png)

3. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

4. **파일 이름** 상자에 **영업 분석**을 입력합니다.

	![그림 14](Linked_image_Files/PowerBI_Lab02A_image2.png)

5. **저장**을 클릭합니다.

	![그림 17](Linked_image_Files/PowerBI_Lab02A_image3.png)

	*팁: 오른쪽 상단에 있는 **저장** 아이콘을 클릭하여 파일을 저장할 수도 있습니다*. 

	![그림 18](Linked_image_Files/PowerBI_Lab02A_image4.png)

### 작업 2: Power BI Desktop 옵션 설정하기

이 작업에서는 Power BI Desktop 옵션을 설정합니다.

1. Power BI Desktop에서 **파일** 리본 탭을 클릭하여 배경 뷰를 엽니다.

7. 왼쪽에서 **옵션 및 설정**을 선택한 다음 **옵션**을 선택합니다.

	![그림 1](Linked_image_Files/PowerBI_Lab02A_image5.png)

8. **옵션** 창의 왼쪽에 있는 **현재 파일** 그룹에서 **데이터 로드**를 선택합니다.

	![그림 5](Linked_image_Files/PowerBI_Lab02A_image6.png)

	*현재 파일의 **데이터 로드** 설정을 사용하면 모델링할 때 기본 동작을 결정하는 옵션의 설정을 허용합니다*.

9. **관계** 그룹에서는 선택한 두 옵션의 선택을 취소합니다. 

	![그림 7](Linked_image_Files/PowerBI_Lab02A_image7.png)

	*이 두 가지 옵션은 데이터 모델을 개발할 때 유용할 수 있지만 랩 환경을 지원하기 위해 비활성화되었습니다. **랩 03A**에서 관계를 만들 때 각 관계를 추가하는 이유를 알게 됩니다*.

10. **확인**을 클릭합니다.

	![그림 9](Linked_image_Files/PowerBI_Lab02A_image8.png)

11. Power BI Desktop 파일을 저장합니다.

### 작업 3: SQL Server로부터 데이터 받기

이 작업에서는 SQL Server 테이블을 기반으로 쿼리를 만듭니다.

1. **데이터** 그룹 안에 있는 **홈** 리본 탭에서 **SQL Server**를 클릭합니다.

	![그림 19](Linked_image_Files/PowerBI_Lab02A_image9.png)

13. **SQL Server 데이터베이스** 창의 **서버** 상자에 **localhost**를 입력합니다.

	![그림 21](Linked_image_Files/PowerBI_Lab02A_image10.png)

	*랩에서 **localhost**를 사용하여 SQL Server 데이터베이스에 연결합니다. 그러나 여러분 자신을 위한 솔루션을 만들 때 권장되는 방법은 아닙니다. 게이트웨이 데이터 소스가 **localhost**를 해결할 수 없기 때문입니다*.

14. **확인**을 클릭합니다.

	![그림 22](Linked_image_Files/PowerBI_Lab02A_image11.png)

15. 기본 인증은 **내 현재 자격 증명을 사용**하는 것입니다.

	![그림 23](Linked_image_Files/PowerBI_Lab02A_image12.png)

16. **연결**을 클릭합니다.

	![그림 25](Linked_image_Files/PowerBI_Lab02A_image13.png)

17. 암호화 지원에 대한 메시지가 표시되면 **확인**을 클릭합니다.

	![그림 27](Linked_image_Files/PowerBI_Lab02A_image14.png)

18.  **탐색기** 창에서 왼쪽에 있는 **AdventureWorksDW2020** 데이터베이스를 확장합니다.  

	***AdventureWorksDW2020** 데이터베이스는 **AdventureWorksDW2017** 샘플 데이터베이스를 기반으로 합니다. 이것은 과정 랩의 학습 목표를 지원하기 위해 수정되었습니다*.

	![그림 28](Linked_image_Files/PowerBI_Lab02A_image15.png)

19. **DimEmployee** 테이블을 선택하지만 체크하지 마십시오.

	![그림 29](Linked_image_Files/PowerBI_Lab02A_image16.png)

20. 오른쪽 창에 테이블의 미리 보기가 있습니다.

	*미리 보기를 사용하면 열과 행 샘플을 확인할 수 있습니다*.

21. 쿼리를 만들려면 다음 여섯 개의 테이블을 확인합니다.

	* DimEmployee

	* DimEmployeeSalesTerritory

	* DimProduct

	* DimReseller

	* DimSalesTerritory

	* FactResellerSales

22. 선택한 테이블의 데이터에 변환을 적용하려면 **데이터 변환**을 클릭합니다.

	*이 랩의 데이터를 변환하지는 않을 것입니다. 이 랩의 목적은 **파워 쿼리 편집기** 창에서 데이터를 탐색하고 프로파일링하는 것입니다*.

	![그림 30](Linked_image_Files/PowerBI_Lab02A_image17.png)

### 작업 4: SQL Server 쿼리 미리 보기

이 작업에서는 SQL Server 쿼리의 데이터를 미리 봅니다. 먼저 데이터에 대한 관련 정보를 알아봅니다. 또한 열 품질, 열 분포 및 열 프로필 도구를 사용하여 데이터를 이해하고 데이터 품질을 평가합니다.

1. **Power Query 편집기** 창의 왼쪽에 **쿼리** 창이 표시됩니다.

	![그림 31](Linked_image_Files/PowerBI_Lab02A_image18.png)

	* **쿼리** 창에는 선택한 각 테이블에 대한 쿼리가 하나 있습니다*.

24. 첫 번째 쿼리 **DimEmployee** 를 선택합니다.

	![그림 33](Linked_image_Files/PowerBI_Lab02A_image19.png)

	***DimEmployee** 테이블에는 각 직원에 대해 하나의 행이 저장됩니다. 행의 하위 집합은 영업 직원을 나타내며, 이는 개발할 모델과 관련이 있습니다*.

25. 왼쪽 아래의 상태 표시줄에는 테이블 통계에 33개의 열과 296개의 행이 있습니다.

	![그림 36](Linked_image_Files/PowerBI_Lab02A_image20.png)

26. 데이터 미리 보기 창에서 가로로 스크롤하여 모든 열을 검토합니다.

27. 마지막 다섯 열에는 **테이블** 또는 **값** 링크가 포함되어 있습니다.

	*이 다섯 개의 열은 데이터베이스 내 다른 테이블과의 관계를 나타냅니다. 테이블을 함께 조인하는 데 사용할 수 있습니다. **랩 03A**에서 테이블에 조인합니다*.

28. 열 품질을 평가하려면 **데이터 미리 보기** 그룹 안에 있는 **뷰 ** 리본 탭에서 **열 품질**을 체크합니다.

	![그림 35](Linked_image_Files/PowerBI_Lab02A_image21.png)

	*열 품질을 사용하면 유효, 오류 또는 빈 값의 백분율을 쉽게 확인할 수 있습니다*.

29. **위치** 열(6번째 마지막 열)의 경우 행의 94%가 비어 있습니다(null).

	![그림 38](Linked_image_Files/PowerBI_Lab02A_image22.png)

30. 열 분포를 평가하려면 **데이터 미리 보기** 그룹 안에 있는 **뷰** 리본 탭에서 **열 분포**를 체크합니다.

	![그림 40](Linked_image_Files/PowerBI_Lab02A_image23.png)

31. **위치** 열을 다시 검토하면 네 개의 고유한 값과 하나의 고유 값이 있음을 알 수 있습니다.

32. **EmployeeKey**(첫 번째) 열에 대한 열 분포를 검토합니다. 296개의 고유한 값, 296개의 고유 값이 있습니다.

	![그림 43](Linked_image_Files/PowerBI_Lab02A_image24.png)

	*고유 카운트가 같으면 열에 고유 값이 포함되어 있음을 의미합니다. 모델링할 때 일부 테이블에 고유한 열이 포함되어 있는 것이 중요합니다. 이들은 **Lab 04A**에서 수행할 일대다 관계를 생성하는 데 사용됩니다*.

33. **쿼리** 창에서 **DimEmployeeSalesTerritory** 쿼리를 선택합니다.

	![그림 44](Linked_image_Files/PowerBI_Lab02A_image25.png)

	***DimEmployeeSalesTerritory** 테이블은 각 직원과 그들이 관리하는 영업 지역 분야별로 하나의 행을 저장합니다. 이 테이블은 많은 지역을 한 명의 직원과 연결하는 작업을 지원합니다. 일부 직원은 하나, 둘 또는 더 많은 지역을 관리합니다. 이 데이터를 모델링할 때 **랩 05A**에서 수행할 다대다 관계를 정의해야 합니다*.

34. **쿼리** 창에서 **DimProduct** 쿼리를 선택합니다.

	![그림 46](Linked_image_Files/PowerBI_Lab02A_image26.png)

	***DimProduct** 테이블에는 회사에서 판매하는 제품당 하나의 행이 포함되어 있습니다*.

35. 가로로 스크롤하여 마지막 열을 표시합니다.

36. **DimProductSubcategory** 열에 주목하십시오.

	*다음 랩에서 이 쿼리에 변환을 추가하면 **DimProductSubcategory** 열을 사용하여 테이블을 조인합니다*.

37. **쿼리** 창에서 **DimReseller** 쿼리를 선택합니다.

	![그림 49](Linked_image_Files/PowerBI_Lab02A_image27.png)

	***DimReseller** 테이블에는 재판매인당 하나의 행이 있습니다. 재판매인은 Adventure Works 제품을 판매, 배포 또는 부가가치를 추가합니다*.

38. 열 값을 보려면 **뷰** 리본 탭에 있는 **데이터 미리 보기** 그룹 내부에서 **열 프로필**을 선택합니다.

	![그림 41](Linked_image_Files/PowerBI_Lab02A_image28.png)

39. **BusinessType** 열 헤더를 선택합니다.

40. 데이터 미리 보기 창 아래에 새 창이 열립니다.

41. 열 통계 및 값 분포를 검토합니다.

42. 데이터 품질 문제 주의 사항: 웨어하우스에 대한 두 개의 레이블이 있습니다(**Warehouse,** 및 철자가 틀린 **Ware House**).

	![그림 51](Linked_image_Files/PowerBI_Lab02A_image29.png)

43. **웨어 하우스** 바 위에 커서를 가리키면 이 값이 있는 5개의 행이 보입니다.

	*다음 랩에서는 변환을 적용하여 이 다섯 행의 레이블을 다시 지정합니다*.

44. **쿼리** 창에서 **DimSalesTerritory** 쿼리를 선택합니다.

	![그림 52](Linked_image_Files/PowerBI_Lab02A_image30.png)

	***DimSalesTerritory** 테이블에는 **기업 HQ**(본사)를 포함하여 영업 지역당 하나의 행이 포함되어 있습니다. 지역은 국가에 할당되고 국가는 그룹에 할당됩니다. **랩 04A**에서 지역, 국가 또는 그룹 수준에서 분석을 지원하는 계층 구조를 만듭니다*.

45. **쿼리** 창에서 **FactReplayerSales** 쿼리를 선택합니다.

	![그림 54](Linked_image_Files/PowerBI_Lab02A_image31.png)

	* **FactResellerSales** 테이블에는 판매 주문 라인당 하나의 행이 포함되어 있으며, 하나의 판매 주문에는 하나 이상의 품목이 포함되어 있습니다*.

46. **TotalProductCost** 열의 열 품질을 검토하면 행의 8%가 비어 있음을 알 수 있습니다.

	![그림 63](Linked_image_Files/PowerBI_Lab02A_image32.png)

	***TotalProductCost** 열 값을 누락하는 것은 데이터 품질 문제입니다. 문제를 해결하려면 다음 랩에서 **DimProduct** 테이블에 저장된 제품 표준 비용을 사용하여 누락된 값을 채우기 위해 변환을 적용합니다.*

### 작업 5: CSV 파일에서 데이터 가져오기

이 작업에서는 CSV 파일을 기반으로 쿼리를 생성합니다.

1. 새 쿼리를 추가하려면 **파워 쿼리 편집기** 창에서 **새 쿼리** 그룹 내에 있는 **홈** 리본 탭에서 **새 소스** 아래쪽 화살표를 클릭한 다음, **텍스트/CSV**를 선택합니다.

	![그림 70](Linked_image_Files/PowerBI_Lab02A_image33.png)

48. **열기** 창에서 **D:\DA100\Data** 폴더로 이동하여 **ResellerSalesTargets.csv**파일을 선택합니다.

49. **열기**를 클릭합니다.

50. **ResellerSalesSalesTargets.csv** 창에서 데이터 미리 보기를 확인합니다.

51. **확인**을 클릭합니다.

	![그림 71](Linked_image_Files/PowerBI_Lab02A_image34.png)

52. **쿼리** 창에서 **ResellerSalesTargets** 쿼리가 추가됩니다.

	![그림 72](Linked_image_Files/PowerBI_Lab02A_image35.png)

	***ResellerSalesTargets** CSV 파일에는 영업 직원당 연간 하나의 행이 포함되어 있습니다. 각 행은 12개의 월별 판매 목표를 기록합니다(천 단위로 표시). Adventure Works 회사의 비즈니스 연도는 7월 1일부터 시작됩니다*.

53. 빈 값이 포함된 열이 없습니다.

	*월별 판매 목표가 없는 경우 대신 하이픈 문자가 저장됩니다*.

54. 열 이름의 왼쪽에 있는 각 열 헤더 안의 아이콘을 검토합니다.

	![그림 74](Linked_image_Files/PowerBI_Lab02A_image36.png)

	*아이콘은 열 데이터 형식을 나타냅니다. **123**은 정수이며 **ABC**는 텍스트입니다*.

	*다음 랩에서는 세 개의 열로 구성된 다른 모양의 결과를 달성하기 위해 많은 변환을 적용합니다. **날짜**, **EmployeeKey** 및 **TargetAmount***.

### 작업 6: CSV 파일에서 추가 데이터 얻기

이 작업에서는 다른 CSV 파일을 기반으로 추가 쿼리를 만듭니다.

1. 이전 작업의 단계를 사용하여 **D:\DA100\Data**\**ColorFormats.csv** 파일을 기반으로 쿼리를 만듭니다. 

	![그림 75](Linked_image_Files/PowerBI_Lab02A_image37.png)

	* **ColorFormats** CSV 파일에는 제품 색상당 하나의 행이 포함되어 있습니다.  각 행은 HEX 코드를 기록하여 배경 및 글꼴 색상 형식을 지정합니다. 다음 랩에서는 이 데이터를 **DimProduct** 쿼리 데이터와 통합합니다*.

### 완료

이 작업에서는 랩을 완료합니다.

1. 리본 **보기** 탭의 **데이터 미리 보기** 그룹 내부에서 다음 세 가지 데이터 미리 보기 옵션을 선택 취소합니다:

	* 열 품질

	* 열 분포

	* 열 프로필

	![그림 76](Linked_image_Files/PowerBI_Lab02A_image38.png)

57. **파일** 백스테이지 뷰에서 Power BI Desktop 파일을 저장하려면  **저장**을 선택합니다.   

	![그림 77](Linked_image_Files/PowerBI_Lab02A_image39.png)

58. 쿼리를 적용하라는 메시지가 표시되면 **나중에 적용**을 클릭합니다.

	![그림 86](Linked_image_Files/PowerBI_Lab02A_image40.png)

	*쿼리를 적용하면 데이터가 데이터 모델에 로드됩니다. 우선 많은 변환이 적용되어야 하므로 아직 준비되지 않았습니다.*

59. Power BI Desktop을 열어 둡니다.

	*다음 랩에서는 쿼리에 다양한 변환을 적용한 다음, 쿼리를 적용하여 데이터 모델에 로드합니다.*