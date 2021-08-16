---
title: Énumération des groupes locaux
description: sur les serveurs membres et les ordinateurs qui s’exécutent sur Windows 2000 Professional, vous pouvez énumérer tous les groupes locaux.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Énumération des groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1584cf8650b3fa341e7a314e0b6f94120b28c50226f16230c53206d6e14b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191329"
---
# <a name="enumerating-local-groups"></a>Énumération des groupes locaux

sur les serveurs membres et les ordinateurs qui s’exécutent sur Windows 2000 Professional, vous pouvez énumérer tous les groupes locaux.

seuls les groupes locaux peuvent être créés sur les serveurs membres et Windows Professional 2000. Toutefois, ces groupes locaux peuvent contenir :

-   Groupes universels et globaux de la forêt qui contient le domaine dont l’ordinateur est membre.
-   Groupes locaux de domaine à partir du domaine de cet ordinateur.
-   Utilisateurs de n’importe quel domaine de la forêt.

**pour énumérer les groupes locaux sur un serveur membre ou un ordinateur exécutant Windows 2000 Professional**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».

        Le paramètre « the <computer name> » est le nom du groupe d’ordinateurs auquel accéder. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.

    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Définissez un filtre qui contient des « groupes » à l’aide de la propriété [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Cela vous permet d’énumérer le conteneur et de récupérer uniquement les groupes.
3.  Énumérez les objets de groupe à l’aide de la méthode [**IADsContainer :: obten \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .
4.  Pour chaque objet Group, utilisez l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) pour lire le nom et les membres du groupe.

 

 