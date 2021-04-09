---
description: Comme mentionné dans vue d’ensemble de l’analyse de l’encre, la technologie d’analyse des encres gère en interne un modèle de document basé sur les arborescences pour contenir les résultats d’analyse et les relations.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy de données avec analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868298"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy de données avec analyse de l’encre

Comme mentionné dans [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre, la technologie d’analyse des encres gère en interne un modèle de document basé sur les arborescences pour contenir les résultats d’analyse et les relations. Si votre application a déjà un magasin de documents établi différent, vous devrez utiliser les fonctionnalités d’analyse de l’encre conçues pour effectuer un proxy de données entre différents modèles de document.

## <a name="types-of-data-proxy"></a>Types de proxy de données

Les fonctionnalités de proxy de données permettent à votre application d’effectuer les opérations suivantes :

-   Intégrer les données de résultats d’analyse dans un modèle de document existant.
-   Communiquez les résultats précédents (ou l’État) dans le [**InkAnalyzer**](inkanalyzer.md).
-   Communiquer l’état de non-encre dans le [**InkAnalyzer**](inkanalyzer.md).
-   Communiquez uniquement l’ensemble minimal de données (à la fois l’état précédent et non-Ink) nécessaire pour terminer l’opération d’analyse.
-   Mettez facilement à jour le modèle de document d’application interne avec les résultats d’analyse.

Il existe deux approches de base pour le proxy de données d’analyse d’encre. Les différences définissent les détails du moment et de la façon dont la synchronisation entre les modèles de document se produit. La première approche, mise à jour synchrone, requiert la modification du modèle de document d’analyse d’encre au fur et à mesure que des modifications se produisent dans le document de l’application. La deuxième approche, mise à jour à la demande, requiert uniquement les données affectées par les modifications apportées au modèle de document de l’application à passer au [**InkAnalyzer**](inkanalyzer.md). Autrement dit, seules les données des parties du modèle de document d’analyse d’encre qui se trouvent dans la même zone que les modifications apportées au document de l’application doivent être passées au **InkAnalyzer** comme il en a besoin.

### <a name="synchronous-update"></a>Mise à jour synchrone

L’approche de mise à jour synchrone requiert la modification (création et suppression) des nœuds dans la collection d’objets [**ContextNode**](icontextnode.md) de l’objet [**InkAnalyzer**](inkanalyzer.md) à mesure qu’ils se produisent dans le document de l’application. Par exemple, chaque fois qu’un mot de texte est ajouté à l’application, un **ContextNode** de type **TextWord** correspondant est créé dans le **InkAnalyzer**. Si l’emplacement du texte dans la page change, l’emplacement du **ContextNode** correspondant est mis à jour en même temps. Cette méthode est moins efficace en termes de ressources de calcul que la méthode à la demande, car chaque modification de document implique une mise à jour du **InkAnalyzer**, même si la modification n’affecte pas l’encre en cours d’analyse.

L’exemple suivant est destiné à illustrer le fonctionnement de la mise à jour synchrone. Imaginez une application qui a un modèle de document existant. Lorsque l’utilisateur final apporte une modification au document, telle que l’ajout d’un nouveau texte, la modification est traitée comme suit :

1.  L’utilisateur final crée les nouvelles données.
2.  L’application détermine la façon de traiter les données, de les stocker et de les restituer.
3.  Pour des raisons pratiques, les étapes suivantes se produisent simultanément.
    1.  L’application place les données dans son modèle de document.
    2.  L’application crée un [**InkAnalyzer**](inkanalyzer.md) et le met à jour. Cela permet de s’assurer que le **InkAnalyzer** dispose toujours des informations les plus récentes.
    3.  L’application appelle [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) sur [**InkAnalyzer**](inkanalyzer.md) pour commencer l’analyse.
4.  Une série d’événements est déclenchée si la modification implique une entrée manuscrite et que le [**InkAnalyzer**](inkanalyzer.md) détermine de nouveaux résultats. Un événement est déclenché pour chaque modification apportée à la collection d’objets [**ContextNode**](icontextnode.md) dans le **InkAnalyzer**. Ces événements sont les suivants : [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)et [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md). L’application gère ces événements pour replacer les résultats de l’opération d’analyse dans le modèle de document, le cas échéant.
5.  L’application met à jour la disposition du document, en extrayant les nouvelles données du modèle de document.
6.  Les nouvelles données sont restituées à l’utilisateur final.

### <a name="on-demand-update"></a>Mise à jour à la demande

L’approche à la demande nécessite uniquement que les données soient transmises pour les objets [**ContextNode**](icontextnode.md) qui sont dans les zones en cours d’analyse. Les objets **ContextNode** nécessaires sont extraits du modèle de document de l’application juste après l’appel de l’opération d’analyse, et à nouveau juste avant de rapprocher les résultats. Bien qu’elles soient plus compliquées à implémenter que les mises à jour synchrones, cette approche permet d’obtenir de meilleurs résultats en matière de performances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de l’analyse de l’encre](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer, classe (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft. Ink. InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft. Ink. ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
