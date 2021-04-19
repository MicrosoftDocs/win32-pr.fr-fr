---
description: L’API de regroupement pair combine la technologie de l’API du fournisseur d’espace de noms PNRP et l’API de graphique.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: À propos de l’API de regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543501"
---
# <a name="about-the-grouping-api"></a>À propos de l’API de regroupement

L’API de regroupement pair combine la technologie de l' [API du fournisseur d’espace de noms PNRP](pnrp-namespace-provider-api.md) et l' [API de graphique](graphing-api.md). Le regroupement ajoute les deux technologies suivantes :

-   Couche de multiplexage qui permet à plusieurs applications d’utiliser un graphique, un port et une base de données d’enregistrement.
-   La sécurité qui garantit que seuls les homologues invités à un groupe peuvent rejoindre et se connecter pendant toute la durée de vie d’un groupe.

Le regroupement offre une approche accessible et facile aux réseaux homologues en raison du flot d’appels simple et de la messagerie sécurisée. Cette API utilise PNRP pour la découverte de groupes et un fournisseur de sécurité standard basé sur l’infrastructure à clé publique au lieu de demander à un développeur d’en implémenter un. Toutefois, si votre application exige une plus grande flexibilité en termes d’options de sécurité, envisagez d’utiliser l' [API Graph](about-the-graphing-api.md).

Le tableau suivant répertorie les rubriques de cette section de l’API de regroupement :

| Rubrique                                                                | Description                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Utilisation des groupes](how-to-work-with-groups.md)               | Décrit le workflow d’appel dans une application de regroupement d’homologues du démarrage à l’arrêt.         |
| [Fonctionnement de la sécurité de groupe](how-group-security-works.md)             | Décrit le mode de sécurisation de l’appartenance aux groupes homologues et des échanges de données.                      |
| [Invitation d’un pair à un groupe](inviting-a-peer-to-a-group.md)         | Décrit le processus par lequel les homologues sont invités et ajoutés à un groupe homologue.              |
| [Comment se connecter à un groupe homologue](how-to-connect-to-a-peer-group.md) | Décrit comment un homologue se connecte à un groupe homologue et interagit avec lui.                        |
| [Gestion des enregistrements de groupe](managing-group-records.md)                 | Décrit les enregistrements de groupe homologue et comment les gérer en tant que membre et en tant qu’administrateur. |



 

> [!Note]  
> Les applications qui utilisent l’API de regroupement dans un environnement avec un pare-feu nécessitent des groupes d’exceptions qui couvrent le port propre à l’application, ainsi que le port « 3587-TCP » pour l’API de regroupement et le port « 3540-UDP » pour PNRP. Ces groupes d’exceptions doivent être activés chaque fois que l’application est en cours d’exécution.

 

 

 



