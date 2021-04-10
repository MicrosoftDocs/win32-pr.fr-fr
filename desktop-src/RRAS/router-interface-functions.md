---
title: Fonctions de l’interface du routeur
description: Utilisez les fonctions suivantes pour administrer les interfaces sur le routeur.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309157"
---
# <a name="router-interface-functions"></a><span data-ttu-id="0b5c9-103">Fonctions de l’interface du routeur</span><span class="sxs-lookup"><span data-stu-id="0b5c9-103">Router Interface Functions</span></span>

<span data-ttu-id="0b5c9-104">Utilisez les fonctions suivantes pour administrer les interfaces sur le routeur.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="0b5c9-105">Fonction d’administration</span><span class="sxs-lookup"><span data-stu-id="0b5c9-105">Administration Function</span></span>                                          | <span data-ttu-id="0b5c9-106">Fonction de configuration</span><span class="sxs-lookup"><span data-stu-id="0b5c9-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0b5c9-107">**MprAdminInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="0b5c9-108">**MprConfigInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="0b5c9-109">**MprAdminInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="0b5c9-110">**MprConfigInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="0b5c9-111">**MprAdminInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="0b5c9-112">**MprConfigInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="0b5c9-113">**MprAdminInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="0b5c9-114">**MprConfigInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="0b5c9-115">**MprAdminInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="0b5c9-116">**MprConfigInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="0b5c9-117">**MprAdminInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="0b5c9-118">**MprConfigInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="0b5c9-119">Ces fonctions affectent les interfaces elles-mêmes, pas les clients qui s’exécutent sur les interfaces.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="0b5c9-120">Pour cette raison, aucune des fonctions n’impose à l’appelant de spécifier un transport particulier (IP ou IPX); Bien que les clients (tels que les protocoles de routage) soient associés à des transports particuliers, les interfaces elles-mêmes ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="0b5c9-121">Ces fonctions sont gérées directement par DIM.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="0b5c9-122">Ils n’utilisent pas les gestionnaires de routeur.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="0b5c9-123">Les fonctions [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) et [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) ne peuvent pas créer ou supprimer des interfaces LAN.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="0b5c9-124">Ils peuvent uniquement créer ou supprimer des interfaces de connexion à la demande.</span><span class="sxs-lookup"><span data-stu-id="0b5c9-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="0b5c9-125">Pour obtenir la liste des types d’interfaces, consultez [**\_ \_ type d’interface de routeur**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .</span><span class="sxs-lookup"><span data-stu-id="0b5c9-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




