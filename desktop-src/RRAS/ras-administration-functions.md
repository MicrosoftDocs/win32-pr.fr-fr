---
title: Fonctions d’administration RAS
description: Cette documentation décrit les fonctions RRAS utilisées pour développer des logiciels afin d’administrer les connexions d’accès à distance RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311062"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="969a9-103">Fonctions d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="969a9-103">RAS Administration Functions</span></span>

<span data-ttu-id="969a9-104">Cette documentation décrit les fonctions RRAS utilisées pour développer des logiciels afin d’administrer les connexions d’accès à distance RAS.</span><span class="sxs-lookup"><span data-stu-id="969a9-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="969a9-105">Ces fonctions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="969a9-105">These functions include:</span></span>

-   [<span data-ttu-id="969a9-106">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="969a9-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="969a9-107">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="969a9-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="969a9-108">**MprAdminConnectionEnumEx**</span><span class="sxs-lookup"><span data-stu-id="969a9-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="969a9-109">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="969a9-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="969a9-110">**MprAdminConnectionGetInfoEx**</span><span class="sxs-lookup"><span data-stu-id="969a9-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="969a9-111">**MprAdminConnectionRemoveQuarantine**</span><span class="sxs-lookup"><span data-stu-id="969a9-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="969a9-112">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="969a9-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="969a9-113">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="969a9-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="969a9-114">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="969a9-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="969a9-115">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="969a9-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="969a9-116">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="969a9-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="969a9-117">Des fonctions supplémentaires sont utilisées pour l’administration RAS et l’administration du routeur.</span><span class="sxs-lookup"><span data-stu-id="969a9-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="969a9-118">Les fonctions suivantes décrites dans la référence [fonctions d’administration du routeur](router-administration-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="969a9-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="969a9-119">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="969a9-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="969a9-120">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="969a9-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="969a9-121">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="969a9-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="969a9-122">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="969a9-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="969a9-123">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="969a9-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="969a9-124">Pour implémenter une DLL d’administration RAS, utilisez les fonctions décrites dans la rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="969a9-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="969a9-125">Fonctions de la DLL d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="969a9-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="969a9-126">Pour gérer les utilisateurs d’un serveur RAS, utilisez les fonctions décrites dans la rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="969a9-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="969a9-127">Fonctions d’administration d’utilisateur RAS</span><span class="sxs-lookup"><span data-stu-id="969a9-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




