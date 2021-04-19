---
title: RegistrationInfo. date, propriété
description: Pour les scripts, obtient ou définit la date et l’heure d’enregistrement de la tâche.
ms.assetid: ecff01b6-a1de-458a-9728-34169f17d42b
keywords:
- Propriété Date Planificateur de tâches
- Propriété Date Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété Date
topic_type:
- apiref
api_name:
- RegistrationInfo.Date
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adfdfa8b2dd3f8dcaa3b2fd5778b1e50dabfab51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510516"
---
# <a name="registrationinfodate-property"></a>RegistrationInfo. date, propriété

Pour les scripts, obtient ou définit la date et l’heure d’enregistrement de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.Date As String
```



## <a name="property-value"></a>Valeur de la propriété

Date d’inscription de la tâche.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, la date d’inscription est spécifiée à l’aide de l’élément [**Date**](taskschedulerschema-date-registrationinfotype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





