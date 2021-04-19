---
description: La rubrique suivante décrit le fonctionnement de l’API de plateforme d’évaluation Windows As a service (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: À propos de la plateforme d’évaluation WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544903"
---
# <a name="about-the-waas-assessment-platform"></a>À propos de la plateforme d’évaluation WaaS

La rubrique suivante décrit le fonctionnement de l’API de plateforme d’évaluation Windows As a service (WaaS).

L’API d’évaluation de WaaS offre à l’appelant les informations suivantes :

-   Si un appareil se trouve sur les dernières mises à jour Microsoft.
-   Si l’appareil a atteint la fin du support.
-   Heures de publication des dernières mises à jour applicables pour l’appareil.
-   Évaluation de la raison pour laquelle un appareil n’est pas à jour et l’impact potentiel qu’il peut avoir sur l’appareil.

La plateforme d’évaluation WaaS utilise le modèle d’API COM et s’exécute automatiquement au moins une fois par jour. Ce cycle intercepte les informations de version applicables. Pendant la période mise en cache, les évaluations sont effectuées par rapport aux informations de version mises en cache. Si un appel est effectué en dehors de la fenêtre d’expiration du cache, un nouvel appel et une nouvelle évaluation sont effectués, mis en cache et retournés. Lorsqu’un appel est effectué, le client d’évaluation de WaaS contacte le service d’évaluation WaaS avec les attributs de l’appareil et reçoit un dossier d’informations qui s’applique à l’appareil. Le client utilise ensuite ces informations par rapport aux informations recueillies sur l’appareil pour effectuer l’évaluation.

> [!NOTE]
> Votre code doit disposer de privilèges d’administrateur pour appeler l’API d’évaluation WAAS. Pour plus d’informations sur le développement d’applications qui requièrent des privilèges d’administrateur, consultez [cet article](../secauthz/developing-applications-that-require-administrator-privilege.md).

 
