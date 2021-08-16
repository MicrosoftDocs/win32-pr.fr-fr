---
description: Obtient le rectangle englobant du IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion :: GetBounds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092330"
---
# <a name="ianalysisregiongetbounds-method"></a>IAnalysisRegion :: GetBounds, méthode

Obtient le rectangle englobant du [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBoundingRectangle* \[ à\]
</dt> <dd>

Rectangle englobant du [**IAnalysisRegion**](ianalysisregion.md) dans les coordonnées de l’espace d’encre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Les limites sont exprimées en coordonnées d’espace d’encre.

Si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone infinie, les limites gauche et supérieure sont **int \_ min**; et les limites droite et inférieure sont **int \_ Max**.

Si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone vide, toutes les limites du rectangle sont 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion :: GetRegionScans, méthode**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




