---
description: Indique un impact élevé, moyen ou faible sur un appareil exécutant un système d’exploitation obsolète.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Énumération UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544237"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="a6b24-103">Énumération UpdateImpactLevel</span><span class="sxs-lookup"><span data-stu-id="a6b24-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="a6b24-104">Indique un impact élevé, moyen ou faible sur un appareil exécutant un système d’exploitation obsolète.</span><span class="sxs-lookup"><span data-stu-id="a6b24-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="a6b24-105">Cette énumération est généralement utilisée par les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , qui sont à son tour imbriquées dans le [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) retourné à partir de [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span><span class="sxs-lookup"><span data-stu-id="a6b24-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b24-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6b24-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="a6b24-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="a6b24-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6b24-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Aucun**</span><span class="sxs-lookup"><span data-stu-id="a6b24-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="a6b24-109">Il n’y a aucun impact prévisible sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="a6b24-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="a6b24-110">Cela peut être dû au fait que l’appareil est à jour ou qu’il n’est pas à jour, car l’appareil respecte ses Windows Update pour les périodes de report d’entreprise, ou est obsolète, mais n’a pas encore atteint le seuil **daysOutOfDate** pour atteindre un niveau d’impact plus élevé.</span><span class="sxs-lookup"><span data-stu-id="a6b24-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="a6b24-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ bas**</span><span class="sxs-lookup"><span data-stu-id="a6b24-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="a6b24-112">L’appareil n’exécute pas le système d’exploitation le plus récent, mais dispose d’une mise à jour récente.</span><span class="sxs-lookup"><span data-stu-id="a6b24-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="a6b24-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Moyenne**</span><span class="sxs-lookup"><span data-stu-id="a6b24-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="a6b24-114">L’appareil exécute le système d’exploitation le plus récent, mais une mise à jour est modérément récente.</span><span class="sxs-lookup"><span data-stu-id="a6b24-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="a6b24-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ élevé**</span><span class="sxs-lookup"><span data-stu-id="a6b24-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="a6b24-116">L’appareil n’est plus à jour pendant une longue période.</span><span class="sxs-lookup"><span data-stu-id="a6b24-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="a6b24-117">Ce périphérique peut présenter des failles de sécurité et il manque peut-être des correctifs importants qui permettent à Windows de s’exécuter mieux.</span><span class="sxs-lookup"><span data-stu-id="a6b24-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="a6b24-118">Quand un appareil exécute une version de Windows qui n’est plus prise en charge, **UpdateImpactLevel \_ High** est toujours retourné.</span><span class="sxs-lookup"><span data-stu-id="a6b24-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6b24-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a6b24-119">Remarks</span></span>

<span data-ttu-id="a6b24-120">Quand [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) est appelé, une structure [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) est retournée.</span><span class="sxs-lookup"><span data-stu-id="a6b24-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="a6b24-121">Au sein de la structure se trouve un **assessmentForCurrent** et **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="a6b24-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="a6b24-122">Il s’agit de structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) .</span><span class="sxs-lookup"><span data-stu-id="a6b24-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="a6b24-123">Les deux membres ont une énumération **UpdateImpactLevel** , qui indique un impact élevé, moyen, faible ou non pour un appareil exécutant un système d’exploitation obsolète.</span><span class="sxs-lookup"><span data-stu-id="a6b24-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="a6b24-124">Ces niveaux sont déterminés par la valeur de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="a6b24-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b24-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6b24-125">Requirements</span></span>



| <span data-ttu-id="a6b24-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6b24-126">Requirement</span></span> | <span data-ttu-id="a6b24-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6b24-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b24-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6b24-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b24-129">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6b24-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a6b24-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6b24-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b24-131">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6b24-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6b24-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="a6b24-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6b24-133"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6b24-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




