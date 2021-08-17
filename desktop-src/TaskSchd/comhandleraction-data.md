---
title: ComHandlerAction. Data, propriété
description: Pour les scripts, obtient ou définit les données supplémentaires associées au gestionnaire.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Planificateur de tâches de propriétés de données
- Planificateur de tâches de propriétés de données, objet ComHandlerAction
- Objet ComHandlerAction Planificateur de tâches, propriété de données
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254457941d55d9a6b130ec504563236e60baf7ba1a1d44d5851ed3c712634afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139602"
---
# <a name="comhandleractiondata-property"></a>ComHandlerAction. Data, propriété

Pour les scripts, obtient ou définit les données supplémentaires associées au gestionnaire.

## <a name="syntax"></a>Syntaxe


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Valeur de la propriété

Arguments requis par le gestionnaire.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de code XML, les données d’un gestionnaire COM sont spécifiées dans l’élément [**Data**](taskschedulerschema-data-comhandlertype-element.md) du schéma planificateur de tâches.

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

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





