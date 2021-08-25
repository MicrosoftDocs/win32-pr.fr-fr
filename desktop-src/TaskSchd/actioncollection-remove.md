---
title: ActionCollection. Remove, méthode
description: Pour les scripts, supprime l’action spécifiée de la collection.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Supprimer la méthode Planificateur de tâches
- Remove, méthode Planificateur de tâches, objet ActionCollection
- Objet ActionCollection Planificateur de tâches, Remove, méthode
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011739"
---
# <a name="actioncollectionremove-method"></a>ActionCollection. Remove, méthode

Pour les scripts, supprime l’action spécifiée de la collection.

## <a name="syntax"></a>Syntaxe


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index de l’action à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsque vous supprimez des éléments, Notez que l’index du premier élément de la collection est 1 et que l’index du dernier élément est la valeur de la propriété [**ActionCollection. Count**](actioncollection-count.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





