---
title: Énumération des groupes locaux
description: Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, vous pouvez énumérer tous les groupes locaux.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Énumération des groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724556"
---
# <a name="enumerating-local-groups"></a>Énumération des groupes locaux

Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, vous pouvez énumérer tous les groupes locaux.

Seuls les groupes locaux peuvent être créés sur les serveurs membres et Windows 2000 professionnel. Toutefois, ces groupes locaux peuvent contenir :

-   Groupes universels et globaux de la forêt qui contient le domaine dont l’ordinateur est membre.
-   Groupes locaux de domaine à partir du domaine de cet ordinateur.
-   Utilisateurs de n’importe quel domaine de la forêt.

**Pour énumérer les groupes locaux sur un serveur membre ou un ordinateur exécutant Windows 2000 professionnel**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».

        Le paramètre « the <computer name> » est le nom du groupe d’ordinateurs auquel accéder. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.

    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Définissez un filtre qui contient des « groupes » à l’aide de la propriété [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Cela vous permet d’énumérer le conteneur et de récupérer uniquement les groupes.
3.  Énumérez les objets de groupe à l’aide de la méthode [**IADsContainer :: obten \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .
4.  Pour chaque objet Group, utilisez l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) pour lire le nom et les membres du groupe.

 

 