---
title: Méthode RegisteredTask. SetSecurityDescriptor
description: Pour les scripts, définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Planificateur de tâches de la méthode SetSecurityDescriptor
- Méthode SetSecurityDescriptor Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105685"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Méthode RegisteredTask. SetSecurityDescriptor

Pour les scripts, définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*langage SDDL* \[ dans\]
</dt> <dd>

Descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.

> [!Note]  
> Si l’accès à une tâche est refusé au compte système local, le service Planificateur de tâches peut produire des résultats inattendus.

 

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Indicateurs qui spécifient comment définir le descripteur de sécurité. La tâche \_ \_ d’ajout \_ \_ de l’indicateur d’entrée de contrôle d’accès principal (0x10) à partir de l’énumération de [**\_ création de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) peut être spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous pouvez spécifier la liste de contrôle d’accès (ACL) dans le descripteur de sécurité d’une tâche afin d’autoriser ou de refuser l’accès à une tâche à certains utilisateurs et groupes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





