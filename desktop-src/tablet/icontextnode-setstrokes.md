---
description: Associe les traits spécifiés à ce IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'IContextNode :: SetStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514446"
---
# <a name="icontextnodesetstrokes-method"></a>IContextNode :: SetStrokes, méthode

Associe les traits spécifiés à ce [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Identificateurs des traits à associer à ce [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Cette méthode ne met pas à jour la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Utilisez cette méthode pour assigner des données de trait à un nœud de contexte spécifique. Pour plus d’informations sur la synchronisation des données de votre application avec **IInkAnalyzer**, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Si l’un des traits spécifiés est déjà associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne **E \_ INVALIDARG**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStrokes, méthode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




