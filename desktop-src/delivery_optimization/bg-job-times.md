---
title: Structure BG_JOB_TIMES (Deliveryoptimization. h)
description: La structure BG_JOB_TIMES fournit des horodatages liés aux travaux.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Structure BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b0fe36c9994bc03a807ff4a575945d203b1f62391b498cca094ed8f264be684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793400"
---
# <a name="bg_job_times-structure"></a>Structure BG_JOB_TIMES

La structure **BG_JOB_TIMES** fournit des horodatages liés aux travaux.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Membres

<dl> <dt>

**CreationTime**
</dt> <dd>

Heure de création du travail. L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**ModificationTime**
</dt> <dd>

Heure de la dernière modification du travail ou du transfert d’octets. L’ajout de fichiers ou l’appel de l’une des méthodes Set dans les interfaces [ * *méthode ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) modifie cette valeur. En outre, les modifications apportées à l’état du travail et l’appel des méthodes [_ *suspend* *](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)et [**complet**](ibackgroundcopyjob-complete.md) modifient cette valeur. L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

Heure à laquelle le travail est passé à l’État BG_JOB_STATE_TRANSFERRED. L’heure est spécifiée en tant que [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob :: GetTimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

