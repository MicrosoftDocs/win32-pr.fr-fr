---
description: Modifie l’identificateur de paramètres régionaux pour le trait spécifié.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'IInkAnalyzer :: SetStrokeLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc91d7d8a710d2640c31e639146bd6a2fd1deac854420d7ceac1bbfdd778022c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091479"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>IInkAnalyzer :: SetStrokeLanguageId, méthode

Modifie l’identificateur de paramètres régionaux pour le trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait auquel assigner l’identificateur de paramètres régionaux.

</dd> <dt>

*lStrokeLCID* \[ dans\]
</dt> <dd>

Identificateur de paramètres régionaux à assigner au trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Les paramètres régionaux d’un trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Pour obtenir les paramètres régionaux actuellement assignés à un trait, appelez la [**méthode IInkAnalyzer :: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Le trait spécifié est déplacé vers un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)) qui contient des traits de la même langue. S’il n’existe pas de [**IContextNode**](icontextnode.md) de ce type, cette méthode crée un nouveau nœud d’encre non classifié et y déplace le trait. Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.

Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Cette méthode ne déplace pas un trait si le paramètre *lStrokeLCID* correspond à l’identificateur de langue actuel du trait.

Si le trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.

Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: GetStrokeLanguageId, méthode**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer :: SetStrokesLanguageId, méthode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

