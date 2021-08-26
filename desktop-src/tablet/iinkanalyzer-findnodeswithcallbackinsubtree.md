---
description: Récupère tous les objets IContextNode qui correspondent aux critères spécifiés et sont des descendants de l’objet IContextNode spécifié.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d6ab8e66e75af4e31a1efacd082f79f68d5f63c546c56d59bf4ca0fedc201929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939929"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode

Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés et sont des descendants de l’objet **IContextNode** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCriteria* \[ dans\]
</dt> <dd>

Objet [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilisé pour déterminer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à ses critères spécifiés.

</dd> <dt>

*pContextNodeToSearchFrom* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) dont les descendants sont recherchés.

</dd> <dt>

*ppContextNodesFound* \[ à\]
</dt> <dd>

Pointeur vers le [**IContextNodes**](icontextnodes.md) contenant tous les nœuds qui répondent aux critères spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas le nœud *pContextNodeToSearchFrom* , cette méthode retourne un code d’erreur.

Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.

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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

