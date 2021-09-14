---
description: Cette rubrique présente les détails de l’événement lors de l’utilisation des fonctionnalités du proxy d’analyse des données d’encre.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Flow de l’événement de proxy de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196327"
---
# <a name="data-proxy-event-flow"></a>Flow de l’événement de proxy de données

Cette rubrique présente les détails de l’événement lors de l’utilisation des fonctionnalités du proxy d’analyse des données d’encre.

## <a name="data-proxy-event-flow-overview"></a>vue d’ensemble des Flow d’événements de Proxy de données

Dans l’utilisation du proxy de données de [**InkAnalyzer**](inkanalyzer.md), il est supposé que l’application intégrant le InkAnalyzer possède déjà un modèle de document existant auquel il souhaite effectuer un proxy des résultats de l’analyse. Il est également supposé que l’application aura des résultats de toutes les opérations d’analyse précédentes qu’elle souhaiterait créer sur stockées dans son modèle de document. Il peut également y avoir des contextes non manuscrits qui peuvent être ajoutés au **InkAnalyzer** sous la forme d’un [**ContextNode**](icontextnode.md) **ImageNode** ou **TextWordNode** pour être éventuellement annotés avec de l’encre.

La clé du système de proxy de données est que l’application marque le [**ContextNode**](icontextnode.md) comme étant « partiellement rempli » à l’aide de [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md). Lorsque cet indicateur a la valeur true, [**InkAnalyzer**](inkanalyzer.md) suppose que trois choses sur ce **ContextNode**:

-   L’emplacement du [**ContextNode**](icontextnode.md) est correct.
-   Le type de [**ContextNode**](icontextnode.md) est correct.
-   Toutes les autres informations sur ce [**ContextNode**](icontextnode.md) sont stockées ailleurs.

Sur la base de ces trois règles, si et quand le [**InkAnalyzer**](inkanalyzer.md) a besoin d’informations supplémentaires sur un [**ContextNode**](icontextnode.md) , il déclenchera l’événement [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) et référencera le **ContextNode** en question. Cela donne à l’application la possibilité de définir toutes les informations connues sur ce **ContextNode** avant que le **InkAnalyzer** ne les examine plus en détail. Après la gestion d’un événement **PopulateContextNode** , le **ContextNode** en question doit avoir une propriété Location valide, le nombre correct de sous-nœuds définis s’il s’agit d’un conteneur **ContextNode** ou avoir les traits corrects définis à l’aide de [**SetStrokes**](icontextnode-setstrokes.md), s’il s’agit d’une feuille d’entrée manuscrite **ContextNode**. Si vous ne définissez pas correctement cet emplacement et les informations sur le sous-nœud ou le trait, une exception **InvalidOperation** se produira. Les sous-nœuds d’un conteneur **ContextNode** peuvent eux-mêmes être définis comme partiellement remplis, auquel cas davantage d’événements **PopulateContextNode** sont déclenchés si le **InkAnalyzer** détermine qu’ils seront nécessaires pour l’opération d’analyse en cours.

Les tableaux ci-dessous décrivent le moment où l’événement [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) est déclenché tout au long de l’utilisation de [**InkAnalyzer**](inkanalyzer.md).

Une fois que le [**InkAnalyzer**](inkanalyzer.md) a calculé des résultats, il revient à l’application pour mettre à jour les résultats. Le premier événement déclenché est l’événement [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Cet événement signifie simplement que l’application que l’état de l’arborescence de l’objet **InkAnalyzer** va changer. Cela offre aux applications la possibilité de définir l’indicateur [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) sur true sur tout [**ContextNodes**](icontextnodes.md) dont l’État est stocké ailleurs. **InkAnalyzer** déclenchera ensuite une série d’événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) pour déterminre l’état actuel des données. Une fois determiend, une opération de réconciliation est commise pour déterminer les résultats de l’arrière-plan qui peuvent toujours être appliqués.

Pour appliquer des résultats à [**InkAnalyzer**](inkanalyzer.md) , une série d’événements de modification d’arborescence sont déclenchés. Les événements de modification d’arborescence décrivent, pas à pas, toutes les modifications nécessaires pour mettre à jour les résultats. Ces événements sont destinés à être gérés dans sucession sans interuption ou à annuler. Si l’opération d’analyse est annulée (par le biais de la méthode [**Abort**](iinkanalyzer-abort.md) ) pendant le traitement des événements de modification de l’arborescence, l’état du **InkAnalyzer** n’est pas valide et le document entier peut nécessiter une réanalyse.

Les tableaux ci-dessous décrivent le moment où les événements de modification d’arborescence sont déclenchés tout au long de l’utilisation de InkAnalyzer. Les tables font référence aux horodateurs présentés ci-après.

![IImage présentant le flow entre l’interface utilisateur de l’application et l’analyseur d’arrière-plan](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Ajout d’un trait



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 et T9<br/> | \[À l’intérieur de l’appel à l' \] \[ événement d’exploration d’arborescence AddStroke ()\]<br/> | Événement [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenché<br/> | Il peut y avoir n événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenchés en fonction du nombre d’événements [**ContextNodes**](icontextnodes.md) non **classifiés** avec une valeur [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) définie sur true.<br/> |
| T1, T5 et T9<br/> | \[Événement de modification d’arborescence\]<br/>                                  | Événement [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) déclenché<br/>   | Un seul événement [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) est déclenché suite à l’appel de la méthode [**AddStroke**](iinkanalyzer-addstroke.md) . Tous les traits sont ajoutés au même [**ContextNode**](icontextnode.md)non classifié.<br/>                      |



 

### <a name="deleting-a-stroke"></a>Suppression d’un trait



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 et T10<br/> | \[À l’intérieur de [](iinkanalyzer-removestroke.md)l’appel à l' \] \[ événement d’exploration d’arborescence RemoveStroke ()\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Événement déclenché<br/> | Il peut y avoir un certain nombre d’événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenchés en fonction du nombre de [**ContextNodes**](icontextnodes.md) liés aux traits en cours de suppression, avec la valeur [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) true.<br/> |
| T2, T6 et T10<br/> | \[Événement de modification d’arborescence\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Événement déclenché<br/> | Il peut y avoir un nombre quelconque d’événements [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) déclenchés, en fonction du contenu de l’encre en cours de suppression et de la structure d’analyse actuelle.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Appel de la méthode BackgroundAnalyze



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[À l’intérieur de [](iinkanalyzer-backgroundanalyze.md)l’appel à l' \] \[ événement d’exploration d’arborescence BackgroundAnalyze ()\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Événement déclenché<br/> | Il peut y avoir n événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenchés, selon le nombre de [**ContextNodes**](icontextnodes.md) dans l’arborescence ayant la valeur [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) true (un événement par [**ContextNode**](icontextnode.md) nécessaire dans l’opération d’analyse actuelle).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Après le retour de l’appel à BackgroundAnalyze ()



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 à T7<br/>   | \[Événements déclenchés par le thread BG\]<br/> | Événement d’activité déclenché<br/> | Plusieurs événements d’activité sont déclenchés pendant la période d’analyse en arrière-plan.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Quand les IntermediateResults sont prêts



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 à T8<br/>   | \[Événements déclenchés par le thread BG, signifiant le début de la première opération de rapprochement\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Événement déclenché<br/>         | Un seul événement [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) déclenché. Cet événement est déclenché avant l’inspection de l’état du [**InkAnalyzer**](inkanalyzer.md), ce qui donne à l’application la possibilité de définir la valeur [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) sur tous les nœuds ou d’effectuer tout verrouillage de document local nécessaire.<br/> |
| T7 à T8<br/>   | \[Événement d’exploration d’arborescence\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Événement déclenché<br/>                   | Il peut y avoir n événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                               |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Événement déclenché<br/>                     | Il peut y avoir n événements [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                                 |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Événement déclenché<br/>                   | Il peut y avoir n événements [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                               |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Il peut y avoir n événements [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                               |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Il peut y avoir n événements [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                         |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Il peut y avoir n événements [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                                     |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Il peut y avoir n événements [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                           |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Il peut y avoir n événements [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                       |
| T7 à T8<br/>   | \[Événement de modification d’arborescence\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Événement déclenché<br/> | Il peut y avoir n événements [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) déclenchés, en fonction du contenu de l’encre. Les **ContextNodePropertiesUpdated** sont planifiés de générées une fois que tous les autres événements de modification [**ContextNode**](icontextnode.md) ont été déclenchés pendant cette période de [**rapprochement**](iinkanalyzer-reconcile.md) .<br/>              |
| T7 à T8<br/>   | \[L’événement désigne la fin de la première opération de rapprochement\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Événement déclenché<br/>                        | Un seul événement [**IntermediateResults**](-ianalysisevents-intermediateresults.md) est déclenché par opération d’analyse.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Après la gestion de IntermediateResults



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 à T11<br/>  | \[Événements déclenchés par le thread BG\]<br/> | [**Activité**](-ianalysisevents-activity.md) Événement déclenché<br/> | Plusieurs événements d' [**activité**](-ianalysisevents-activity.md) sont déclenchés pendant la période d’analyse en arrière-plan.<br/> |



 

### <a name="when-final-results-are-ready"></a>Quand les résultats finaux sont prêts



| Horodatage | Type d’événement ou objectif | Événement déclenché | Commentaire                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 à T12<br/> | \[Événements déclenchés par le thread BG, signifiant le début de la deuxième opération de rapprochement\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Événement déclenché<br/>         | Un seul événement [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) déclenché. Cet événement est déclenché avant l’inspection de l’état du [**InkAnalyzer**](inkanalyzer.md), ce qui donne à l’application la possibilité de définir la valeur [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) sur tous les nœuds ou d’effectuer tout verrouillage de document local nécessaire.<br/> |
| T11 à T12<br/> | \[Événement d’exploration d’arborescence\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Événement déclenché<br/>                   | Il peut y avoir un nombre quelconque d’événements [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                             |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Événement déclenché<br/>                     | Il peut y avoir un nombre quelconque d’événements [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                               |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Événement déclenché<br/>                   | Il peut y avoir un nombre quelconque d’événements [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                             |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Il peut y avoir un nombre quelconque d’événements [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                             |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Il peut y avoir un nombre quelconque d’événements [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                       |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Il peut y avoir un nombre quelconque d’événements [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                                   |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Il peut y avoir un nombre quelconque d’événements [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                         |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Il peut y avoir un nombre quelconque d’événements [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) déclenchés, en fonction du contenu de l’encre.<br/>                                                                                                                                                                                                                                     |
| T11 à T12<br/> | \[Événement de modification d’arborescence\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Événement déclenché<br/> | Il peut y avoir un nombre quelconque d’événements [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) déclenchés, en fonction du contenu de l’encre. Les **ContextNodePropertiesUpdated** sont planifiés de générées une fois que tous les autres événements de modification [**ContextNode**](icontextnode.md) ont été déclenchés pendant cette période de [**rapprochement**](iinkanalyzer-reconcile.md) .<br/>            |
| T11 à T12<br/> | \[L’événement désigne la fin de la deuxième opération de rapprochement\]<br/>                            | [**Résultats**](-ianalysisevents-results.md) Événement déclenché<br/>                                                | Un seul événement [**results**](-ianalysisevents-results.md) est déclenché par opération d’analyse.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




