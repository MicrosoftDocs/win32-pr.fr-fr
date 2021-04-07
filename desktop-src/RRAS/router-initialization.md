---
title: Initialisation du routeur
description: Les informations de configuration pour le routeur, les gestionnaires de routeur et les protocoles/clients de routage sont divisées en informations globales et par interface et sont stockées dans le registre et le fichier d’annuaire téléphonique du routeur, Router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- routeurs RRAS, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670898"
---
# <a name="router-initialization"></a><span data-ttu-id="5c3ca-104">Initialisation du routeur</span><span class="sxs-lookup"><span data-stu-id="5c3ca-104">Router Initialization</span></span>

<span data-ttu-id="5c3ca-105">Les informations de configuration pour le routeur, les gestionnaires de routeur et les protocoles/clients de routage sont divisées en informations globales et par interface et sont stockées dans le registre et le fichier d’annuaire téléphonique du routeur, Router. pbk.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="5c3ca-106">Au démarrage du processus de routeur, DIM (gestionnaire d’interface dynamique) lit la configuration du routeur à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="5c3ca-107">DIM crée les interfaces qui sont spécifiées par les informations d’interface.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="5c3ca-108">DIM récupère également les informations globales du gestionnaire de routage.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="5c3ca-109">DIM démarre les gestionnaires de routeur qui correspondent à ces informations et leur transmet les informations.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="5c3ca-110">Par exemple, si DIM trouve des informations globales pour le gestionnaire de routeur IP dans le registre, DIM démarre le gestionnaire de routeur IP et lui transmet les informations globales.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="5c3ca-111">Si aucune information globale n’est présente dans le registre pour un gestionnaire de routage particulier, DIM ne démarre pas ce gestionnaire de routeur.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="5c3ca-112">Les gestionnaires de routeur examinent les informations globales reçues de DIM.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="5c3ca-113">Si le gestionnaire de routeur trouve des informations spécifiques à un client particulier dans les informations globales, il charge la DLL du client (par exemple IpNAT.dll) et initialise le client en appelant les fonctions [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) et [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) du client.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="5c3ca-114">Le gestionnaire de routeur transmet les informations globales spécifiques au client au client lors de l’appel à [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span><span class="sxs-lookup"><span data-stu-id="5c3ca-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="5c3ca-115">À chaque étape, les informations transmises à l’entité suivante sont opaques pour l’entité qui le précède.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="5c3ca-116">Autrement dit, DIM n’interprète pas les informations globales pour le gestionnaire de routeur IP, au-delà du fait que les informations sont destinées au gestionnaire de routeur IP.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="5c3ca-117">De même, le gestionnaire de routeur IP n’interprète pas les informations spécifiques au protocole OSPF au-delà du fait qu’il s’agit d’informations OSPF.</span><span class="sxs-lookup"><span data-stu-id="5c3ca-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




