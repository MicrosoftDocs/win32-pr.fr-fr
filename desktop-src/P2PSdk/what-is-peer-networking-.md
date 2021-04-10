---
description: Le réseau pair à pair est une technologie de mise en réseau sans serveur qui permet à plusieurs périphériques réseau de partager des ressources et de communiquer directement entre eux.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Qu’est-ce que le réseau homologue ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952024"
---
# <a name="what-is-peer-networking"></a>Qu’est-ce que le réseau homologue ?

Le réseau pair à pair est une technologie de mise en réseau sans serveur qui permet à plusieurs périphériques réseau de partager des ressources et de communiquer directement entre eux. Cette technologie est disponible pour Windows XP avec Service Pack 1 (SP1) et les clients ultérieurs qui exécutent le Pack de mise en réseau avancée pour l’infrastructure d’égal à égal.

L’infrastructure d’égal à égal est un ensemble d’API de mise en réseau pour vous aider à développer des applications de mise en réseau décentralisées qui utilisent la puissance collective des ordinateurs sur un réseau. Par exemple, les applications d’égal à égal peuvent être des communications collaboratives, des technologies de distribution de contenu, etc.

L’infrastructure d’égal à égal fournit une infrastructure de mise en réseau solide qui vous permet de vous concentrer sur le développement d’applications, car l’infrastructure est développée pour vous.

L’infrastructure d’égal à égal comprend les composants principaux suivants :

-   [Résolution de noms d’homologue évolutive et sécurisée](#scalable-and-secure-peer-name-resolution)
-   [Communication multipoint efficace](#efficient-multipoint-communication)
-   [Gestion des données distribuées](#distributed-data-management)
-   [Identités d’homologue sécurisées](#secure-peer-identities)
-   [Sécuriser les groupes d’égal à égal](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Résolution de noms d’homologue évolutive et sécurisée

L' [API du fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) est un protocole de résolution de nom à adresse IP. L’étendue ou le contexte IPv6 qui comprend tous les pairs participant est appelé [Cloud](clouds.md). PNRP permet aux pairs d’interagir entre eux au sein d’un Cloud.

## <a name="efficient-multipoint-communication"></a>Communication multipoint efficace

L’infrastructure d’égal à égal inclut l' [API graphique](graphing-api.md) qui fournit une communication multipoint efficace. Comme PNRP, la représentation graphique d’égal à égal permet à un ensemble de nœuds d’interagir et de transmettre des données de l’un à l’autre sous la forme d’un [enregistrement](records.md). Chaque enregistrement généré ou mis à jour par un homologue est envoyé à tous les nœuds d’un graphique.

## <a name="distributed-data-management"></a>Gestion des données distribués

La gestion distribuée des données stocke automatiquement tous les enregistrements envoyés à un graphique d’égal à égal jusqu’à la date et l’heure d’expiration spécifiées pour chaque enregistrement. La mise en réseau pair à pair garantit que chaque nœud d’un graphique d’égal à égal a une vue similaire de la base de données d’enregistrement. Si un modèle de sécurité est associé à un graphique d’égal à égal, le graphique contient les informations suivantes :

-   Qui peut et ne peut pas se connecter à un graphique
-   Qui peut sécuriser et valider les enregistrements en fonction de critères définis en externe

## <a name="secure-peer-identities"></a>Identités d’homologue sécurisées

L’infrastructure d’égal à égal fournit une [API de gestionnaire d’identité](identity-manager-api.md) d’égal à égal qui vous permet de créer, gérer et manipuler les identités d’homologue. Les identités homologues sont utilisées pour définir des noms pour les points de terminaison sécurisés dans PNRP et peuvent représenter n’importe quelle ressource participant à un réseau pair à pair, y compris des groupes et des services d’égal à égal sécurisés.

## <a name="secure-peer-to-peer-groups"></a>Sécuriser les groupes d’égal à égal

L' [API de regroupement](grouping-api.md) d’égal à égal combine les API de graphiques d’égal à égal, Identity Manager et PNRP pour former une solution cohérente et pratique pour le développement d’applications de réseau pair à pair. L’API de regroupement d’égal à égal utilise l’API du gestionnaire d’identité d’égal à égal et un schéma de certificat auto-signé pour garantir la sécurité au sein de l’infrastructure de graphiques. Chaque groupe peut être résolu et inscrit via PNRP, ce qui permet la résolution de noms d’homologues aléatoires au sein d’un groupe d’égal à égal inscrit. Un groupe peut être un point de terminaison dans PNRP, tout comme un homologue.

Pour obtenir une vue d’ensemble de l’infrastructure d’égal à égal, consultez l’article «[Présentation de la mise en réseau pair à pair de Windows XP](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)».

Pour obtenir une vue d’ensemble des API de l’infrastructure d’égal à égal, consultez la rubrique [qu’est-ce que l’infrastructure homologue ?](what-is-the-peer-infrastructure-.md).

 

 



