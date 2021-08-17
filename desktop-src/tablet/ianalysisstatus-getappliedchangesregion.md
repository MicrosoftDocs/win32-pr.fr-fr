---
description: Récupère la région du document qui correspond aux modifications apportées à l’arborescence du nœud de contexte de l’objet IInkAnalyzer à la suite de l’analyse de l’encre.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus :: GetAppliedChangesRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044992"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>IAnalysisStatus :: GetAppliedChangesRegion, méthode

Récupère la région du document qui correspond aux modifications apportées à l’arborescence du nœud de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) à la suite de l’analyse de l’encre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAppliedChangesRegion* \[ à\]
</dt> <dd>

Pointeur vers le [**IAnalysisRegion**](ianalysisregion.md) du document où des modifications ont été apportées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pAppliedChangesRegion* lorsque vous n’avez plus besoin d’utiliser la région d’analyse.

 

Cette méthode est la plus fréquemment utilisée lorsque l’application reçoit des informations à des fins de débogage et qu’elle doit invalider la zone dans laquelle des modifications peuvent se produire afin que les informations de débogage soient peintes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

