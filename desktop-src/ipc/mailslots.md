---
description: Un mailslot est un mécanisme de communication interprocessus (IPC) unidirectionnel. Les applications peuvent stocker des messages dans un mailslot. Le propriétaire de la mailslot peut récupérer les messages qui y sont stockés.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Boîtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537065"
---
# <a name="mailslots"></a>Boîtes

Un *mailslot* est un mécanisme de communication interprocessus (IPC) unidirectionnel. Les applications peuvent stocker des messages dans un mailslot. Le propriétaire de la mailslot peut récupérer les messages qui y sont stockés. Ces messages sont généralement envoyés sur un réseau à un ordinateur spécifié ou à tous les ordinateurs d’un domaine spécifié. Un *domaine* est un groupe de stations de travail et de serveurs qui partagent un nom de groupe.

-   [À propos des mailslots](about-mailslots.md)
-   [Utilisation de mailslots](using-mailslots.md)
-   [Référence mailslot](mailslot-reference.md)

Vous pouvez choisir d’utiliser des [canaux nommés](named-pipes.md) ou des [sockets Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) au lieu de mailslots pour les communications entre processus. Les canaux nommés sont un moyen simple pour deux processus d’échanger des messages. Les mailslots, quant à eux, sont un moyen simple pour un processus de diffuser des messages à plusieurs processus. Un point important à prendre en compte est que les messages MailSlots diffusent des messages à l’aide de datagrammes. Un *datagramme* est un petit paquet d’informations que le réseau envoie le long du câble. À l’instar d’une diffusion de radio ou de télévision, un datagramme n’offre aucune confirmation de réception. Il n’existe aucun moyen de garantir qu’un datagramme a été reçu. Tout comme les montagnes, les grands bâtiments ou les signaux interférants peuvent entraîner la perte d’un signal de radio ou de télévision, il existe des éléments qui peuvent empêcher un datagramme d’atteindre une destination particulière. Les canaux nommés sont similaires aux appels téléphoniques : vous communiquez uniquement à un tiers, mais vous savez que le message est reçu.

 

 
