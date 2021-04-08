---
title: Référence de l’interface de protocole de routage
description: Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routage et accès à distance service RRAS, interface de protocole de routage, référence
- Routage de l’interface de protocole RRAS, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839981"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="1e118-105">Référence de l’interface de protocole de routage</span><span class="sxs-lookup"><span data-stu-id="1e118-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="1e118-106">Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e118-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="1e118-107">MPR50 doit être défini dans le fichier Make pour le protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="1e118-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="1e118-108">La macro de **\_ \_ liaison IP (x) sizeof** calcule la taille, en octets, d’une structure d’informations de [**\_ \_ liaison \_ d’adaptateur IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) qui contient le nombre d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="1e118-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="1e118-109">Ces éléments de référence sont décrits dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e118-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="1e118-110">Fonctions de l’interface de protocole de routage</span><span class="sxs-lookup"><span data-stu-id="1e118-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="1e118-111">Structures de l’interface de protocole de routage</span><span class="sxs-lookup"><span data-stu-id="1e118-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="1e118-112">Gestion des tables de services IPX</span><span class="sxs-lookup"><span data-stu-id="1e118-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




