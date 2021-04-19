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
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="57ebb-103">Éléments de l’interface Windows Sockets 2 pour multipoint et multidiffusion</span><span class="sxs-lookup"><span data-stu-id="57ebb-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="57ebb-104">Les mécanismes qui ont été incorporés dans Windows Sockets 2 pour l’utilisation des fonctionnalités multipoint peuvent être résumés comme suit :</span><span class="sxs-lookup"><span data-stu-id="57ebb-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="57ebb-105">Trois bits d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="57ebb-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="57ebb-106">Quatre indicateurs définis pour le paramètre *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="57ebb-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="57ebb-107">Une fonction, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), pour l’ajout de nœuds terminaux dans une session multipoint.</span><span class="sxs-lookup"><span data-stu-id="57ebb-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="57ebb-108">Deux codes de commande [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour contrôler le bouclage multipoint et l’étendue des transmissions par multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="57ebb-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="57ebb-109">Les sections suivantes décrivent ces éléments d’interface plus en détail :</span><span class="sxs-lookup"><span data-stu-id="57ebb-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="57ebb-110">Sémantique pour joindre des feuilles multipoint</span><span class="sxs-lookup"><span data-stu-id="57ebb-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="57ebb-111">Comment les protocoles multipoint existants prennent en charge ces extensions</span><span class="sxs-lookup"><span data-stu-id="57ebb-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
