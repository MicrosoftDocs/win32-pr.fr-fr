---
title: Interfaces ADSI
description: Cette rubrique décrit les catégories utilisées pour les interfaces ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI des interfaces ADSI
- ADSI ADSI, référence, interfaces
- interfaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75463a2b9ce70013482d2abee4f21ff786e7914cff0fefe691c562c4f39edb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023817"
---
# <a name="adsi-interfaces"></a>Interfaces ADSI

Les interfaces de service Active Directory (ADSI) prennent en charge un ensemble complet d’interfaces qui peuvent être classées en fonction des catégories suivantes :

-   [Cœur](core-interfaces.md). Ces interfaces fournissent les fonctions de base de gestion des objets ADSI. Les fonctions principales incluent la fourniture d’un point d’entrée dans un magasin d’annuaires, le chargement des propriétés dans le cache de propriétés et la validation des modifications dans l’annuaire sous-jacent.
-   [Schéma](schema-interfaces.md). Ces interfaces fournissent des méthodes pour la gestion et l’extension du schéma d’annuaire.
-   [Cache de propriétés](property-cache-interfaces.md). Ces interfaces définissent des méthodes de manipulation des propriétés dans le cache de propriétés.
-   [Objet persistant](persistent-object-interfaces.md). Ces interfaces manipulent les données persistantes dans l’espace de noms du service d’annuaire sous-jacent. Les objets ADSI implémentent ces types d’interfaces pour permettre l’accès à leurs données persistantes, y compris les comptes d’utilisateur, les partages de fichiers, les hiérarchies organisationnelles et les listes de travaux dans une file d’attente à l’impression.
-   [Objet dynamique](dynamic-object-interfaces.md). Ces interfaces fonctionnent avec Dynamic Data dans un service d’annuaire. Les objets d’annuaire non représentés dans le service d’annuaire sous-jacent implémentent ces interfaces. Les commandes émises sur un réseau sont des exemples de données dynamiques.
-   [Sécurité](security-interfaces.md). Ces interfaces permettent à un client ADSI d’établir ses informations d’identification sur un serveur et d’utiliser les fonctionnalités de sécurité prises en charge par le service d’annuaire, telles que la liste de contrôle d’accès ou les descripteurs de sécurité.
-   [Non Automation](non-automation-interfaces.md). Ces interfaces permettent aux clients non-Automation (par exemple, les applications C/C++) un accès à faible charge aux objets d’annuaire en fournissant un accès vtable aux méthodes de gestion et de recherche d’objets de service d’annuaire.
-   [Extension](extension-interfaces.md). Ces interfaces permettent aux clients ADSI d’étendre les fonctionnalités des classes ADSI existantes pour offrir des solutions personnalisées aux services d’annuaire.
-   [Utilitaire](utility-interfaces.md). Ces interfaces fournissent des fonctions d’assistance avancées pour la gestion des objets ADSI.
-   [Type de données](data-type-interfaces.md). Ces interfaces fournissent des méthodes pour accéder aux types de données ADSI.

 

 




