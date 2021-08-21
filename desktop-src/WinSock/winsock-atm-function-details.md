---
description: sur la base de la taxonomie définie Windows pour les modèles multipoint/multidiffusion de sockets 2 indépendantes du protocole, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Détails de la fonction ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051377"
---
# <a name="winsock-atm-function-details"></a>Détails de la fonction ATM Winsock

sur la base de la taxonomie définie Windows pour les modèles multipoint/multidiffusion de sockets 2 indépendantes du protocole, la technologie ATM se trouve dans la catégorie des données enracinées et des plans de contrôle enracinés. (pour plus d’informations, consultez la spécification de l’API Windows sockets 2, annexe D.) Une application agissant comme racine crée des \_ sockets racine c, et les homologues exécutés sur les nœuds terminaux utilisent des \_ sockets de feuille c. L’application racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour ajouter de nouveaux nœuds terminaux. Les applications correspondantes sur les nœuds terminaux auront défini leurs \_ sockets de feuille c en mode d’écoute. **WSAJoinLeaf** avec un \_ Socket racine c spécifié sera MAPPÉ au message d’installation Q. 2931 (pour la première feuille) ou au message d’ajout de tiers (pour les autres feuilles).

> [!Note]  
> Les paramètres de qualité de service (QoS) spécifiés dans **WSAJoinLeaf** pour les autres feuilles doivent être ignorés par la spécification Uni du Forum ATM.

 

La jointure initiée par feuille ne fait pas partie du ATM UNI 3,1, mais elle est prise en charge dans le ATM UNI 4,0. Par conséquent, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) avec un \_ Socket feuille c spécifié peut être MAPPÉ au message ATM Uni 4,0 approprié.

Le paramètre AAL et la négociation B-LLI sont pris en charge par la modification des IEs correspondants dans le paramètre *lpSQOS* lors de l’appel de la fonction conditionnelle spécifiée dans [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> Seuls certains champs dans ces deux champs peuvent être modifiés. Pour plus d’informations, consultez la spécification UNI du Forum ATM annexe C et annexe F.

 

 

 



