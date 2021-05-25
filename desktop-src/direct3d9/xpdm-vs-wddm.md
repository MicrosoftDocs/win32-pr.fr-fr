---
description: L’API Direct3D 9 fonctionne sur Windows XP Display Driver Model (XPDM) ou Windows Vista Display Driver Model (WDDM), selon le système d’exploitation installé.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM et WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343534"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="227e1-103">XPDM et WDDM</span><span class="sxs-lookup"><span data-stu-id="227e1-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="227e1-104">L’API Direct3D 9 fonctionne sur Windows XP Display Driver Model (XPDM) ou Windows Vista Display Driver Model (WDDM), selon le système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="227e1-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="227e1-105">Il existe des différences dans la façon dont l’API Direct3D se comporte sur les deux modèles de pilote.</span><span class="sxs-lookup"><span data-stu-id="227e1-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="227e1-106">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="227e1-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="227e1-107">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="227e1-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="227e1-108">Service Windows</span><span class="sxs-lookup"><span data-stu-id="227e1-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="227e1-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="227e1-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="227e1-110">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="227e1-110">Secure Desktop</span></span>

<span data-ttu-id="227e1-111">Le Bureau sécurisé est actif quand l’un des éléments suivants se produit : l’utilisateur verrouille son bureau (Windows + L), l’économiseur d’écran est activé (quand aucun utilisateur n’est connecté) ou par défaut lorsque le contrôle de compte d’utilisateur affiche une invite.</span><span class="sxs-lookup"><span data-stu-id="227e1-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="227e1-112">Lorsque le Bureau sécurisé est actif, le périphérique HAL n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="227e1-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="227e1-113">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="227e1-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="227e1-114">La tentative de création d’un appareil HAL Direct3D9 échoue (avec **D3DERR \_ non \_ disponible**) et tout périphérique Direct3D 9 existant indique qu’un code de retour de l’appareil a été perdu sur présent.</span><span class="sxs-lookup"><span data-stu-id="227e1-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="227e1-115">Les API Direct3D9Ex et Direct3D 10 peuvent créer correctement un appareil alors que le Bureau sécurisé est actif et tous les appels à présent ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) ou dxgi) renvoient un code d’état indiquant que le bureau n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="227e1-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="227e1-116">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="227e1-116">Remote Desktop</span></span>

<span data-ttu-id="227e1-117">Lorsqu’un bureau à distance est actif, l’affichage est géré par l’ordinateur d’affichage et l’ordinateur hôte envoie des informations via le réseau.</span><span class="sxs-lookup"><span data-stu-id="227e1-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="227e1-118">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="227e1-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="227e1-119">Sur XPDM, toutes les tentatives de création d’un périphérique Direct3D 9 sur un bureau à distance échouent.</span><span class="sxs-lookup"><span data-stu-id="227e1-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="227e1-120">Sur WDDM, le Bureau à distance prend en charge la création d’un appareil HAL via une session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="227e1-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="227e1-121">Service Windows</span><span class="sxs-lookup"><span data-stu-id="227e1-121">Windows Service</span></span>

<span data-ttu-id="227e1-122">Un service Windows est un processus qui s’exécute en arrière-plan, contrôlé par le gestionnaire de contrôle des services (SCM).</span><span class="sxs-lookup"><span data-stu-id="227e1-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="227e1-123">Un service s’exécute indépendamment du bureau actif et dispose donc d’une capacité d’interaction limitée avec les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="227e1-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="227e1-124">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="227e1-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="227e1-125">Sur WDDM, l’isolation de la session 0 garantit qu’un service n’a pas accès aux postes de travail des utilisateurs comme mesure de sécurité. par conséquent, un appareil HAL de Direct3D 9 n’est jamais disponible à partir d’un service Windows.</span><span class="sxs-lookup"><span data-stu-id="227e1-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="227e1-126">Vous ne pouvez pas utiliser Direct3D 9 dans un service Windows.</span><span class="sxs-lookup"><span data-stu-id="227e1-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="227e1-127">Pour plus d’informations, consultez [l’article du support technique Microsoft 978635](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="227e1-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="227e1-128">Le tableau suivant récapitule les différences répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="227e1-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="227e1-129">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="227e1-129">Secure Desktop</span></span> | <span data-ttu-id="227e1-130">XPDM</span><span class="sxs-lookup"><span data-stu-id="227e1-130">XPDM</span></span> | <span data-ttu-id="227e1-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="227e1-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="227e1-132">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="227e1-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="227e1-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="227e1-133">NULLREF</span></span>         | <span data-ttu-id="227e1-134">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-134">Yes</span></span>  | <span data-ttu-id="227e1-135">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-135">Yes</span></span>              | <span data-ttu-id="227e1-136">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-136">Yes</span></span>                          |
| <span data-ttu-id="227e1-137">COUCHE</span><span class="sxs-lookup"><span data-stu-id="227e1-137">HAL</span></span>             | <span data-ttu-id="227e1-138">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-138">No</span></span>   | <span data-ttu-id="227e1-139">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-139">No</span></span>               | <span data-ttu-id="227e1-140">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-140">Yes</span></span>                          |
| <span data-ttu-id="227e1-141">REF</span><span class="sxs-lookup"><span data-stu-id="227e1-141">REF</span></span>             | <span data-ttu-id="227e1-142">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-142">Yes</span></span>  | <span data-ttu-id="227e1-143">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-143">Yes</span></span>              | <span data-ttu-id="227e1-144">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-144">Yes</span></span>                          |
| <span data-ttu-id="227e1-145">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="227e1-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="227e1-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="227e1-146">NULLREF</span></span>         | <span data-ttu-id="227e1-147">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-147">No</span></span>   | <span data-ttu-id="227e1-148">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-148">Yes</span></span>              | <span data-ttu-id="227e1-149">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-149">Yes</span></span>                          |
| <span data-ttu-id="227e1-150">COUCHE</span><span class="sxs-lookup"><span data-stu-id="227e1-150">HAL</span></span>             | <span data-ttu-id="227e1-151">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-151">No</span></span>   | <span data-ttu-id="227e1-152">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-152">Yes</span></span>              | <span data-ttu-id="227e1-153">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-153">Yes</span></span>                          |
| <span data-ttu-id="227e1-154">REF</span><span class="sxs-lookup"><span data-stu-id="227e1-154">REF</span></span>             | <span data-ttu-id="227e1-155">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-155">Yes</span></span>  | <span data-ttu-id="227e1-156">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-156">Yes</span></span>              | <span data-ttu-id="227e1-157">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-157">Yes</span></span>                          |
| <span data-ttu-id="227e1-158">Service Windows</span><span class="sxs-lookup"><span data-stu-id="227e1-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="227e1-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="227e1-159">NULLREF</span></span>         | <span data-ttu-id="227e1-160">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-160">No</span></span>   | <span data-ttu-id="227e1-161">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-161">No</span></span>               | <span data-ttu-id="227e1-162">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-162">No</span></span>                           |
| <span data-ttu-id="227e1-163">COUCHE</span><span class="sxs-lookup"><span data-stu-id="227e1-163">HAL</span></span>             | <span data-ttu-id="227e1-164">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-164">No</span></span>   | <span data-ttu-id="227e1-165">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-165">No</span></span>               | <span data-ttu-id="227e1-166">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-166">No</span></span>                           |
| <span data-ttu-id="227e1-167">REF</span><span class="sxs-lookup"><span data-stu-id="227e1-167">REF</span></span>             | <span data-ttu-id="227e1-168">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-168">No</span></span>   | <span data-ttu-id="227e1-169">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-169">No</span></span>               | <span data-ttu-id="227e1-170">Non</span><span class="sxs-lookup"><span data-stu-id="227e1-170">No</span></span>                           |
| <span data-ttu-id="227e1-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="227e1-171">WARP10</span></span>          | <span data-ttu-id="227e1-172">N/A</span><span class="sxs-lookup"><span data-stu-id="227e1-172">N/A</span></span>  | <span data-ttu-id="227e1-173">N/A</span><span class="sxs-lookup"><span data-stu-id="227e1-173">N/A</span></span>              | <span data-ttu-id="227e1-174">Oui</span><span class="sxs-lookup"><span data-stu-id="227e1-174">Yes</span></span>                          |



 

<span data-ttu-id="227e1-175">Pour plus d’informations sur XPDM, WDDM, Direct3D9Ex et Direct3D 10, consultez [API graphiques dans Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="227e1-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="227e1-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="227e1-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="227e1-177">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="227e1-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
