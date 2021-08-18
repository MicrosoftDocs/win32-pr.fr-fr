---
description: Récupère d’autres analyses pour les nœuds d’une collection IContextNodes spécifiée.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'IInkAnalyzer :: GetAlternatesForContextNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939858"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>IInkAnalyzer :: GetAlternatesForContextNodes, méthode

Récupère d’autres analyses pour les nœuds d’une collection [**IContextNodes**](icontextnodes.md) spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextNodes* \[ dans\]
</dt> <dd>

Collection [**IContextNodes**](icontextnodes.md) pour laquelle les alternatives d’analyse sont retournées.

</dd> <dt>

*ulMaximumAlternates* \[ dans\]
</dt> <dd>

Nombre maximal d’alternatives à retourner.

</dd> <dt>

*ppAlternates* \[ à\]
</dt> <dd>

Objet [**IAnalysisAlternates**](ianalysisalternates.md) contenant les alternatives d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAlternates* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Le [**IAnalysisAlternate**](ianalysisalternate.md) supérieur est retourné en tant que premier remplacement de la collection.

Les objets [**IContextNode**](icontextnode.md) dans *pContextNodes* n’ont pas besoin de représenter des zones adjacentes du document.

Pour chaque indicateur d’analyse dans les nœuds, le [**IInkAnalyzer**](iinkanalyzer.md) retourne uniquement l’alternative supérieure.

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternates, méthode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer :: GetAlternatesForStrokes, méthode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: ModifyTopAlternate, méthode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

