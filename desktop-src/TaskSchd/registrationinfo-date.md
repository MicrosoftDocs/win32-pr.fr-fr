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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122865"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





