---
description: Charge les résultats d’analyse enregistrés dans le IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer :: LoadResults, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485073"
---
# <a name="iinkanalyzerloadresults-method"></a>IInkAnalyzer :: LoadResults, méthode

Charge les résultats d’analyse enregistrés dans le [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulDataSize* \[ dans\]
</dt> <dd>

Nombre d’octets dans *pbSerializedResults*.

</dd> <dt>

*pbSerializedResults* \[ dans\]
</dt> <dd>

Résultats de l’analyse sérialisée.

</dd> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait.

</dd> <dt>

*plOriginalStrokeIds* \[ dans\]
</dt> <dd>

Tableau d’identificateurs de trait d’origine.

</dd> <dt>

*plNewStrokeIds* \[ dans\]
</dt> <dd>

Tableau de nouveaux identificateurs de trait.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** si le chargement a réussi ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Lorsque [**IInkAnalyzer**](iinkanalyzer.md) ajoute un [**IContextNode**](icontextnode.md) à partir des résultats enregistrés, il attribue un nouvel identificateur global unique (Guid) au **IContextNode** (voir [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md) et les propriétés du [nœud de contexte](context-node-properties.md)).

Cette méthode ajoute les résultats d’analyse enregistrés à l’arborescence [**IContextNode**](icontextnode.md) existante. Pour vous assurer que les résultats combinés sont triés correctement, ajoutez la zone contenant les nœuds de contexte chargés à la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) et Réanalysez l’encre.

Les méthodes de méthode [**IInkAnalyzer :: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer :: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)et [**IInkAnalyzer :: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) n’enregistrent pas les données de paquet avec les résultats d’analyse.

Chaque identificateur dans *plOriginalStrokeIds* est l’identificateur de trait du trait dans les résultats d’analyse enregistrés. Chaque identificateur dans *plNewStrokeIds* est le nouvel identificateur avec lequel remplacer l’identificateur d’origine dans les résultats de l’analyse chargée.

Si un indicateur d’analyse enregistré est en conflit avec un indicateur d’analyse existant, le [**IInkAnalyzer**](iinkanalyzer.md) ne charge pas l’indicateur enregistré, mais charge le reste des résultats enregistrés. Toutefois, si le **IInkAnalyzer** charge des résultats pour un trait qui se trouve dans la zone d’un indicateur d’analyse enregistré que le **IInkAnalyzer** ne charge pas, le **IInkAnalyzer** ajoute le cadre englobant du trait à la région de modification de l’objet **IInkAnalyzer** . En outre, si le **IInkAnalyzer** charge des résultats pour un trait qui se trouve dans une zone d’indicateur d’analyse existante, le **IInkAnalyzer** ajoute également le cadre englobant du trait à la région de modification de l’objet **IInkAnalyzer** . Pour plus d’informations sur les indicateurs d’analyse, consultez Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md).

Cette méthode peut déclencher les événements [**\_ IAnalysisProxyEvents :: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents :: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)et [**\_ IAnalysisProxyEvents :: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) lors du chargement des résultats enregistrés.

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: GetDirtyRegion, méthode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: SetDirtyRegion, méthode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResults, méthode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResultsForNodes, méthode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer :: SaveResultsForStrokes, méthode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




