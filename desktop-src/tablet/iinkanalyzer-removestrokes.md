---
description: Supprime les traits spécifiés du IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'IInkAnalyzer :: RemoveStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525333"
---
# <a name="iinkanalyzerremovestrokes-method"></a>IInkAnalyzer :: RemoveStrokes, méthode

Supprime les traits spécifiés du [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans *plStrokes*.

</dd> <dt>

*plStrokes* \[ dans\]
</dt> <dd>

Identificateurs des traits à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Cette méthode supprime les données de paquet pour et les références aux traits spécifiés à partir du [**IInkAnalyzer**](iinkanalyzer.md).

Cette méthode supprime les traits du nœud de contexte feuille qui référence les traits. Si un [**IContextNode**](icontextnode.md) ne fait plus référence à aucun trait, cette méthode supprime le **IContextNode** et tout objet **IContextNode** ancêtre qui n’a plus de nœuds enfants.

Une fois que cette méthode a supprimé les traits du [**IContextNode**](icontextnode.md), elle met à jour la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) pour inclure le cadre englobant des traits supprimés.

Si un trait identifié dans *plStrokes* n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.

Si aucun des traits identifiés dans *plStrokes* n’est associé à l’analyseur d’encre, cette méthode retourne sans mettre à jour la [**IInkAnalyzer**](iinkanalyzer.md).

Cette méthode retourne le code d’erreur et lorsque *plStrokes* a la valeur null.

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

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer :: GetDirtyRegion, méthode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




