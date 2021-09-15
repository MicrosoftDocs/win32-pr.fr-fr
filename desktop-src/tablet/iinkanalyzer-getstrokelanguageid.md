---
description: Retourne l’identificateur de paramètres régionaux du trait spécifié.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer :: GetStrokeLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524064"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>IInkAnalyzer :: GetStrokeLanguageId, méthode

Retourne l’identificateur de paramètres régionaux du trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait.

</dd> <dt>

*lStrokeLCID* \[ à\]
</dt> <dd>

Identificateur de paramètres régionaux pour le trait spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Les paramètres régionaux du trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Pour modifier les paramètres régionaux du trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou [**IInkAnalyzer :: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

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

[**IInkAnalyzer :: SetStrokeLanguageId, méthode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer :: SetStrokesLanguageId, méthode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




