---
description: Récupère tous les objets IContextNode qui correspondent aux critères spécifiés.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'IInkAnalyzer :: FindNodesWithCallBack, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522268"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a>IInkAnalyzer :: FindNodesWithCallBack, méthode

Récupère tous les objets [**IContextNode**](icontextnode.md) qui correspondent aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCriteria* \[ dans\]
</dt> <dd>

Objet [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilisé pour déterminer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à ses critères spécifiés.

</dd> <dt>

*ppContextNodesFound* \[ à\]
</dt> <dd>

Pointeur vers la collection [**IContextNodes**](icontextnodes.md) contenant tous les nœuds qui répondent aux critères spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.

## <a name="requirements"></a>Spécifications



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

[**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

