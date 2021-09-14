---
description: Récupère des alternatives d’analyse pour les traits avec les identificateurs de trait spécifiés.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer :: GetAlternatesForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220164"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>IInkAnalyzer :: GetAlternatesForStrokes, méthode

Récupère des alternatives d’analyse pour les traits avec les identificateurs de trait spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans *plStrokes*.

</dd> <dt>

*plStrokes* \[ dans\]
</dt> <dd>

Tableau d’identificateurs de trait.

</dd> <dt>

*ulMaximumAlternates* \[ dans\]
</dt> <dd>

Nombre maximal d’autres solutions d’analyse retournées.

</dd> <dt>

*ppAlternates* \[ à\]
</dt> <dd>

Objet [**IAnalysisAlternates**](ianalysisalternates.md) contenant les alternatives d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppAlternates* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Le [**IAnalysisAlternate**](ianalysisalternate.md) supérieur est retourné en tant que premier remplacement de la collection.

Les traits spécifiés n’ont pas besoin de représenter des zones adjacentes du document.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternates, méthode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer :: ModifyTopAlternate, méthode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

