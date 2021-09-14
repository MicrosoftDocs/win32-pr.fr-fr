---
description: Spécifie les événements associés aux étapes du proxy de données d’un objet IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interface _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220289"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Interface IAnalysisProxyEvents

Spécifie les événements associés aux étapes du proxy de données d’un objet [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Événements](/windows)

### <a name="events"></a>Événements

L’interface **\_ IAnalysisProxyEvents** contient ces événements.



| Événement                                                                                      | Description                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)                     | Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a créé un objet [**IContextNode**](icontextnode.md) .<br/>                                                                  |
| [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)                   | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextNode**](icontextnode.md) .<br/>                                                                 |
| [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)               | Se produit avant que [**IInkAnalyzer**](iinkanalyzer.md) ajoute un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .<br/>           |
| [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .<br/>         |
| [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) vers une nouvelle position dans la collection de sous-nœuds du nœud parent.<br/> |
| [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a mis à jour une ou plusieurs propriétés d’un objet [**IContextNode**](icontextnode.md) .<br/>                                        |
| [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)             | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) en modifiant son nœud parent.<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le **IInkAnalyzer**.<br/>                      |
| [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse dans la région d’un objet [**IContextNode**](icontextnode.md) partiellement rempli.<br/>               |
| [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)                         | Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) déplace un trait d’un objet [**IContextNode**](icontextnode.md) à un autre.<br/>                                           |



 

## <a name="remarks"></a>Notes

Utilisez ces événements lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Pour plus d’informations sur la synchronisation des données de votre application avec **IInkAnalyzer**, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_IAnalysisEvents](-ianalysisevents.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

