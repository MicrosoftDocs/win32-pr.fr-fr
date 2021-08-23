---
description: Modifie le type du trait spécifié.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer :: SetStrokeType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6d65c01ba3618bad563ee2b8c8a9c4fee3479a12c796b2f2f570832fac1d826c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709029"
---
# <a name="iinkanalyzersetstroketype-method"></a>IInkAnalyzer :: SetStrokeType, méthode

Modifie le type du trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur de trait du trait auquel assigner *StrokeType*.

</dd> <dt>

*StrokeType* \[ dans\]
</dt> <dd>

Valeur [**StrokeType**](stroketype.md) à assigner au trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Si le type du trait est la [](stroketype.md) valeur StrokeType **StrokeType non \_ classifiée**, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre. Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.

[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre. Pour spécifier ou modifier le type de trait, utilisez la méthode **IInkAnalyzer :: SetStrokeType** ou [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md).

Si un trait est associé à un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)), cette méthode déplace le trait vers un nœud d’encre non classifié qui contient des traits du même langage. Si ce nœud de contexte n’existe pas, cette méthode crée un nouveau nœud d’encre non classifié et lui ajoute le trait. Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.

Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Cette méthode ne déplace pas un trait si le paramètre *StrokeType* correspond au type actuel du trait.

La définition du type de trait sur les traits associés à un ContextNode qui a NodeTypeAndProperties Confirm lève une exception InvalidOperationException.

Si le trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.

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

[**IInkAnalyzer :: GetStrokeType, méthode**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer :: SetStrokesType, méthode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




