---
description: Remplace le IAnalysisAlternate actuel par le haut de la valeur spécifiée.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523241"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode

Remplace le [**IAnalysisAlternate**](ianalysisalternate.md)actuel par le haut de la valeur spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*autre* \[ dans\]
</dt> <dd>

L’analyse alternative à définir en tant que nouvelle alternative supérieure.

</dd> <dt>

*fconfirmAutomatically* \[ dans\]
</dt> <dd>

**Variante \_ TRUE** pour définir tous les nœuds de contexte de feuille manuscrite qui correspondent à l’analyse alternative à un type de confirmation **ConfirmationType \_ NodeTypeAndProperties** (consultez [**IContextNode :: IsConfirmed**](icontextnode-isconfirmed.md) et [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSe** pour définir tous les nœuds de contexte de feuille manuscrite qui correspondent à l’analyse alternative à un type de confirmation **ConfirmationType \_ None**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Pour récupérer des analyses alternatives, utilisez la méthode [**IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer :: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou la [**méthode IInkAnalyzer :: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Pour récupérer les objets de nœud de contexte associés à une analyse alternative, utilisez la [**méthode IAnalysisAlternate :: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Pour modifier le type de confirmation d’un nœud de contexte, utilisez [**IContextNode :: Confirm**](icontextnode-confirm.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType de l’analyse de l’encre**](confirmationtype.md)
</dt> <dt>

[Référence](ink-analysis-reference.md)
</dt> </dl>

 

 




