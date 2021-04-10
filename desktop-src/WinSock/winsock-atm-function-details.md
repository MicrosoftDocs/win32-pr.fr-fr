---
description: En fonction de la taxonomie définie pour les schémas multipoint/multidiffusion indépendante du protocole Windows Sockets 2, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Détails de la fonction ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114290"
---
# <a name="winsock-atm-function-details"></a>Détails de la fonction ATM Winsock

En fonction de la taxonomie définie pour les schémas multipoint/multidiffusion indépendante du protocole Windows Sockets 2, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés. (Pour plus d’informations, consultez la spécification de l’API Windows Sockets 2, annexe D.) Une application agissant comme racine crée des \_ sockets racine c, et les homologues exécutés sur les nœuds terminaux utilisent des \_ sockets de feuille c. L’application racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter de nouveaux nœuds terminaux. Les applications correspondantes sur les nœuds terminaux auront défini leurs \_ sockets de feuille c en mode d’écoute. **WSAJoinLeaf** avec un \_ Socket racine c spécifié sera MAPPÉ au message d’installation Q. 2931 (pour la première feuille) ou au message d’ajout de tiers (pour les autres feuilles).

> [!Note]  
> Les paramètres de qualité de service (QoS) spécifiés dans **WSAJoinLeaf** pour les autres feuilles doivent être ignorés par la spécification Uni du Forum ATM.

 

La jointure initiée par feuille ne fait pas partie du ATM UNI 3,1, mais elle est prise en charge dans le ATM UNI 4,0. Par conséquent, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) avec un \_ Socket feuille c spécifié peut être MAPPÉ au message ATM Uni 4,0 approprié.

Le paramètre AAL et la négociation B-LLI sont pris en charge par la modification des IEs correspondants dans le paramètre *lpSQOS* lors de l’appel de la fonction conditionnelle spécifiée dans [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> Seuls certains champs dans ces deux champs peuvent être modifiés. Pour plus d’informations, consultez la spécification UNI du Forum ATM annexe C et annexe F.

 

 

 



