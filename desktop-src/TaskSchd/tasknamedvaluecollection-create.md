---
title: TaskNamedValueCollection. Create, méthode
description: Pour les scripts, crée une paire nom-valeur dans la collection.
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- Créer une méthode Planificateur de tâches
- Create Method Planificateur de tâches, objet TaskNamedValueCollection
- Planificateur de tâches d’objets TaskNamedValueCollection, méthode Create
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3926142b25cbb2d65efaa45d6b767ce2e56ba86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466426"
---
# <a name="tasknamedvaluecollectioncreate-method"></a>TaskNamedValueCollection. Create, méthode

Pour les scripts, crée une paire nom-valeur dans la collection.

## <a name="syntax"></a>Syntaxe


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

Nom associé à une valeur dans une paire nom-valeur.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Valeur associée à un nom dans une paire nom-valeur.

</dd> <dt>

*paire* \[ à\]
</dt> <dd>

Paire nom-valeur créée dans la collection.

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



 

 





