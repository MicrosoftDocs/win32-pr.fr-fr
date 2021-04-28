---
description: Rapport d’erreurs Windows l’enregistreur des étapes du problème
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Rapport d’erreurs Windows l’enregistreur des étapes du problème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084157"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Rapport d’erreurs Windows l’enregistreur des étapes du problème

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** – Windows 7  
**Serveurs** – Windows Server 2008 R2  


## <a name="description"></a>Description

Avant Windows 7, Rapport d’erreurs Windows (WER) a collecté des rapports d’erreurs qui indiquaient des problèmes nécessitant une réparation. Ces rapports d’erreurs contiennent des informations utiles qui décrivent la nature générale d’un problème, mais pas suffisamment d’informations pour en déterminer la cause racine. Pour cela, les développeurs ont besoin d’un outil pour reproduire le scénario de blocage/blocage du débogage.

Une nouvelle application, enregistreur des étapes du problème (PSR.exe), est livrée sur toutes les builds de Windows 7. Cette fonctionnalité active la collecte des actions effectuées par un utilisateur tout en rencontrant un incident afin que les testeurs et les développeurs puissent reproduire la situation pour l’analyse et le débogage.

## <a name="usage"></a>Utilisation

Actuellement, un développeur de service Rapport d’erreurs Windows doit demander l’activation d’un V.L.Q.P.R.D. pour une application ; Les organisations du support technique Microsoft utilisent également cet outil lors de la résolution des problèmes avec les utilisateurs finaux. Des plans sont en place pour rendre les V.Q.P.R.D. disponibles dans Windows Quality Online Services (winqual) après la sortie de Windows 7.

**Remarque :** Avec les V.Q.P.R.D. activés pour une application, l’application peut constater une dégradation des performances.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Entrée de blog Rapport d’erreurs Windows](/archive/blogs/wer/)
-   [Windows Quality Online Services (winqual)](https://winqual.microsoft.com)

 

 
