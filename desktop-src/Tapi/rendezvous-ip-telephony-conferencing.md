---
description: Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conférence de téléphonie IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202827"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conférence de téléphonie IP Rendezvous

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.

Les composants clés de rendezvous :

Les [contrôles d’annuaire](directory-controls.md) sont une abstraction des listes de conférences sur un serveur ils ou NTDS.

Les [contrôles blob de conférence](conference-blob-controls.md) représentent des informations spécifiques à la Conférence, telles que l’heure de démarrage et d’arrêt. Des interfaces spéciales sont fournies pour les blobs de protocole SDP. Pour plus d’informations, consultez la RFC 2327 intitulée « SDP : session Description Protocol ». Une copie actuelle de cette RFC peut être localisée à l’aide d’un moteur de recherche Internet.

Les [interfaces COM de multidiffusion](multicast-com-interfaces.md) sont des wrappers com pour les fonctions MADCAP, anciennement connues sous le titre de MDHCP. Ces interfaces permettent à une application d’obtenir des adresses de multidiffusion à partir d’un serveur d’allocation d’adresses de multidiffusion.

Les documents suivants fournissent une vue d’ensemble générale et des exemples d’utilisation des contrôles Rendezvous pour la téléphonie et la conférence IP.

 

 



