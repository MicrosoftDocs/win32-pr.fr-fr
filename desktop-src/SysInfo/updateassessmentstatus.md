---
description: Décrit comment mettre à jour le système d’exploitation sur un appareil.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Énumération UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: f4ece78c9593ab674a4198829c4e75612a9c4b337e17b3d2b6c5ed2fc19f42c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884305"
---
# <a name="updateassessmentstatus-enumeration"></a>Énumération UpdateAssessmentStatus

Décrit comment mettre à jour le système d’exploitation sur un appareil. **UpdateAssessmentStatus** est utilisé par les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) et [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , dans les membres **assessmentForCurrent**, **assessmentForUpToDate** et **securityStatus** . Une seule constante est retournée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Dernière version**
</dt> <dd>

Ce résultat dans **assessmentForCurrent** implique que l’appareil se trouve sur les dernières mises à jour de fonctionnalités et mise à jour de qualité disponibles pour cet appareil. Dans **assessmentForUpToDate**, ce résultat implique que l’appareil se trouve sur la dernière mise à jour de qualité pour la version de Windows qu’il est en cours d’exécution.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**
</dt> <dd>

La dernière mise à jour de la fonctionnalité n’a pas été installée en raison d’une restriction logicielle. Lorsqu’une restriction logicielle a été placée sur une mise à jour, la mise à jour n’est pas installée automatiquement. un utilisateur doit lancer automatiquement le téléchargement au sein de l’expérience utilisateur de la mise à jour. Cet État s’applique uniquement à **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**
</dt> <dd>

La dernière mise à jour de la fonctionnalité n’a pas été installée en raison d’une restriction matérielle. Lorsqu’une restriction matérielle a été placée sur une mise à jour, la mise à jour n’est pas applicable à l’appareil. Cet État s’applique uniquement à **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**
</dt> <dd>

L’appareil n’est pas dans la dernière mise à jour, car la mise à jour des fonctionnalités de l’appareil n’est plus prise en charge par Microsoft. Lorsque Microsoft arrête de prendre en charge une version de fonctionnalité, cet État est renvoyé pour **assessmentForCurrent** et **assessmentForUpToDate**.

> [!Note]  
> Lorsque **UpdateAssessmentStatus \_ NotLatestEndOfSupport** est retourné, le **UpdateImpactLevel** de l’évaluation est toujours **UpdateImpactLevel \_ élevé**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**
</dt> <dd>

L’appareil n’est pas sur la dernière mise à jour des fonctionnalités, car le train de maintenance de l’appareil limite la mise à jour de l’appareil à la dernière mise à jour de la fonctionnalité. Par exemple : si un appareil se trouve sur Current Branch for Business (CBB) et qu’une nouvelle mise à jour de fonctionnalité a été publiée pour Current Branch (CB), cette opération est retournée. Cet État s’applique uniquement à **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**
</dt> <dd>

la dernière mise à jour de la fonctionnalité n’a pas été installée en raison de la stratégie de report des mises à jour Windows Update pour les fonctionnalités d’entreprise de l’appareil. La détermination des **daysOutOfDate** prend en compte les stratégies de report. **daysOutOfDate** ne commence pas à s’incrémenter tant que la période de report n’a pas expiré. Cet État s’applique uniquement à **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**
</dt> <dd>

l’appareil n’est pas sur la dernière mise à jour de qualité en raison de la Windows Update de l’appareil pour la stratégie de report de mise à jour de qualité professionnelle. La détermination des **daysOutOfDate** prend en compte les stratégies de report. **daysOutOfDate** ne commence pas à s’incrémenter tant que la période de report n’a pas expiré.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**
</dt> <dd>

L’appareil n’est pas sur la dernière mise à jour des fonctionnalités, car l’appareil a des mises à jour de fonctionnalités suspendues. Le fait qu’un appareil soit mis en pause n’est pas pris en compte dans le calcul de **daysOutOfDate**. Cet État s’applique uniquement à **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**
</dt> <dd>

L’appareil n’est pas sur la dernière mise à jour de qualité, car l’appareil a des mises à jour qualité suspendues. Le fait qu’un appareil soit mis en pause n’est pas pris en compte dans le calcul de **daysOutOfDate**. **daysOutOfDate** ne détermine pas si un appareil est mis en pause dans son calcul.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**
</dt> <dd>

l’appareil n’est pas sur la dernière mise à jour, car l’approbation des mises à jour n’est pas effectuée par le biais de Windows Update.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**
</dt> <dd>

L’appareil n’est pas sur la dernière mise à jour en raison d’une raison qui ne peut pas être déterminée par l’évaluation.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**
</dt> <dd>

l’appareil n’est pas sur la dernière mise à jour des fonctionnalités en raison de la stratégie de Version cible de l’Windows Update de l’appareil. Cette stratégie conserve l’appareil sur la version de la fonctionnalité ciblée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée le plus souvent avec les structures [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) et [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , qui sont utilisées à leur tour avec la méthode [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) pour [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                   |
| MIDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




