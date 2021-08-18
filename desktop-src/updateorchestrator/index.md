---
title: Mettre à jour l’API Orchestrator
description: UpdateOrchestrator planifie vos mises à jour logicielles automatiques en tenant compte de l’impact de l’utilisateur.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: 6460446397af168a4098a7203179d5587d4dcd9a3cea813991648a5083d07334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966098"
---
# <a name="updateorchestrator-api"></a>API UpdateOrchestrator

**UpdateOrchestrator** planifie vos mises à jour logicielles automatiques en tenant compte de l’impact de l’utilisateur. Cette API vous permet de planifier le téléchargement et l’installation automatiques, ainsi que leurs besoins afin d’exécuter des mises à jour à un moment optimal qui réduit l’impact sur l’utilisateur. Ces fonctionnalités sont particulièrement utiles pour réduire les systèmes de performances avec des ressources informatiques limitées ou lentes.

Windows 19H1 comprend une solution de première génération pour les cas d’utilisation de mises à jour logicielles automatiques qui ont été adoptées par les mises à jour du système d’exploitation et qui exposent une version initiale de « accès limité » de cette API pour un ensemble sélectionné de mises à jour d’applications « en mode utilisateur », comme décrit ci-dessous.

## <a name="features"></a>Fonctionnalités

- Inscrit dynamiquement les mises à jour logicielles
 
- Appelle les mises à jour logicielles inscrites pendant les périodes optimales, par exemple lors de l’absence de l’utilisateur, pour mettre à jour les « applications en mode utilisateur ».
    - Offre la possibilité de « rester éveillé » sur secteur pour réduire encore davantage l’impact sur l’utilisateur.

- Opère sur un modèle d’approbation qui appelle uniquement des mises à jour logicielles approuvées tierces approuvées
    - L’exposition de UpdateOrchestrator à tous les appelants, tels que la mise à jour du microprogramme BIOS ou des pilotes lorsqu’un utilisateur n’est pas présent, présente des risques substantiels.  UpdateOrchestrator comprend un modèle d’approbation pour atténuer ces risques.

## <a name="developer-audience"></a>Public de développeurs

> [!IMPORTANT]
> L’API UpdateOrchestrator est actuellement une [fonctionnalité d’accès limité](/uwp/api/windows.applicationmodel.limitedaccessfeatures). Cette API sera rendue publiquement disponible dans une version ultérieure.

Utilisez l’API UpdateOrchestrator si vous avez déjà des mises à jour logicielles en arrière-plan pour les applications en mode utilisateur Win32, telles que le programme de mise à jour d’Adobe pour Acrobat Reader ou la vaporisation de la vanne. cette interface n’est pas nécessaire pour les applications UWP/Store, car la Microsoft Store tire déjà parti de cette fonctionnalité pour les mises à jour logicielles.

Pour offrir la meilleure expérience client, cette version d’API initiale est étendue à un ensemble sélectionné de mises à jour inscrites qui répondent aux critères suivants :

- Mises à jour pour les applications « en mode utilisateur » uniquement
- Ne pas impliquer le BIOS, le microprogramme, le périphérique ou les pilotes logiciels
    - La mise à jour du BIOS, du microprogramme ou des pilotes de périphérique/logiciel qui n’ont pas passé un critère de qualité commun pose un risque substantiel, en particulier lorsqu’un utilisateur n’est pas présent. 
- Le fait de participer à l’utilisation de cette API implique la possibilité de disposer de tous les contenus téléchargés et installés par vos programmes de mise à jour en arrière-plan sur les systèmes des utilisateurs via des audits. 

Cette API peut être modifiée de manière significative avant la publication publique.   Lorsque l’API UpdateOrchestrator est en cours de développement, cette version initiale en tant que fonctionnalité d’accès limité est uniquement pour les mises à jour qui répondent aux critères ci-dessus pour l’instant.

Notre objectif est d’améliorer les fonctionnalités de cette API et de réduire l’impact de plusieurs mises à jour logicielles automatiques sur Windows. Nous apprécions votre contribution dans ce [**bref questionnaire**](https://aka.ms/UOAPISurvey) pour nous aider à comprendre comment l’API UpdateOrchestrator peut mieux répondre à vos besoins en matière de développement.

