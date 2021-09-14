---
description: L’infrastructure homologue est un ensemble de plusieurs API qui sont puissantes et flexibles.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Qu’est-ce que l’infrastructure homologue ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009195"
---
# <a name="what-is-the-peer-infrastructure"></a>Qu’est-ce que l’infrastructure homologue ?

L’infrastructure homologue est un ensemble de plusieurs API qui sont puissantes et flexibles. Les principaux composants sont les suivants :

-   [API graphique d’homologues](#peer-graphing-api)
-   [API de regroupement d’homologues](#peer-grouping-api)
-   [API du gestionnaire d’identités homologues](#peer-identity-manager-api)
-   [API du fournisseur d’espace de noms PNRP](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>API graphique d’homologues

L’infrastructure de pairs fournit une technologie graphique qui permet de transmettre des informations de manière efficace et fiable entre les pairs d’un graphique homologue. L' [API graphique d’homologue](graphing-api.md) garantit que chaque nœud dispose d’une vue cohérente des données dans un graphique.

Vous pouvez utiliser l' [API graphique d’homologues](graphing-api.md) pour effectuer les opérations suivantes :

-   Créer et gérer des graphiques homologues
-   Énumérer et interagir avec d’autres pairs dans un graphique homologue
-   Envoyer des données sous la forme d’un [enregistrement](records.md) à chaque nœud dans un graphique homologue

## <a name="peer-grouping-api"></a>API de regroupement d’homologues

L' [API de regroupement d’homologues](grouping-api.md) combine et améliore les API [PNRP](#pnrp-namespace-provider-api) et [graphique](#peer-graphing-api) de l’homologue, et ajoute les deux composants suivants :

-   Couche de multiplexage qui permet à plusieurs applications s’exécutant sur une entité homologue de se connecter à un groupe
-   Un modèle de sécurité spécifique qui garantit que seuls les homologues invités à un groupe peuvent se connecter au groupe tout au long de la durée de vie du groupe.

Vous pouvez utiliser l’API de regroupement d’homologues pour effectuer les opérations suivantes :

-   Créer et gérer des groupes homologues sécurisés
-   Énumérer et interagir avec d’autres pairs dans un groupe
-   Envoyer des données sous la forme d’un [enregistrement](records.md) à chaque nœud dans un groupe homologue

## <a name="peer-identity-manager-api"></a>API du gestionnaire d’identités homologues

À l’aide de l' [API du gestionnaire d’identités homologues](identity-manager-api.md) , vous pouvez créer des [noms d’homologues](peer-names.md) sécurisés que PNRP peut utiliser pour s’assurer qu’une personne publiant un nom possède officiellement le nom. Les noms d’homologues sont également appelés identités, et ils sont utilisés dans l’API de regroupement d’homologues pour identifier les individus d’un groupe.

Vous pouvez utiliser l' [API du gestionnaire d’identités homologues](identity-manager-api.md) pour effectuer les opérations suivantes :

-   Créer, énumérer et gérer des identités d’homologue.

## <a name="pnrp-namespace-provider-api"></a>API du fournisseur d’espace de noms PNRP

L’infrastructure homologue fournit une technologie de résolution de noms sans serveur appelée [API du fournisseur d’espace de noms PNRP](pnrp-namespace-provider-api.md). À l’aide de l’API du fournisseur d’espace de noms PNRP de Winsock 2, un homologue, un service, un appareil informatique et un point de terminaison de groupe pair peuvent gérer, inscrire, désinscrire et résoudre un autre point de terminaison dans un [Cloud](clouds.md)PNRP.

> [!Note]  
> PNRP est un acronyme pour le protocole PNRP ( **Peer Name Resolution Protocol**).

 

 

 



