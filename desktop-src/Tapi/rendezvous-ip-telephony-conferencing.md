---
description: Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conférence de téléphonie IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773569"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conférence de téléphonie IP Rendezvous

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.

Les composants clés de rendezvous :

Les [contrôles d’annuaire](directory-controls.md) sont une abstraction des listes de conférences sur un serveur ils ou NTDS.

Les [contrôles blob de conférence](conference-blob-controls.md) représentent des informations spécifiques à la Conférence, telles que l’heure de démarrage et d’arrêt. Des interfaces spéciales sont fournies pour les blobs de protocole SDP. Pour plus d’informations, consultez la RFC 2327 intitulée « SDP : session Description Protocol ». Une copie actuelle de cette RFC peut être localisée à l’aide d’un moteur de recherche Internet.

Les [interfaces COM de multidiffusion](multicast-com-interfaces.md) sont des wrappers com pour les fonctions MADCAP, anciennement connues sous le titre de MDHCP. Ces interfaces permettent à une application d’obtenir des adresses de multidiffusion à partir d’un serveur d’allocation d’adresses de multidiffusion.

Les documents suivants fournissent une vue d’ensemble générale et des exemples d’utilisation des contrôles Rendezvous pour la téléphonie et la conférence IP.

 

 



