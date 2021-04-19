---
title: RegistrationInfo. SecurityDescriptor, propriété
description: Pour les scripts, obtient ou définit le descripteur de sécurité de la tâche.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propriété SecurityDescriptor Planificateur de tâches
- Propriété SecurityDescriptor Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510928"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo. SecurityDescriptor, propriété

Pour les scripts, obtient ou définit le descripteur de sécurité de la tâche. Si un descripteur de sécurité différent est fourni lors de l’inscription de la tâche, il remplacera le descripteur de sécurité défini par cette propriété.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valeur de la propriété

Descripteur de sécurité associé à la tâche.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, le descripteur de sécurité de la tâche est spécifié à l’aide de l’élément [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) du schéma planificateur de tâches.

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

 

 





