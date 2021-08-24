---
description: Rapport d'erreurs Windows Enregistreur des étapes du problème
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Rapport d'erreurs Windows Enregistreur des étapes du problème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba90b76b3d486dc0708e0803609539fda6d6141d0a6f3ab100ba0ce198846fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328081"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Rapport d'erreurs Windows Enregistreur des étapes du problème

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** – Windows 7  
**serveurs** – Windows Server 2008 R2  


## <a name="description"></a>Description

avant le Windows 7, Rapport d’erreurs Windows (WER) a collecté des rapports d’erreurs qui indiquaient des problèmes nécessitant une réparation. Ces rapports d’erreurs contiennent des informations utiles qui décrivent la nature générale d’un problème, mais pas suffisamment d’informations pour en déterminer la cause racine. Pour cela, les développeurs ont besoin d’un outil pour reproduire le scénario de blocage/blocage du débogage.

une nouvelle application, enregistreur des étapes du problème (PSR.exe), est livrée sur toutes les builds de Windows 7. Cette fonctionnalité active la collecte des actions effectuées par un utilisateur tout en rencontrant un incident afin que les testeurs et les développeurs puissent reproduire la situation pour l’analyse et le débogage.

## <a name="usage"></a>Usage

actuellement, un développeur de service Rapport d’erreurs Windows doit demander l’activation d’un v.l.q.p.r.d. pour une application ; Les organisations du support technique Microsoft utilisent également cet outil lors de la résolution des problèmes avec les utilisateurs finaux. des Plans sont en place pour rendre les v.q.p.r.d. disponibles dans Windows Quality Online Services (Winqual) après la sortie de Windows 7.

**Remarque :** Avec les V.Q.P.R.D. activés pour une application, l’application peut constater une dégradation des performances.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [entrée de blog Rapport d’erreurs Windows](/archive/blogs/wer/)
-   [Windows Services en ligne de qualité (winqual)](https://winqual.microsoft.com)

 

 
