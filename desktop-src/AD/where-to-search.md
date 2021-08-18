---
title: Choix de l’emplacement de recherche
description: Cette rubrique explique les différentes recherches qui peuvent être effectuées dans Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Choix de l’emplacement où rechercher les annonces
- Active Directory AD, recherche, choix de l’emplacement de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024317"
---
# <a name="deciding-where-to-search"></a>Choix de l’emplacement de recherche

Cette rubrique explique les différentes recherches qui peuvent être effectuées dans Active Directory Domain Services.

Toutes les recherches sont effectuées dans l’un des contextes de nommage suivants :

-   Domaine, y compris les partitions d’annuaire d’applications
-   Conteneur de schéma
-   Conteneur de configuration
-   Catalogue global

## <a name="searching-a-domain"></a>Recherche dans un domaine

Les domaines contiennent la plupart des objets hautement utilisés tels que les utilisateurs, les contacts, les groupes, les unités d’organisation, les ordinateurs, etc. La plupart des requêtes effectuent une recherche dans un domaine. Pour plus d’informations sur la recherche d’un domaine, consultez [recherche de contenu de domaine](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Recherche dans le conteneur de schéma

Le conteneur de schéma contient les objets [**classSchema**](/windows/desktop/ADSchema/c-classschema) et [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) qui fournissent la définition formelle de chaque classe et attribut qui peut exister dans Active Directory Domain Services. Pour rechercher des objets dans le conteneur de schéma, connectez-vous au conteneur de schéma sur n’importe quel contrôleur de domaine. Le conteneur de schéma est disponible sur tous les contrôleurs de domaine. Le nom unique du conteneur de schéma est obtenu à partir de l’attribut **schemaNamingContext** de rootDSE. Pour plus d’informations sur rootDSE et l’attribut **schemaNamingContext** , consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).

Pour plus d’informations sur la lecture à partir du conteneur de schéma ou de schéma abstrait, consultez [instructions pour la liaison au schéma](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Recherche dans le conteneur de configuration

Le conteneur de configuration contient des informations de configuration, telles que les sites, les services et les spécificateurs d’affichage, pour l’ensemble de la forêt. Pour rechercher des objets dans le conteneur de configuration, connectez-vous au conteneur de configuration sur n’importe quel contrôleur de domaine. Le conteneur de configuration est disponible sur tous les contrôleurs de domaine. Le nom unique du conteneur de configuration est obtenu à partir de l’attribut **configurationNamingContext** de rootDSE. Pour plus d’informations sur rootDSE et l’attribut **configurationNamingContext** , consultez [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Recherche dans le catalogue global

Le catalogue global contient un réplica de chaque objet dans Active Directory Domain Services, mais avec seulement un petit nombre de leurs attributs. Les attributs du catalogue global sont ceux qui sont utilisés le plus fréquemment dans les opérations de recherche, comme le prénom et le nom d’un utilisateur, les noms de connexion, etc. Pour plus d’informations sur la recherche dans le catalogue global, consultez [recherche dans le catalogue global](searching-global-catalog-contents.md).

 

 