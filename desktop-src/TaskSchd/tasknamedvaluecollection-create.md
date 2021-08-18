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
ms.openlocfilehash: d974eb7fb93d3bb617ce122426b4003a708cbe3ed753ba758fdd5f71ed8bc87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858062"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





