---
description: Éléments de l’interface Windows Sockets 2 (Winsock) pour multipoint et multidiffusion.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Éléments de l’interface Windows Sockets 2 pour multipoint et multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520416"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Éléments de l’interface Windows Sockets 2 pour multipoint et multidiffusion

Les mécanismes qui ont été incorporés dans Windows Sockets 2 pour l’utilisation des fonctionnalités multipoint peuvent être résumés comme suit :

-   Trois bits d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quatre indicateurs définis pour le paramètre *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Une fonction, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint.
-   Deux codes de commande [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour contrôler le bouclage multipoint et l’étendue des transmissions par multidiffusion.

Les sections suivantes décrivent ces éléments d’interface plus en détail :

-   [Sémantique pour joindre des feuilles multipoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Comment les protocoles multipoint existants prennent en charge ces extensions](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
