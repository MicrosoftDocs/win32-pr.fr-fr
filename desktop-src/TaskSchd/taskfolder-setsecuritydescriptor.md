---
title: TaskFolder. SetSecurityDescriptor, propriété
description: Pour les scripts, définit le descripteur de sécurité du dossier.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Planificateur de tâches de la propriété SetSecurityDescriptor
- Planificateur de tâches de la propriété SetSecurityDescriptor, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033789"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>TaskFolder. SetSecurityDescriptor, propriété

Pour les scripts, définit le descripteur de sécurité du dossier.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’un dossier de tâches afin d’autoriser ou de refuser à certains utilisateurs et groupes l’accès à un dossier de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





