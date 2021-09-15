---
description: Modifie l’identificateur de paramètres régionaux pour les traits spécifiés.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'IInkAnalyzer :: SetStrokesLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294598"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>IInkAnalyzer :: SetStrokesLanguageId, méthode

Modifie l’identificateur de paramètres régionaux pour les traits spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
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

Tableau d’identificateurs pour les traits auxquels assigner l’identificateur de paramètres régionaux.

</dd> <dt>

*lStrokesLCID* \[ dans\]
</dt> <dd>

Identificateur de paramètres régionaux à assigner aux traits.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Les paramètres régionaux d’un trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Pour obtenir les paramètres régionaux actuellement assignés à un trait, appelez la [**méthode IInkAnalyzer :: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Les traits spécifiés sont déplacés vers un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)) qui contient des traits de la même langue. S’il n’existe pas de [**IContextNode**](icontextnode.md) de ce type, cette méthode crée un nouveau nœud d’encre non classifié et y déplace les traits. Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.

Si cette méthode déplace les traits d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également les zones englobantes des traits à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Cette méthode ne déplace pas un trait si le paramètre *lStrokeLCID* correspond à l’identificateur de langue actuel du trait.

Si un trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.

Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.

Cette méthode retourne un code d’erreur lorsque strokeIds a la **valeur null**.

Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**IInkAnalyzer :: GetStrokeLanguageId, méthode**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer :: SetStrokeLanguageId, méthode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

