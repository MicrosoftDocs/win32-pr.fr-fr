---
title: RegisteredTask. Stop, méthode
description: Pour les scripts, arrête immédiatement la tâche inscrite.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Stop, méthode Planificateur de tâches
- Stop, méthode Planificateur de tâches, objet RegisteredTask
- Objet RegisteredTask Planificateur de tâches, méthode Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122905"
---
# <a name="registeredtaskstop-method"></a>RegisteredTask. Stop, méthode

Pour les scripts, arrête immédiatement la tâche inscrite.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Réservé. Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **RegisteredTask. Stop** arrête toutes les instances de la tâche.

Les utilisateurs du compte système peuvent arrêter une tâche, les utilisateurs disposant de privilèges de groupe d’administrateurs peuvent arrêter une tâche et, si un utilisateur dispose de droits pour exécuter et lire une tâche, l’utilisateur peut arrêter la tâche. Un utilisateur peut arrêter les instances de tâche qui s’exécutent sous les mêmes informations d’identification que le compte d’utilisateur. Dans tous les autres cas, l’utilisateur se voit refuser l’accès pour arrêter la tâche.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





