---
description: Contient une collection d’objets qui implémentent l’interface IContextNode et qui sont le résultat d’une opération d’analyse d’encre.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interface IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e1cc15817fa36c8cecaf06c1da0fd8fb7dae77b77909f2e04b5ebaef8100d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266149"
---
# <a name="icontextnodes-interface"></a>Interface IContextNodes

Contient une collection d’objets qui implémentent l’interface [**IContextNode**](icontextnode.md) et qui sont le résultat d’une opération d’analyse d’encre.

## <a name="members"></a>Membres

L’interface **IContextNodes** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNodes** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IContextNodes** possède ces méthodes.



| Méthode                                                       | Description                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddContextNode**](icontextnodes-addcontextnode.md)       | Ajoute un objet [**IContextNode**](icontextnode.md) à cette collection. <br/>                                  |
| [**GetContextNode**](icontextnodes-getcontextnode.md)       | Récupère l’objet [**IContextNode**](icontextnode.md) à l’index spécifié dans cette collection. <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | Récupère le nombre d’objets [**IContextNode**](icontextnode.md) contenus dans cette collection. <br/>       |
| [**RemoveContextNode**](icontextnodes-removecontextnode.md) | Supprime un objet [**IContextNode**](icontextnode.md) de cette collection. <br/>                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

