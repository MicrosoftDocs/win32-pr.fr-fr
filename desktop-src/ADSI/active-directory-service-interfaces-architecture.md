---
title: Architecture des interfaces de service Active Directory
description: De nombreux services d’annuaire sont hiérarchiques et se prêtent donc à un modèle d’objet hiérarchique. Cette section utilise des représentations d’objets COM pour illustrer différentes fonctionnalités d’ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Architecture des interfaces de service Active Directory ADSI
- ADSI ADSI, à propos de, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afbc212edbea6491de4cae89f2c8b7c873019b6d5678c5bf1d5b531f519260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024081"
---
# <a name="active-directory-service-interfaces-architecture"></a>Architecture des interfaces de service Active Directory

De nombreux services d’annuaire sont hiérarchiques et se prêtent donc à un modèle d’objet hiérarchique. Cette section utilise des représentations d’objets COM pour illustrer différentes fonctionnalités d’ADSI.

Dans la figure ci-dessous, un objet système de niveau supérieur contient un objet d’espace de noms pour chaque fournisseur ADSI installé.

![objet conteneur d’espaces de noms](images/ds2top.png)

Chacun des objets d’espace de noms est lui-même un conteneur qui contient les nœuds racine de niveau supérieur de chaque serveur, domaine ou tout autre type d’objets de système d’annuaire qui sont définis en tant que racines dans chaque service d’annuaire.

ADSI fournit un ensemble d’interfaces et d’objets prédéfinis afin que les applications clientes puissent interagir avec les services d’annuaire à l’aide d’un ensemble de méthodes uniformes. Toutefois, ADSI peut ne pas fournir l’accès à toutes les fonctionnalités d’un service d’annuaire. Pour mieux utiliser l’ensemble complet des fonctionnalités de chaque service d’annuaire, ADSI fournit un modèle de schéma que les fournisseurs de services d’annuaire et les fournisseurs de logiciels tiers peuvent utiliser pour étendre les fonctionnalités au-delà des interfaces fournies dans ADSI.

Les objets conteneurs de nœud racine, qui se trouvent dans chaque objet espace de noms de fournisseur, incluent un objet conteneur de schéma ADSI. Cet objet contient la définition de toutes les fonctionnalités de ce fournisseur. Pour plus d’informations, consultez [modèle de schéma ADSI](adsi-schema-model.md).

Cette section comprend les rubriques suivantes :

-   [Objets interfaces du service Active Directory](active-directory-service-interfaces-objects.md)
-   [Espaces de noms](namespaces.md)
-   [Fournisseur d’interfaces de service Active Directory](active-directory-service-interfaces-provider.md)
-   [Modèle de schéma ADSI](adsi-schema-model.md)

 

 




