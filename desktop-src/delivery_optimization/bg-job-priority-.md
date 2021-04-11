---
title: Énumération BG_JOB_PRIORITY (Deliveryoptimization. h)
description: L’énumération BG_JOB_PRIORITY définit les valeurs constantes qui spécifient le niveau de priorité d’un travail.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Énumération BG_JOB_PRIORITY
- Énumération BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032725"
---
# <a name="bg_job_priority-enumeration"></a>Énumération BG_JOB_PRIORITY

L’énumération **BG_JOB_PRIORITY** définit les valeurs constantes qui spécifient le niveau de priorité d’un travail.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Transfère la tâche au premier plan. Les transferts de premier plan concurrencent la bande passante réseau avec d’autres applications, ce qui peut nuire à l’expérience réseau de l’utilisateur. Il s’agit du niveau de priorité le plus élevé.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Transfère la tâche en arrière-plan. Les transferts en arrière-plan utilisent un petit pourcentage de bande passante réseau.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Le comportement est le même pour tous les travaux qui ne sont pas au premier plan. Pour plus d’informations, consultez les commentaires dans BG_JOB_PRIORITY_HIGH.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Le comportement est le même pour tous les travaux qui ne sont pas au premier plan. Pour plus d’informations, consultez les commentaires dans BG_JOB_PRIORITY_HIGH.

</dd> </dl>

## <a name="remarks"></a>Notes

Plusieurs transferts de premier plan et d’arrière-plan peuvent avoir lieu simultanément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob :: getPriority,**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





