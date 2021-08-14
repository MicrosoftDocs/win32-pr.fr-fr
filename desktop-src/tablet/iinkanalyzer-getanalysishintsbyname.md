---
description: Récupère tous les objets IContextNode Hint d’analyse attachés au IInkAnalyzer et portant le nom spécifié.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer :: GetAnalysisHintsByName, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 24c69cd1dd321b5f142fe07b7463941fc0944a2206f1f8d6baf0ebbe8459b6ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719191"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>IInkAnalyzer :: GetAnalysisHintsByName, méthode

Récupère tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés au [**IInkAnalyzer**](iinkanalyzer.md) et portant le nom spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hintName* \[ dans\]
</dt> <dd>

Nom de l’indicateur à rechercher.

</dd> <dt>

*ppAnalysisHints* \[ à\]
</dt> <dd>

L’indicateur d’analyse [**IContextNode**](icontextnode.md) les objets du [**IInkAnalyzer**](iinkanalyzer.md) qui portent le nom spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md) de l’encre valeurs de retour.

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

[**IInkAnalyzer :: GetAnalysisHints, méthode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

