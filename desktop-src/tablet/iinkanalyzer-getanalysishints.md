---
description: Obtient tous les objets IContextNode Hint d’analyse attachés à IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'IInkAnalyzer :: GetAnalysisHints, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b1aa2dede2e5027b3e626d3cbcc152d03348e34b87e4cbb5e9d3e2106d3b58c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008379"
---
# <a name="iinkanalyzergetanalysishints-method"></a>IInkAnalyzer :: GetAnalysisHints, méthode

Obtient tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés à [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAnalysisHints* \[ à\]
</dt> <dd>

Pointeur vers tous les objets Hint d’analyse [**IContextNode**](icontextnode.md) dans le [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAnalysisHints* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Cette méthode retourne une collection vide si aucun nœud d’indicateur d’analyse n’est attaché à [**IInkAnalyzer**](iinkanalyzer.md).

Un nœud d’indicateur d’analyse est un [**IContextNode**](icontextnode.md) avec un type de nœud de contexte AnalysisHint (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md)).

Pour ajouter des informations de contexte à l’indicateur, utilisez [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) avec le paramètre *pPropertyDataId* défini sur l’un des identificateurs globaux uniques (Guid) dans les constantes des propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) .

Pour rechercher les valeurs de propriété qui sont définies sur un nœud de contexte, utilisez [**IContextNode :: GetPropertyDataIds**](icontextnode-getpropertydataids.md). Pour rechercher la valeur d’une propriété, utilisez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer ::D méthode eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHintsByName, méthode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

