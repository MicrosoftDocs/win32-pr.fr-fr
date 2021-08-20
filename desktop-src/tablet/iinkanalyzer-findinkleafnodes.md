---
description: Récupère tous les nœuds de feuille d’encre.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'IInkAnalyzer :: FindInkLeafNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a4cd945c32ace514654c6d9c63a7d05ae486adf0158205ae088d443ed9be6992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043966"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a>IInkAnalyzer :: FindInkLeafNodes, méthode

Récupère tous les nœuds de feuille d’encre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppContextNodesFound* \[ à\]
</dt> <dd>

Pointeur vers la collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds de feuille d’encre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Les nœuds terminaux ne contiennent pas de nœuds enfants. Les nœuds d’entrée contiennent des données de trait. Les objets InkWord, InkDrawing et InkBullet [**IContextNode**](icontextnode.md) sont des exemples de nœuds feuille d’encre. Pour plus d’informations, consultez [types de nœuds de contexte](context-node-types.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: FindLeafNodes, méthode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer :: FindNode, méthode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfType, méthode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBack, méthode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

