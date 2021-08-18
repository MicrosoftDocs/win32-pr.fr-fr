---
title: Utilisation de WinSAT
description: vous pouvez utiliser l’API Windows System Assessment Tool (winsat) pour initier des évaluations formelles et ad hoc de la configuration matérielle de l’ordinateur, récupérer le score de base pour l’ordinateur et les scores pour chaque sous-composant de l’évaluation, et récupérer les détails de l’évaluation, tels que les détails du processeur qui a été évalué.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23cf26d31ccbd3eb6e51fb1717c055fb6538c57612d374b0a3b7a2a5b2382681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733779"
---
# <a name="using-winsat"></a>Utilisation de WinSAT

\[WinSAT peut être modifié ou non disponible pour les mises en production après Windows 8.1.\]

vous pouvez utiliser l’API Windows System Assessment Tool (winsat) pour [initier des évaluations formelles et ad hoc](#initiating-an-assessment) de la configuration matérielle de l’ordinateur, [récupérer le score de base pour l’ordinateur](#retrieving-the-scores-of-the-assessment) et les scores pour chaque sous-composant de l’évaluation, et [récupérer les détails de l’évaluation](#retrieving-details-of-the-assessment), tels que les détails du processeur qui a été évalué.

## <a name="initiating-an-assessment"></a>Lancement d’une évaluation

après Windows 8.1 vous pouvez lancer des évaluations formelles et ad hoc de l’ordinateur. Une évaluation formelle évalue les sous-composants suivants de l’ordinateur :

-   UC
-   Mémoire
-   Disque principal
-   Carte vidéo

Pour lancer une évaluation formelle, appelez la méthode [**IInitiateWinSATAssessment :: InitiateFormalAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) . Les résultats des évaluations formelles sont enregistrés dans le magasin d’évaluation et peuvent être récupérés à une date ultérieure.

En règle générale, vous utilisez des évaluations ad hoc pour évaluer un seul sous-composant de l’ordinateur, par exemple le processeur ou la mémoire. Toutefois, vous pouvez utiliser le commutateur **formel** pour évaluer tous les sous-composants. Pour lancer une évaluation ad hoc, appelez la méthode [**IInitiateWinSATAssessment :: InitiateAssessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) . Notez que les résultats des évaluations ad hoc ne sont pas enregistrés dans le magasin d’évaluation.

Pour récupérer une notification lorsque la progression est effectuée ou lorsque l’évaluation se termine, implémentez l’interface [**IWinSATInitiateEvents**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) .

Vous ne pouvez pas exécuter des évaluations formelles à distance ou sur un ordinateur qui s’exécute sur des batteries. Vous ne pouvez pas non plus exécuter à distance une évaluation ad hoc sur le sous-composant Graphics.

## <a name="retrieving-the-scores-of-the-assessment"></a>Récupération des scores de l’évaluation

Vous pouvez récupérer le score de base de l’ordinateur et le score pour chaque sous-composant de l’évaluation. Vous pouvez utiliser l’API pour récupérer les scores uniquement pour les évaluations formelles. Pour récupérer les scores pour les évaluations ad hoc, vous devez inclure l’argument **-XML** dans la ligne de commande pour enregistrer les résultats de l’évaluation dans un fichier XML, puis analyser le fichier pour le score du sous-composant.

Le score de base est une mesure générale de la configuration matérielle de l’ordinateur. Un score de base plus élevé signifie généralement que l’ordinateur sera plus performant et plus rapide qu’un ordinateur avec un score de base inférieur, en particulier lors de l’exécution de tâches plus avancées et gourmandes en ressources.

Chaque composant matériel reçoit un sous-score individuel. Le score de base de votre ordinateur est déterminé par le sous-score le plus bas. Par exemple, si le sous-score le plus bas d’un composant matériel individuel est 2,6, le score de base est 2,6. Le score de base n’est pas une moyenne des sous-scores combinés.

Un utilisateur peut utiliser le score de base pour acheter en toute confiance des programmes et autres logiciels qui sont mis en correspondance avec le score de base de leur ordinateur. par exemple, si l’ordinateur a un score de base de 3,3, l’utilisateur peut acheter en toute confiance tout logiciel conçu pour cette version de Windows qui nécessite un ordinateur dont le score de base est de 3 ou moins.

Pour récupérer le score de base, appelez d’abord la méthode [**IQueryRecentWinSATAssessment :: obtenir des \_ informations**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) pour obtenir l’interface [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Ensuite, appelez la méthode [**IProvideWinSATResultsInfo :: obten \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) pour récupérer le score de base.

Un utilisateur peut utiliser des scores de sous-composant pour déterminer si un sous-composant de l’ordinateur peut prendre en charge un type spécifique d’application. Par exemple, un utilisateur qui consacre plus de temps à lire ou écrire des documents peut exiger un score plus élevé pour le disque qu’un utilisateur qui exécute des applications scientifiques, et un utilisateur qui exécute des applications scientifiques souhaitera probablement un score de sous-composant plus élevé et peut ne pas se préoccuper d’un score de disque inférieur.

Pour récupérer le score pour chaque sous-composant, appelez d’abord la méthode [**IQueryRecentWinSATAssessment :: obtenir des \_ informations**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) pour obtenir l’interface [**IProvideWinSATResultsInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) . Appelez ensuite la méthode [**IProvideWinSATResultsInfo :: GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) pour accéder à l’interface [**IProvideWinSATAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) . Pour chaque sous-composant dont vous souhaitez récupérer le score, appelez la méthode [**IProvideWinSATAssessmentInfo :: obtenir \_ score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="retrieving-details-of-the-assessment"></a>Récupération des détails de l’évaluation

L’API WinSAT fournit le score de base global et les scores pour chaque sous-composant. Pour obtenir des détails sur l’évaluation (par exemple, les mesures utilisées pour calculer le score et les détails du processeur qui a été évalué), vous devez récupérer les données du document d’évaluation XML. Pour récupérer les détails de l’évaluation formelle la plus récente, appelez la méthode [**IQueryRecentWinSATAssessment :: obtenir \_ XML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) . Pour récupérer les détails de chaque évaluation dans le magasin de données WinSAT, appelez la méthode [**IQueryAllWinSATAssessments :: obtenir \_ AllXML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) .

Pour plus d’informations sur le schéma XML et les détails que vous pouvez récupérer, consultez [schéma WinSAT](winsat-schema.md).

 

 




