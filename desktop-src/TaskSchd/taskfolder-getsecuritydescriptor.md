---
title: TaskFolder. GetSecurityDescriptor, propriété
description: Pour les scripts, obtient le descripteur de sécurité pour le dossier.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Planificateur de tâches de la propriété GetSecurityDescriptor
- Planificateur de tâches de la propriété GetSecurityDescriptor, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531620"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>TaskFolder. GetSecurityDescriptor, propriété

Pour les scripts, obtient le descripteur de sécurité pour le dossier.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





