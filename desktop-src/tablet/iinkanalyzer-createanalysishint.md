---
description: Ajoute un nouveau nœud d’indicateur d’analyse avec une zone infinie à la IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer :: CreateAnalysisHint, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318458"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>IInkAnalyzer :: CreateAnalysisHint, méthode

Ajoute un nouveau nœud d’indicateur d’analyse avec une zone infinie à la [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAnalysisHint* \[ à\]
</dt> <dd>

Nouveau nœud d’indicateur d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md) de l’encre pour obtenir une description des valeurs de retour.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAnalysisHint* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Pour fournir des informations de contexte supplémentaires pour [**IInkAnalyzer**](iinkanalyzer.md), vous pouvez ajouter des indicateurs d’analyse à l’analyseur d’encre. Les indicateurs d’analyse peuvent améliorer la précision de la reconnaissance. Par exemple, vous pouvez ajouter des Factoid et des informations de guide pour les champs dans une application de formulaire.

Cette méthode crée un nouveau [**IContextNode**](icontextnode.md) avec un type de nœud de contexte AnalysisHint (voir [**IContextNode :: GetType**](icontextnode-gettype.md)) et ajoute le nouvel indicateur en tant que sous-nœud du nœud racine de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode méthode**](iinkanalyzer-getrootnode.md)).

Pour ajouter des informations de contexte à l’indicateur, utilisez [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) avec le paramètre *pPropertyDataId* défini sur l’une des constantes de propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) .

Si une indication est assignée à une zone infinie, appelée indication globale, le [**IInkAnalyzer**](iinkanalyzer.md) applique le contexte de l’indicateur à toute l’encre qui ne se trouve pas dans la zone d’un autre indicateur. Plusieurs indicateurs peuvent être attachés à un seul **IInkAnalyzer**. Toutefois, un seul indicateur global peut être attaché à un analyseur d’encre unique, et aucun indicateur non global ne peut se chevaucher. Pour plus d’informations sur les types d’informations de contexte qu’un indicateur peut fournir, consultez Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md).

L’ajout d’un indicateur d’analyse ne marque pas la zone de l’indicateur pour la réanalyse. Pour marquer la zone dans l’indicateur pour la réanalyse, utilisez la [**méthode IInkAnalyzer :: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) pour définir la région de modification sur l’Union de la région et de la zone de modification actuelles de l’indicateur d’analyse.

Lorsque vous utilisez des indicateurs pour une application de formulaire, l’application doit éviter de mélanger le contexte de texte avec de l’encre dans les formulaires. Cela signifie, par exemple, que les noms de champs de texte ne doivent pas être créés dans l’arborescence d’analyse. Les indicateurs sont destinés à associer l’encre à des zones sur des pages ; tout contexte de texte interfère avec cette association d’entrée manuscrite. L’opération d’analyse peut fusionner l’encre et le contexte de texte dans la même région d’écriture, ce qui empêche l’encre d’être associée à la zone d’indication.

Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IInkAnalyzer ::D méthode eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHints, méthode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHintsByName, méthode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Propriétés de l’indicateur d’analyse](analysis-hint-properties.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

