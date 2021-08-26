---
description: Obtient les objets IContextNode associés à cet autre.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate :: GetAlternateNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935519"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>IAnalysisAlternate :: GetAlternateNodes, méthode

Obtient les objets [**IContextNode**](icontextnode.md) associés à cet autre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAlternateNodes* \[ à\]
</dt> <dd>

Pointeur vers la collection [**IContextNodes**](icontextnodes.md) qui contient les objets [**IContextNode**](icontextnode.md) associés à cet autre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppAlternateNodes* lorsque vous n’avez plus besoin d’utiliser la collection de nœuds de contexte.

 

Cette méthode retourne les nœuds de contexte feuille associés à cet autre. Les nœuds terminaux sont, par exemple, InkWord, TextWord, image, InkDrawing et InkBullet. Pour plus d’informations, consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md).

Étant donné qu’ils correspondent à des substitutions, ces objets [**IContextNode**](icontextnode.md) ne sont pas des descendants de la racine **IContextNode** de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)), sauf s’il s’agit de l’alternative supérieure, qui est le premier élément d’une collection [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> <dt>

[Requise. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

