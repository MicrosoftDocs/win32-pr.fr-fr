---
description: Les interfaces COM de multidiffusion autorisent l’accès à la fonction réseaux pour l’allocation, le renouvellement et la libération des baux sur les adresses de multidiffusion.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Interfaces COM de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749532"
---
# <a name="multicast-com-interfaces"></a>Interfaces COM de multidiffusion

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les interfaces COM de multidiffusion autorisent l’accès à la fonctionnalité du réseau pour l’allocation, le renouvellement et la libération des baux sur les adresses de multidiffusion. Elles encapsulent un ensemble de définitions de structure de données et de fonction. Les interfaces COM libèrent le programmeur des tâches fastidieuses de compréhension et de manipulation de ces structures de données. En outre, étant donné que TAPI 3 lui-même est basé sur COM, ces interfaces rendent l’allocation d’adresses de multidiffusion accessible de manière cohérente avec les autres fonctionnalités fournies par TAPI 3. Les applications écrites à l’aide de Visual Basic, Java ou des langages de script qui ne peuvent normalement pas accéder directement à l’API Windows sont en mesure d’utiliser ces interfaces.

L’allocation d’adresses de multidiffusion fait actuellement l’objet d’un groupe de travail IETF. Pour accéder aux informations actuelles, interrogez « MDHCP » ou « MADCAP » et « brouillon Internet » à l’aide de n’importe quel moteur de recherche Internet. En plus de MADCAP, l’architecture proposée comprend un protocole pour la coordination de serveur à serveur au sein d’un domaine ou en tant que, ainsi qu’un protocole pour la coordination entre domaines. Bien que cette architecture soit en cours de développement, le client n’a pas à se préoccuper des détails de ce schéma.

Ce composant ne prend actuellement en charge que les adresses IP version 4.

> [!Note]  
> Le protocole utilisé pour ces interfaces est actuellement MADCAP. Dans les versions précédentes, il était connu sous le nom de MDHCP.

 

L’objet multicast est créé en appelant **CoCreateInstance** sur l’interface [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) . L’interface **IMcastAddressAllocation** expose la méthode [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) , qui permet à une application d’obtenir une liste de toutes les étendues de multidiffusion disponibles.

Une fois qu’une étendue de travail a été obtenue, la méthode [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) est utilisée pour demander une adresse de multidiffusion à partir du serveur. Si la requête réussit, un pointeur [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) est retourné. La méthode [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) exposée par cette interface peut ensuite être utilisée pour obtenir les adresses.

Chaque objet multimédia associé à la Conférence expose une interface [**ITConnection**](itconnection.md) . La méthode [**ITConnection :: SetAddressInfo**](itconnection-setaddressinfo.md) permet d’attribuer les adresses de multidiffusion obtenues au média de la Conférence. L’adresse doit être définie pour chaque interface **ITConnection** de chaque objet multimédia associé à la Conférence.

 

 



