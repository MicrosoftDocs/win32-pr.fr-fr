---
title: Interfaces de requête
description: Trois types d’interfaces ADSI peuvent être utilisés pour effectuer des recherches dans les répertoires. L’environnement de l’application et d’autres conditions peuvent indiquer l’interface utilisée.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfaces ADSI des interfaces de requête
- Requêtes ADSI, interfaces de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839145"
---
# <a name="query-interfaces"></a>Interfaces de requête

Trois types d’interfaces ADSI peuvent être utilisés pour effectuer des recherches dans les répertoires. L’environnement de l’application et d’autres conditions peuvent indiquer l’interface utilisée.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** est une interface com de base uniquement disponible pour les programmeurs C/C++. Pour plus d’informations, consultez [recherche à l’aide de l’interface IDirectorySearch](searching-with-idirectorysearch.md).
-   Objet. Les interfaces ADO (ActiveX Data Object) sont des interfaces d’automatisation qui utilisent OLE DB. Utilisez ADO pour les requêtes dans les applications qui reposent sur l’automatisation. Il s’agit notamment des applications Visual Basic, Active Server des pages, etc. Pour plus d’informations, consultez [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB est un ensemble d’interfaces C/C++ utilisées pour interroger des bases de données. En prenant en charge ces interfaces, les fournisseurs ADSI peuvent implémenter des fonctionnalités de OLE DB avancées, telles que des requêtes distribuées avec d’autres fournisseurs de OLE DB. Pour plus d’informations, consultez [recherche avec OLE DB](searching-with-ole-db.md).

 

 




