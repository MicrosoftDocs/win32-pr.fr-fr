---
description: Récupère tous les objets IContextNode du type spécifié qui contiennent les traits spécifiés.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513428"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode

Récupère tous les objets [**IContextNode**](icontextnode.md) du type spécifié qui contiennent les traits spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNodeType* \[ dans\]
</dt> <dd>

Identificateur global unique (GUID) qui spécifie le type de nœud.

</dd> <dt>

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

Collection d’objets [**IContextNode**](icontextnode.md) qui contiennent tous les nœuds de type *pNodeType* qui contiennent les traits avec des identificateurs dans le tableau *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodesFound* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

La propriété *pNodeType* doit contenir un GUID à partir des constantes de [type de nœud de contexte](context-node-types.md) .

Si le type de nœud spécifié n’est pas un nœud terminal, mais qu’un des descendants du nœud référence un trait dans la collection Strokes, ce nœud est ajouté à la collection retournée.

Si le [**IInkAnalyzer**](iinkanalyzer.md) ne contient pas de [**IContextNode**](icontextnode.md)de ce type, une collection [**IContextNodes**](icontextnodes.md) vide est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
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

[**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBack, méthode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

