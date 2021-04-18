---
title: TaskVariables. GetContext, méthode
description: Pour les scripts, permet de partager le contexte entre différentes étapes et tâches qui se trouvent dans la même instance de tâche.
ms.assetid: c3f1245c-531b-43f4-a3e4-8cb5deedd375
keywords:
- GetContext, méthode Planificateur de tâches
- GetContext, méthode Planificateur de tâches, objet TaskVariables
- Objet TaskVariables Planificateur de tâches, GetContext, méthode
topic_type:
- apiref
api_name:
- TaskVariables.GetContext
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897f0b160afd2276831ad5adb59a91fec9d0820d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536285"
---
# <a name="taskvariablesgetcontext-method"></a>TaskVariables. GetContext, méthode

Pour les scripts, permet de partager le contexte entre différentes étapes et tâches qui se trouvent dans la même instance de tâche. Cette méthode n’est pas implémentée.

## <a name="syntax"></a>Syntaxe


```VB
TaskVariables.GetContext( _
  ByRef context _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*contexte* \[ à\]
</dt> <dd>

Contexte utilisé pour partager le contexte entre différentes étapes et tâches qui se trouvent dans la même instance de tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskVariables**](taskvariables.md)
</dt> </dl>

 

 





