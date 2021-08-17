---
description: Remplace le en-tête supérieur actuel par le autre spécifié et efface le type de confirmation pour tous les objets IContextNode associés à l’autre.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer :: ModifyTopAlternate, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092039"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>IInkAnalyzer :: ModifyTopAlternate, méthode

Remplace le en-tête supérieur actuel par le autre spécifié et efface le type de confirmation pour tous les objets [**IContextNode**](icontextnode.md) associés à l’autre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlternate* \[ dans\]
</dt> <dd>

Objet [**IAnalysisAlternate**](ianalysisalternate.md) contenant la nouvelle alternative supérieure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Pour récupérer des analyses alternatives, utilisez la méthode [**IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer :: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou la [**méthode IInkAnalyzer :: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Pour récupérer les objets [**IContextNode**](icontextnode.md) associés à une analyse alternative, utilisez la [**méthode IAnalysisAlternate :: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Pour modifier le type de confirmation d’un nœud de contexte, utilisez [**IContextNode :: Confirm**](icontextnode-confirm.md).

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




