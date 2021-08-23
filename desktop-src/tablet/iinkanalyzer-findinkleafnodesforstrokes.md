---
description: Récupère les nœuds de feuille d’encre qui contiennent les traits spécifiés.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a7424f62008e15feb538df7a6a27745dda17bf6ace4612218608f8e509e75e59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967278"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode

Récupère les nœuds de feuille d’encre qui contiennent les traits spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait transmis.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Tableau des identificateurs de trait.

</dd> <dt>

*ppContextNodesFound* \[ à\]
</dt> <dd>

Collection d’objets [**IContextNode**](icontextnode.md) qui contiennent tous les nœuds de feuille d’encre qui contiennent les traits avec des identificateurs dans le tableau *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Les nœuds terminaux ne contiennent pas de nœuds enfants. Les nœuds d’entrée contiennent des données de trait. Exemples de nœuds de feuille manuscrite : InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objets. Pour plus d’informations, consultez [types de nœuds de contexte](context-node-types.md).

Si aucun nœud ne contient les traits spécifiés, une collection [**IContextNodes**](icontextnodes.md) vide est retournée. De même, si *ulStrokeIdsCount* est égal à zéro, une collection **IContextNodes** vide est retournée.

## <a name="requirements"></a>Configuration requise



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

[**IInkAnalyzer :: FindInkLeafNodes, méthode**](iinkanalyzer-findinkleafnodes.md)
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

 

