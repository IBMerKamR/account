---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account owner, user roles, manage account, orgs, spaces

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# 조직 및 영역 업데이트
{: #orgupdates}

{{site.data.keyword.Bluemix}} 계정 소유자 또는 조직 관리자는 조직 레벨 및 영역 레벨에서 관리 태스크를 수행할 수 있습니다. 이러한 태스크에는 조직 또는 영역 이름 바꾸기, Cloud Foundry 사용자 역할 지정 또는 업데이트, 도메인 관리 및 조직 할당량 세부사항 보기가 포함됩니다.
{:shortdesc}

**관리 > 계정**으로 이동하여 **Cloud Foundry 조직**을 선택하십시오.

한 번에 한 조직만의 리소스를 볼 수 있습니다. 여러 조직의 구성원인 경우에는 콘솔 메뉴 표시줄의 사용자 계정 환경 설정 링크에서 조직을 전환할 수 있습니다.
{: tip}

  * 조직의 이름을 변경하려면 이름을 변경하고자 하는 조직에 대해 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **이름 바꾸기**를 선택하십시오.
    {: #orgrename}

    변경사항은 조직의 모든 사용자에게 적용됩니다.

  * 조직을 삭제하려면 [지원](/docs/get-support?topic=get-support-getting-customer-support)에 문의하십시오.
    {: #deleteorgs}

    조직을 삭제하면 조직 내 모든 영역과 리소스도 삭제됩니다. 이 조치는 되돌릴 수 없습니다.

  * 영역을 삭제하려면 영역이 지정된 조직을 선택하십시오. 그리고 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **삭제**를 선택하십시오.

    영역을 삭제하면 포함된 모든 리소스 및 사용자도 삭제됩니다.

  * 조직 레벨에서 사용자 역할을 편집하려면 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **사용자**를 선택하십시오.
    {: #listmembers}

    사용자 권한을 수정하려는 방법에 따라 특정 역할에 대한 선택란을 선택하거나 선택 취소하십시오. 조직 레벨에서 지정할 수 있는 역할은 관리자, 청구 관리자 및 감사자입니다. 자세한 정보는 [Cloud Foundry 역할](/docs/iam?topic=iam-cfaccess#cfroles)을 참조하십시오.

  * 특정 영역의 사용자 역할을 편집하려면 영역이 지정된 조직을 클릭하십시오. 그리고 영역의 이름을 클릭하십시오.

    사용자 권한을 수정하려는 방법에 따라 특정 역할에 대한 선택란을 선택하거나 선택 취소하십시오. 영역 레벨에서 지정할 수 있는 역할은 관리자, 개발자 및 감사자입니다. 자세한 정보는 [Cloud Foundry 역할](/docs/iam?topic=iam-cfaccess#cfroles)을 참조하십시오.

  * 도메인을 관리하려면 개별 조직에 대해 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **도메인**을 선택하십시오.
    {: #managedomains}

    계정 소유자나 조직 관리자는 조직 및 해당 영역 내에 빌드된 애플리케이션에 대해 시스템 도메인을 보고 사용자 정의 도메인을 추가할 수 있습니다. 영역 관리자인 경우, 이 페이지는 영역에 지정된 도메인의 읽기 전용 목록을 표시합니다.

    사용자 정의 도메인을 추가하는 경우 사용자 정의 도메인을 분석하여 {{site.data.keyword.Bluemix_notm}} 시스템 도메인을 가리키도록 DNS 서버를 구성해야 합니다. 이런 방법으로 {{site.data.keyword.Bluemix_notm}}가 사용자 정의 도메인에 대한 요청을 수신하면 이 요청이 앱으로 적절하게 라우팅됩니다. 시스템 도메인은 항상 영역에 사용할 수 있으며 사용자 정의 도메인도 영역에 할당할 수 있습니다. 영역에서 작성된 앱은 해당 영역에 대해 나열된 임의의 도메인을 사용할 수 있습니다. 사용자 정의 도메인을 작성하고 사용하는 데 관한 자세한 정보는 [도메인 관리](/docs/apps?topic=creating-apps-update-domain)를 참조하십시오.

  * 조직에 할당된 할당량을 관리하려면 개별 조작에 대해 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **할당량**을 선택하십시오.
    {: #managequota}

    여기에서 플랜 세부사항 및 서비스 수, 메모리 양, 앱 수에 대한 할당량 세부사항을 볼 수 있습니다. 할당량은 조직이 작성될 때 지정된 조직의 리소스 한계를 나타냅니다. 조직이 사용할 수 있는 리소스는 무료 계정 또는 청구 가능 계정이 있는지 여부에 따라 다릅니다. 조직 내의 영역에 포함된 애플리케이션이나 서비스는 할당된 할당량의 사용에 기여합니다.

    조직에 할당된 할당량을 변경하려면 지원 케이스를 작성해야 합니다. 자세한 정보는 [지원 케이스 관련 작업](/docs/get-support?topic=get-support-open-case)을 참조하십시오.

    각 위치에 대해 영역 레벨에서 할당량 세부사항을 보려면 개별 조직에 대해 조치 아이콘 ![조치 아이콘](../icons/action-menu-icon.svg)을 클릭하고 **할당량**을 선택하십시오. 그리고 알맞게 각 행을 펼치십시오.
