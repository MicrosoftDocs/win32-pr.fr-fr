---
title: Utilisation des interfaces de service Active Directory
description: Les interfaces de service Active Directory (ADSI) permettent aux applications clientes des services d’annuaire d’utiliser un ensemble d’interfaces pour communiquer avec n’importe quel espace de noms qui fournit une implémentation ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Utilisation des interfaces de service Active Directory ADSI
- ADSI ADSI, utilisation
- Interfaces ADSI (Active Directory Service Interfaces), utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839118"
---
# <a name="using-active-directory-service-interfaces"></a>Utilisation des interfaces de service Active Directory

Les interfaces de service Active Directory (ADSI) permettent aux applications clientes des services d’annuaire d’utiliser un ensemble d’interfaces pour communiquer avec n’importe quel espace de noms qui fournit une implémentation ADSI. Les clients ADSI utilisent les interfaces de service Active Directory bien définies à la place des appels d’API spécifiques au réseau pour obtenir un accès plus simple aux services d’un espace de noms.

Active Directory interfaces de service sont conformes au modèle COM (Component Object Model) et prennent en charge les fonctionnalités COM standard.

ADSI fournit des interfaces qui sont conformes à l’automatisation pour les contrôleurs liés au nom tels que Java, Microsoft Visual Basic Development System et Visual Basic Scripting Edition (VBScript). ADSI peut également fournir une interface qui peut optimiser les performances pour les interfaces qui ne sont pas conformes à Automation, à utiliser avec des environnements de langage tels que C et C++.

ADSI fournit également les interfaces non-Automation, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) et [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), pour prendre en charge la gestion et les requêtes d’objets d’annuaire.

En outre, l’interface ADSI fournit son propre fournisseur de OLE DB, de sorte que tout client qui utilise déjà OLE DB, y compris ceux qui utilisent ActiveX Data Objects, peut interroger directement les services d’annuaire.

Les applications Web qui utilisent des pages de Active Server peuvent également programmer l’accès aux services d’annuaire par le biais d’ADSI.

Les clients ADSI peuvent découvrir par programmation tous les fournisseurs ADSI sur un site et utiliser les mêmes interfaces pour communiquer avec chaque espace de noms. Au fur et à mesure que des fournisseurs supplémentaires sont installés, les clients ADSI peuvent communiquer, sans recompilation, avec les nouveaux espaces de noms.

Ce guide de programmation décrit le fonctionnement d’ADSI et fournit des informations pour effectuer des tâches spécifiques dans ADSI. Les rubriques suivantes sont présentées :

-   [Liaison à un objet ADSI](binding-to-an-adsi-object.md)
-   [Création et suppression d’objets](creating-and-deleting-objects.md)
-   [Accès et manipulation de données avec ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Utilisation du schéma ADSI](using-the-adsi-schema.md)
-   [Collections et groupes](collections-and-groups.md)
-   [Énumération des objets ADSI](enumerating-adsi-objects.md)
-   [Recherche Active Directory](searching-active-directory.md)
-   [Modèle de sécurité ADSI](adsi-security-model.md)
-   [Extensions ADSI](adsi-extensions.md)
-   [Utilisation d’ADSI avec Exchange](using-adsi-with-exchange.md)
-   [Interfaces de l’utilitaire ADSI](adsi-utility-interfaces.md)
-   [Programmation d’ADSI avec Java/COM](programming-adsi-with-javacom.md)

 

 




