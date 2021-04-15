---
title: Choix de la technologie de recherche
description: Cette rubrique contient la liste des technologies utilisées pour rechercher des Active Directory.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- Rechercher des technologies dans Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462919"
---
# <a name="choosing-the-search-technology"></a>Choix de la technologie de recherche

Les technologies, listées dans le tableau suivant, peuvent être utilisées pour effectuer des recherches dans Active Directory Domain Services.



| Technology                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | La classe [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) est fournie par l’espace de noms [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) pour permettre la recherche dans Active Directory Domain Services avec .NET Framework. Pour plus d’informations, consultez [recherche dans l’annuaire](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**Rubrique IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI fournit l’interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour interroger un serveur de Active Directory, ainsi que d’autres services d’annuaire tels que NDS, à l’aide de LDAP. **IDirectorySearch** est une interface com qui retourne des données richement typées, telles qu’un entier, une chaîne d’octets, une chaîne, un descripteur de sécurité, une heure UTC, un grand entier ou une valeur booléenne. Pour plus d’informations sur l’utilisation de **IDirectorySearch**, consultez [recherche à l’aide de l’interface IDirectorySearch](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB est un ensemble d’interfaces COM qui fournissent aux applications un accès uniforme aux données stockées dans diverses sources de données, quel que soit leur emplacement ou leur type. ADSI fournit également un fournisseur OLE DB pour ADSI qui permet aux applications d’utiliser OLE DB pour accéder aux Active Directory Domain Services. Le fournisseur d’OLE DB ADSI utilise les interfaces [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour envoyer des requêtes à Active Directory Domain Services et collecter les résultats.<br/>                                     |
| ADO et d’autres technologies d’accès aux données basées sur les OLE DB<br/>                 | Le fournisseur d’OLE DB ADSI permet à toute technologie d’accès aux données basée sur OLE DB, telle qu’ADO, d’effectuer des recherches dans Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| API LDAP<br/>                                                            | Les contrôleurs de domaine Windows 2000 sont des serveurs d’annuaire compatibles avec LDAP version 3. L’API LDAP est une bibliothèque de fonctions de style C. Les applications peuvent utiliser l’API LDAP pour effectuer des recherches dans Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                              |



 

Tenez compte des éléments suivants lors du choix d’une technologie :

-   Pour Microsoft Visual Basic et Visual Basic Scripting Edition (VBScript), ADO est recommandé.
-   Pour C/C++, vous pouvez choisir n’importe laquelle des technologies.
-   Si votre application utilise largement ADSI, il peut être plus simple d’utiliser [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Si vous utilisez [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pour gérer des objets dans Active Directory Domain Services, utilisez **IDirectorySearch** pour faciliter la gestion des propriétés renvoyées par la recherche. **IDirectorySearch** utilise les mêmes structures [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que **IDirectoryObject** pour représenter les propriétés. De plus, **IDirectorySearch** est exposé sur presque tous les objets com ADSI. Si vous avez un pointeur vers un objet COM ADSI, vous pouvez appeler **QueryInterface** pour obtenir un pointeur **IDirectorySearch** que vous pouvez utiliser pour effectuer une recherche à partir de l’objet d’annuaire représenté par l’objet com ADSI.
-   Si votre application utilise déjà OLE DB, ADO ou l’API LDAP, vous pouvez continuer à utiliser ces technologies pour effectuer des recherches dans Active Directory Domain Services.
-   Si votre application doit joindre des données à partir d’un service de domaine Active Directory et d’une base de données SQL Server 7, utilisez OLE DB. En utilisant OLE DB, votre application peut effectuer des requêtes distribuées qui font référence à des Active Directory Domain Services et des tables et des ensembles de lignes à partir d’une ou plusieurs bases de données Microsoft SQL Server 7.

 

