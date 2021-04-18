---
title: Comparaison de fonctions Windows 2000 et redistribuable RRAS
description: L’API RAS est distribuée en tant que fonctionnalité des systèmes d’exploitation Windows 2000 et versions ultérieures et est disponible en tant que redistribuable pour Windows NT 4,0 avec Service Pack 3 (SP3) et versions antérieures.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511852"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="88f3f-103">Comparaison de fonctions : Windows 2000 et le package redistribuable RRAS</span><span class="sxs-lookup"><span data-stu-id="88f3f-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="88f3f-104">L’API RAS est distribuée en tant que fonctionnalité des systèmes d’exploitation Windows 2000 et versions ultérieures et est disponible en tant que redistribuable pour Windows NT 4,0 avec Service Pack 3 (SP3) et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="88f3f-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="88f3f-105">RAS offre les mêmes fonctionnalités dans ces deux formes, mais la Convention d’affectation de noms utilisée est différente pour les éléments de référence dans chaque version de l’API RAS.</span><span class="sxs-lookup"><span data-stu-id="88f3f-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="88f3f-106">Les fonctions RAS pour Windows NT 4,0 avec SP3 et les versions antérieures commencent généralement par le préfixe « RasAdmin ».</span><span class="sxs-lookup"><span data-stu-id="88f3f-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="88f3f-107">Les fonctions analogues pour le service Routage et accès à distance (RRAS) commencent par le préfixe « MprAdmin ».</span><span class="sxs-lookup"><span data-stu-id="88f3f-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="88f3f-108">Par exemple, RAS fournit une fonction appelée [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span><span class="sxs-lookup"><span data-stu-id="88f3f-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="88f3f-109">La fonction analogue dans RRAS est appelée [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="88f3f-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="88f3f-110">À titre d’exemple similaire, RAS fournit la fonction de rappel [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="88f3f-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="88f3f-111">RRAS fournit une fonction de rappel similaire appelée [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="88f3f-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="88f3f-112">Les exceptions à cette règle sont [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), qui sous RRAS est [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)et [**RasAdminFreeBuffer**](rasadminfreebuffer.md), qui sous RRAS est [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span><span class="sxs-lookup"><span data-stu-id="88f3f-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="88f3f-113">Le tableau suivant répertorie les fonctions RAS Windows NT 4,0 SP3 et les fonctions RRAS correspondantes.</span><span class="sxs-lookup"><span data-stu-id="88f3f-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="88f3f-114">RAS Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="88f3f-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="88f3f-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="88f3f-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f3f-116">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="88f3f-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="88f3f-117">**MprAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="88f3f-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="88f3f-118">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="88f3f-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="88f3f-119">**MprAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="88f3f-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="88f3f-120">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="88f3f-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="88f3f-121">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="88f3f-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="88f3f-122">**RasAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="88f3f-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="88f3f-123">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="88f3f-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="88f3f-124">**RasAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="88f3f-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="88f3f-125">**MprAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="88f3f-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="88f3f-126">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="88f3f-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="88f3f-127">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="88f3f-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="88f3f-128">**RasAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="88f3f-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="88f3f-129">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="88f3f-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="88f3f-130">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="88f3f-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="88f3f-131">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="88f3f-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="88f3f-132">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="88f3f-133">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="88f3f-134">**RasAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="88f3f-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="88f3f-135">**MprAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="88f3f-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="88f3f-136">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="88f3f-137">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="88f3f-138">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="88f3f-139">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="88f3f-140">Bien que les fonctions RRAS soient similaires à celles de Windows NT 4,0 avec SP3 et des équivalents RAS antérieurs dans les fonctionnalités, les fonctions RRAS utilisent souvent un ensemble de paramètres différent.</span><span class="sxs-lookup"><span data-stu-id="88f3f-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="88f3f-141">Pour obtenir des informations complètes sur la liste de paramètres de cette fonction, consultez la page de référence pour une fonction particulière.</span><span class="sxs-lookup"><span data-stu-id="88f3f-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="88f3f-142">Le redistribuable RRAS pour Windows NT 4,0 avec SP3 et les versions antérieures ajoute les fonctions suivantes, qui n’ont pas d’équivalents RAS :</span><span class="sxs-lookup"><span data-stu-id="88f3f-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="88f3f-143">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="88f3f-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="88f3f-144">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="88f3f-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="88f3f-145">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="88f3f-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="88f3f-146">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="88f3f-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="88f3f-147">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="88f3f-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="88f3f-148">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="88f3f-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="88f3f-149">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="88f3f-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="88f3f-150">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="88f3f-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="88f3f-151">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="88f3f-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="88f3f-152">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="88f3f-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="88f3f-153">Outre les fonctions précédentes, les systèmes d’exploitation Windows 2000 et versions ultérieures ajoutent les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="88f3f-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="88f3f-154">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="88f3f-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="88f3f-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="88f3f-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="88f3f-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="88f3f-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




