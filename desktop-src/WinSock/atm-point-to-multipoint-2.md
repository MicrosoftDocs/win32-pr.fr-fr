---
description: La technologie ATM est incluse dans la catégorie des plans de contrôle et des données enracinées.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Point d’ATM vers multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529118"
---
# <a name="atm-point-to-multipoint"></a>Point d’ATM vers multipoint

La technologie ATM est incluse dans la catégorie des plans de contrôle et des données enracinées. Une application agissant comme racine créerait des \_ sockets racine c et des équivalents s’exécutant sur des nœuds terminaux utiliserait des \_ sockets de feuille c. L’application racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter de nouveaux nœuds terminaux. Les applications correspondantes sur les nœuds terminaux auront défini leurs \_ sockets de feuille c en mode écoute. **WSAJoinLeaf** avec un \_ Socket racine c spécifié est mappé au message Q. 2931 ADDPARTY. La jointure initiée par feuille n’est pas prise en charge dans ATM UNI 3,1, mais elle est prise en charge dans ATM UNI 4,0. Par conséquent, **WSAJoinLeaf** avec un \_ Socket feuille c spécifié est MAPPÉ au message ATM Uni 4,0 approprié.

Il y a d’autres points à prendre en compte pour le point à multipoint :

-   L’ajout de nouvelles feuilles à la session point à multipoint ATM est basé uniquement sur les invitations. Les invitations de la racine quittent, qui ont déjà leur appel de fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , en appelant la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Le workflow de données dans une session ATM point à multipoint ne concerne que la racine jusqu’au départ. les feuilles ne peuvent pas utiliser la même session pour envoyer des informations à la racine.
-   Une seule feuille par adaptateur ATM est autorisée.

 

 



