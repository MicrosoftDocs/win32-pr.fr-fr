---
title: Structure MPTHREAT_INFO (MpClient. h)
description: Contient des informations sur une menace.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFO
- PMPTHREAT_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466655"
---
# <a name="mpthreat_info-structure"></a>\_Structure d’informations MPTHREAT

Contient des informations sur une menace.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ThreatID**
</dt> <dd>

Type : **\_ ID MPTHREAT**

</dd> <dd>

Identificateur de la menace. Le bit supérieur est défini pour identifier les menaces liées à l’antivirus.

</dd> <dt>

**DetectionID**
</dt> <dd>

Type : **GUID**

</dd> <dd>

ID de détection.

</dd> <dt>

**Nom**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Nom de la menace.

</dd> <dt>

**ThreatType**
</dt> <dd>

Type : **[ **MPTHREAT \_**](mpthreat-type.md)**

</dd> <dd>

Type de menace. Permet de faire la distinction entre différents types de menaces, tels que connu, inconnu ou bien connu. Consultez [**\_ type MPTHREAT**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Type : **[ **MPTHREAT \_ Severity**](mpthreat-severity.md)**

</dd> <dd>

Gravité des menaces. Consultez [**\_ gravité MPTHREAT**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Type : **[ **MPTHREAT \_ Category**](mpthreat-category.md)**

</dd> <dd>

Catégorie de menace, comme un cheval de Troie ou un enregistreur d’enregistreur. Consultez [**la \_ catégorie MPTHREAT**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

ID de description brève de la menace.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

ID de description de l’avis de menace.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Type : **[ **MPTHREAT \_ Status**](mpthreat-status.md)**

</dd> <dd>

État de la menace, tel que détecté, nettoyé ou mis en quarantaine. Consultez [**l' \_ État de MPTHREAT**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre d’actions suggérées dans **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Type : **[**\_ actions MPTHREAT action**](mpthreat-action.md) \[ MP \_ Max \_ suggestions\]**

</dd> <dd>

Tableau d’actions suggérées. Consultez [**\_ action MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre de ressources dans **ResourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Type : **PMPRESOURCE \_ info \** _

</dd> <dd>

Liste des ressources identifiées par la menace. Consultez [_ *MPRESOURCE \_ info* *](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Heure de la dernière modification de l’état de la menace.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Type : **HRESULT**

</dd> <dd>

Code d’état associé à l’état de la menace.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Type : **[ **\_ détection MPTHREAT**](mpthreat-detection.md)**

</dd> <dd>

Type de détection des menaces, par exemple concret, suspect ou générique. Consultez [**MPTHREAT \_ Detection**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Type : **GUID**

</dd> <dd>

GUID de mise en quarantaine.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**

</dd> <dd>

État de l’exécution de la menace, tel que inconnu, bloqué ou actif. Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Données**
</dt> <dd>

Informations supplémentaires. Le pointeur vers la structure appropriée dépend de la valeur de **ThreatType**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Type : **PMPTHREAT \_ INFOEX \_ inutilisé**

</dd> <dd>

Lorsque **ThreatType**  ==  **MPTHREAT, \_ tapez \_ KNOWNBAD**. Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Type : **PMPTHREAT \_ INFOEX \_ BEHAVIOR**

</dd> <dd>

Lorsque le  ==  **\_ \_ comportement de type ThreatType MPTHREAT**. Consultez [**\_ \_ comportement de MPTHREAT INFOEX**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Type : **PMPTHREAT \_ INFOEX \_ inutilisé**

</dd> <dd>

Quand le type **ThreatType**  ==  **MPTHREAT est \_ \_ inconnu**. Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Type : **PMPTHREAT \_ INFOEX \_ inutilisé**

</dd> <dd>

Lorsque **ThreatType** = = MPTHREAT \_ \_ , tapez KNOWNGOOD. Consultez [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Type : **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Lorsque **ThreatType**  ==  **MPTHREAT \_ type \_ NIS**. Consultez [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Type : **[ **MPDETECTION \_ State**](mpdetection-state.md)**

</dd> <dd>

État actuel de la détection. Consultez [**\_ État de MPDETECTION**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Utilisateur associé à la détection, au format « domaine/utilisateur ».

</dd> <dt>

**DetectionSource**
</dt> <dd>

Type : **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Source de la détection. Consultez [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Nom du processus associé à la détection.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Type : **[ **MPDETECTION \_ origin**](mpdetection-origin.md)**

</dd> <dd>

Origine de la détection, telle que local ou réseau. Consultez [**MPDETECTION \_ origin**](mpdetection-origin.md).

</dd> <dt>

**Reserved1**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Métadonnées réservées sur la détection.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Heure de la détection initiale.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**

</dd> <dd>

État de l’exécution juste avant la correction. Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**RemediationTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

La mise à jour de l’heure s’est produite.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Type : **[ **MPEXECUTION \_ Status**](mpexecution-status.md)**

</dd> <dd>

État de l’exécution après la correction. Consultez [**l' \_ État de MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Type : **bool**

</dd> <dd>

True si l’échec de la correction était critique.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

La raison de l’échec de la mise à jour n’est pas critique. Il n’est pas garanti que cela soit pris en charge à l’avenir.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Utilisateur qui a demandé la mise à jour, au format « domaine/utilisateur ».

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre de ressources dans **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Type : **PMPRESOURCE \_ info \[ RemediationResourceCount \]**

</dd> <dd>

Liste des ressources qui ont échoué lors de la mise à jour. Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**FailureResolved**
</dt> <dd>

Type : **bool**

</dd> <dd>

True si l’échec de la correction a été résolu. Le compartiment est alors déplacé vers l’achèvement ou une action supplémentaire.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Type : **[ **\_ raison MPRESOLVED**](mpresolved-reason.md)**

</dd> <dd>

Raison de la résolution de l’échec de la correction. C’est la raison pour laquelle la détection a été déplacée de échec vers action supplémentaire ou terminée. Consultez [**la \_ raison MPRESOLVED**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Actions supplémentaires requises.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Toutes les actions supplémentaires qui ont été effectuées.

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Informations supplémentaires sur la détection des menaces.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**MPDETECTION \_ origine**](mpdetection-origin.md)
</dt> <dt>

[**État de MPDETECTION \_**](mpdetection-state.md)
</dt> <dt>

[**État de MPEXECUTION \_**](mpexecution-status.md)
</dt> <dt>

[**\_raison MPRESOLVED**](mpresolved-reason.md)
</dt> <dt>

[**\_informations MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_action MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**\_catégorie MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**\_détection MPTHREAT**](mpthreat-detection.md)
</dt> <dt>

[**comportement de MPTHREAT \_ INFOEX \_**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md)
</dt> <dt>

[**\_gravité MPTHREAT**](mpthreat-severity.md)
</dt> <dt>

[**État de MPTHREAT \_**](mpthreat-status.md)
</dt> <dt>

[**\_type MPTHREAT**](mpthreat-type.md)
</dt> </dl>

 

 





