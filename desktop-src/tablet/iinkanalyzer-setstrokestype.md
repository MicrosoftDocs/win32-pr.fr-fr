---
description: Modifie le type des traits spécifiés.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'IInkAnalyzer :: SetStrokesType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 41852b0a4ec52b5ce07a12964cd03ebb0ab1bfe437e37bf8249752d0162470a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091495"
---
# <a name="iinkanalyzersetstrokestype-method"></a>IInkAnalyzer :: SetStrokesType, méthode

Modifie le type des traits spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strokeIdCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans *plStrokes*.

</dd> <dt>

*plStrokes* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de trait des traits auxquels assigner *StrokeType*.

</dd> <dt>

*StrokeType* \[ dans\]
</dt> <dd>

Valeur [**StrokeType**](stroketype.md) à assigner aux traits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Si le type du trait est la [](stroketype.md) valeur StrokeType **StrokeType non \_ classifiée**, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre. Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.

[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre. Pour spécifier ou modifier le type de trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) ou **IInkAnalyzer :: SetStrokesType**.

Si un trait est associé à un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)), cette méthode déplace le trait vers un nœud d’encre non classifié qui contient des traits du même langage. Si ce nœud de contexte n’existe pas, cette méthode crée un nouveau nœud d’encre non classifié et lui ajoute le trait. Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.

Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Cette méthode ne déplace pas un trait si le paramètre *StrokeType* correspond au type actuel du trait.

Si un trait identifié dans *strokeIds* n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.

Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.

La définition du type de trait sur les traits associés à un ContextNode qui a NodeTypeAndProperties Confirm lève une exception InvalidOperationException.

Cette méthode retourne un code d’erreur lorsque *plStrokes* a la **valeur null**.

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

[**IInkAnalyzer :: SetStrokeType, méthode**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




