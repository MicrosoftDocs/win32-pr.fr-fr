---
title: Recherche Active Directory
description: Une fonction importante de Active Directory consiste à résoudre les requêtes de données pour les utilisateurs, ainsi que les données de configuration pour les ordinateurs et les services.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Recherche Active Directory ADSI
- ADSI ADSI, recherche Active Directory
- interroge ADSI, en recherchant Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309218"
---
# <a name="searching-active-directory"></a>Recherche Active Directory

Une fonction importante de Active Directory consiste à résoudre les requêtes de données pour les utilisateurs, ainsi que les données de configuration pour les ordinateurs et les services. Pour écrire des requêtes efficaces pour Active Directory, il est utile de vous familiariser avec les éléments suivants :

-   Détermination de l’étendue de la requête : le client doit-il Rechercher des propriétés pour les objets qui peuvent se trouver n’importe où dans une forêt, ou uniquement dans un domaine, ou dans une unité d’organisation (UO) donnée ?
-   Détermination de la profondeur de la requête : la requête doit-elle effectuer une recherche uniquement dans un niveau ou peut-elle traverser d’autres annuaires LDAP ?
-   Performances et gestion des jeux de résultats volumineux : comment le client doit-il gérer efficacement le potentiel d’un jeu de résultats volumineux ?
-   Détermination des meilleures requêtes : Quels types de requêtes fournissent les résultats les plus efficaces ? Quels types de requêtes le développeur doit-il éviter ?
-   Compréhension de la syntaxe de requête : ADSI prend en charge la syntaxe LDAP comme indiqué dans RFC 2254, ainsi qu’un sous-ensemble de SQL.
-   Choix des interfaces : ADSI offre une prise en charge OLE DB, ainsi qu’une interface C/C++ appelée [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). Étant donné que l’interface ADSI fonctionne pour plusieurs espaces de noms, vous pouvez utiliser ces interfaces pour interroger d’autres espaces de noms tels qu’Exchange, ainsi que Active Directory. Étant donné que l’objet ADO (ActiveX Data Object) est un modèle objet d’accès aux données simple et scriptable par-dessus OLE DB, les interfaces OLE DB fonctionnent bien pour les programmeurs Visual Basic et les rédacteurs de script de page Web. Les nouvelles fonctionnalités d’accès aux données dans les applications Visual Studio et Office qui tirent parti d’ADO et de OLE DB peuvent désormais accéder aux données Active Directory de la même manière qu’elles accèdent aux données d’autres fournisseurs OLE DB, telles que les SQL Server. Toutefois, si un développeur C/C++ doit effectuer une recherche d’annuaire simple, l’interface **IDirectorySearch** peut être plus appropriée que les interfaces de OLE DB.

Les rubriques suivantes expliquent comment effectuer des recherches Active Directory pour vous assurer que votre application émet la requête la plus efficace, en fonction des exigences du client :

-   [Étendue de la requête](scope-of-query.md)
-   [Performances et gestion des jeux de résultats volumineux](performance-and-handling-large-result-sets.md)
-   [Syntaxe de filtre de recherche](search-filter-syntax.md)
-   [Interfaces de requête](query-interfaces.md)
-   [Recherche de données binaires](searching-binary-data.md)
-   [Requête distribuée](distributed-query.md)

 

 




