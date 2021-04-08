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
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941895"
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

## <a name="remarks"></a>Notes

Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’un dossier de tâches afin d’autoriser ou de refuser à certains utilisateurs et groupes l’accès à un dossier de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





