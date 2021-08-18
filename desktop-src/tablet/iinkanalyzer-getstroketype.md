---
description: Récupère le type du trait spécifié.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer :: GetStrokeType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71bf3775be1c21e59cf41a51fa5a6140e86e44ac81a2863892c1f252666e0f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092139"
---
# <a name="iinkanalyzergetstroketype-method"></a>IInkAnalyzer :: GetStrokeType, méthode

Récupère le type du trait spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait.

</dd> <dt>

*pStrokeType* \[ à\]
</dt> <dd>

Classification du trait spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Si le type du trait est la valeur [**StrokeType**](stroketype.md) StrokeType non \_ classifiée, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre. Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.

[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre. Pour spécifier ou modifier le type de trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) ou [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md).

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

[**IInkAnalyzer :: SetStrokeType, méthode**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**IInkAnalyzer :: SetStrokesType, méthode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




