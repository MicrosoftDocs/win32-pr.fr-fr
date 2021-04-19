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
# <a name="updateimpactlevel-enumeration"></a>Énumération UpdateImpactLevel

Indique un impact élevé, moyen ou faible sur un appareil exécutant un système d’exploitation obsolète. Cette énumération est généralement utilisée par les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , qui sont à son tour imbriquées dans le [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) retourné à partir de [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Aucun**
</dt> <dd>

Il n’y a aucun impact prévisible sur votre appareil. Cela peut être dû au fait que l’appareil est à jour ou qu’il n’est pas à jour, car l’appareil respecte ses Windows Update pour les périodes de report d’entreprise, ou est obsolète, mais n’a pas encore atteint le seuil **daysOutOfDate** pour atteindre un niveau d’impact plus élevé.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ bas**
</dt> <dd>

L’appareil n’exécute pas le système d’exploitation le plus récent, mais dispose d’une mise à jour récente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Moyenne**
</dt> <dd>

L’appareil exécute le système d’exploitation le plus récent, mais une mise à jour est modérément récente.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ élevé**
</dt> <dd>

L’appareil n’est plus à jour pendant une longue période. Ce périphérique peut présenter des failles de sécurité et il manque peut-être des correctifs importants qui permettent à Windows de s’exécuter mieux. Quand un appareil exécute une version de Windows qui n’est plus prise en charge, **UpdateImpactLevel \_ High** est toujours retourné.

</dd> </dl>

## <a name="remarks"></a>Notes

Quand [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) est appelé, une structure [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) est retournée. Au sein de la structure se trouve un **assessmentForCurrent** et **assessmentForUpToDate**. Il s’agit de structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) . Les deux membres ont une énumération **UpdateImpactLevel** , qui indique un impact élevé, moyen, faible ou non pour un appareil exécutant un système d’exploitation obsolète. Ces niveaux sont déterminés par la valeur de **daysOutOfDate**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                   |
| MIDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




