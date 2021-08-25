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
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637719"
---
# <a name="query-interfaces"></a>Interfaces de requête

Trois types d’interfaces ADSI peuvent être utilisés pour effectuer des recherches dans les répertoires. L’environnement de l’application et d’autres conditions peuvent indiquer l’interface utilisée.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** est une interface com de base uniquement disponible pour les programmeurs C/C++. Pour plus d’informations, consultez [recherche à l’aide de l’interface IDirectorySearch](searching-with-idirectorysearch.md).
-   Objet. les interfaces d’objets de données ActiveX (ADO) sont des interfaces d’automatisation qui utilisent des OLE DB. Utilisez ADO pour les requêtes dans les applications qui reposent sur l’automatisation. il s’agit notamment des applications Visual Basic, Active Server des Pages, etc. pour plus d’informations, consultez [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB est un ensemble d’interfaces C/C++ utilisées pour interroger des bases de données. En prenant en charge ces interfaces, les fournisseurs ADSI peuvent implémenter des fonctionnalités de OLE DB avancées, telles que des requêtes distribuées avec d’autres fournisseurs de OLE DB. Pour plus d’informations, consultez [recherche avec OLE DB](searching-with-ole-db.md).

 

 




