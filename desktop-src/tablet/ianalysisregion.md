---
description: Expose des méthodes et des propriétés pour une zone qui représente une zone d’un document.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interface IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d8dc5b0af5746328ead68be3896148b7a4ddf79d6844a6d4ae976b2f29592d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045063"
---
# <a name="ianalysisregion-interface"></a>Interface IAnalysisRegion

Expose des méthodes et des propriétés pour une zone qui représente une zone d’un document.

## <a name="members"></a>Membres

L’interface **IAnalysisRegion** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisRegion** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAnalysisRegion** possède ces méthodes.



| Méthode                                                           | Description                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Répliqué**](ianalysisregion-clone.md)                           | Crée une copie du **IAnalysisRegion**.<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Limite la zone du **IAnalysisRegion** à la partie de sa zone qui ne croise pas le rectangle spécifié.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Limite la zone du **IAnalysisRegion** à la partie de sa zone qui ne croise pas le **IAnalysisRegion** spécifié.<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Récupère le rectangle englobant du **IAnalysisRegion**.<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Récupère un tableau de rectangles qui définit la zone du **IAnalysisRegion**.<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Limite la zone de ce **IAnalysisRegion** à la zone créée par son intersection avec le rectangle spécifié.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Limite la zone du **IAnalysisRegion** à la zone créée par son intersection avec le **IAnalysisRegion** spécifié.<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Détermine si la zone du **IAnalysisRegion** entre en intersection avec le rectangle spécifié.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Récupère une valeur indiquant si le **IAnalysisRegion** représente une zone vide.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Récupère une valeur indiquant si le **IAnalysisRegion** représente une région infinie.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Réduit le **IAnalysisRegion** pour représenter une zone vide.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Développe le **IAnalysisRegion** pour représenter une zone infinie.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Développe la zone de ce **IAnalysisRegion** vers la zone créée par son Union avec le rectangle spécifié.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Développe la zone de ce **IAnalysisRegion** vers la zone créée par son Union avec le **IAnalysisRegion** spécifié.<br/>               |



 

## <a name="remarks"></a>Remarques

Cette interface représente une zone qui est construite à partir de régions rectangulaires. [**IInkAnalyzer**](iinkanalyzer.md) retourne ou interprète les coordonnées d’une zone dans l’espace de coordonnées dans lequel elle reçoit les données de trait.

Pour récupérer les limites actuelles du **IAnalysisRegion**, utilisez la méthode [**IAnalysisRegion :: GetBounds**](ianalysisregion-getbounds.md) ou la [**méthode IAnalysisRegion :: GetRegionScans**](ianalysisregion-getregionscans.md).

Pour modifier la zone d’un **IAnalysisRegion** existant, utilisez les méthodes suivantes.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**IAnalysisRegion :: ExcludeRegion, méthode**](ianalysisregion-excluderegion.md)
-   [**IAnalysisRegion :: IntersectRectangle, méthode**](ianalysisregion-intersectrectangle.md)
-   [**IAnalysisRegion :: IntersectRegion, méthode**](ianalysisregion-intersectregion.md)
-   [**IAnalysisRegion :: MakeEmpty, méthode**](ianalysisregion-makeempty.md)
-   [**IAnalysisRegion :: MakeInfinite, méthode**](ianalysisregion-makeinfinite.md)
-   [**IAnalysisRegion :: UnionRectangle, méthode**](ianalysisregion-unionrectangle.md)
-   [**IAnalysisRegion :: UnionRegion, méthode**](ianalysisregion-unionregion.md)

Cette interface est équivalente au système. Windows. Classe Ink. AnalysisCore. AnalysisRegionBase dans la .NET Framework.

## <a name="requirements"></a>Conditions requises



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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

