---
description: L’API Direct3D 9 fonctionne sur Windows XP Display Driver Model (XPDM) ou Windows Vista Display Driver Model (WDDM), selon le système d’exploitation installé.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM et WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512855"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="025ce-103">XPDM et WDDM</span><span class="sxs-lookup"><span data-stu-id="025ce-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="025ce-104">L’API Direct3D 9 fonctionne sur Windows XP Display Driver Model (XPDM) ou Windows Vista Display Driver Model (WDDM), selon le système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="025ce-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="025ce-105">Il existe des différences dans la façon dont l’API Direct3D se comporte sur les deux modèles de pilote.</span><span class="sxs-lookup"><span data-stu-id="025ce-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="025ce-106">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="025ce-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="025ce-107">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="025ce-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="025ce-108">Service Windows</span><span class="sxs-lookup"><span data-stu-id="025ce-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="025ce-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="025ce-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="025ce-110">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="025ce-110">Secure Desktop</span></span>

<span data-ttu-id="025ce-111">Le Bureau sécurisé est actif quand l’un des éléments suivants se produit : l’utilisateur verrouille son bureau (Windows + L), l’économiseur d’écran est activé (quand aucun utilisateur n’est connecté) ou par défaut lorsque le contrôle de compte d’utilisateur affiche une invite.</span><span class="sxs-lookup"><span data-stu-id="025ce-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="025ce-112">Lorsque le Bureau sécurisé est actif, le périphérique HAL n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="025ce-112">When the secure desktop is active, the HAL device is not accessible.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="025ce-113">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="025ce-113">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="025ce-114">La tentative de création d’un appareil HAL Direct3D9 échoue (avec **D3DERR \_ non \_ disponible**) et tout périphérique Direct3D 9 existant indique qu’un code de retour de l’appareil a été perdu sur présent.</span><span class="sxs-lookup"><span data-stu-id="025ce-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span><br/> <span data-ttu-id="025ce-115">Les API Direct3D9Ex et Direct3D 10 peuvent créer correctement un appareil alors que le Bureau sécurisé est actif et tous les appels à présent ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) ou dxgi) renvoient un code d’état indiquant que le bureau n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="025ce-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span><br/> |



 

## <a name="remote-desktop"></a><span data-ttu-id="025ce-116">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="025ce-116">Remote Desktop</span></span>

<span data-ttu-id="025ce-117">Lorsqu’un bureau à distance est actif, l’affichage est géré par l’ordinateur d’affichage et l’ordinateur hôte envoie des informations via le réseau.</span><span class="sxs-lookup"><span data-stu-id="025ce-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="025ce-118">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="025ce-118">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="025ce-119">Sur XPDM, toutes les tentatives de création d’un périphérique Direct3D 9 sur un bureau à distance échouent.</span><span class="sxs-lookup"><span data-stu-id="025ce-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span><br/> <span data-ttu-id="025ce-120">Sur WDDM, le Bureau à distance prend en charge la création d’un appareil HAL via une session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="025ce-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span><br/> |



 

## <a name="windows-service"></a><span data-ttu-id="025ce-121">Service Windows</span><span class="sxs-lookup"><span data-stu-id="025ce-121">Windows Service</span></span>

<span data-ttu-id="025ce-122">Un service Windows est un processus qui s’exécute en arrière-plan, contrôlé par le gestionnaire de contrôle des services (SCM).</span><span class="sxs-lookup"><span data-stu-id="025ce-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="025ce-123">Un service s’exécute indépendamment du bureau actif et dispose donc d’une capacité d’interaction limitée avec les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="025ce-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="025ce-124">Différences entre XPDM et WDDM :</span><span class="sxs-lookup"><span data-stu-id="025ce-124">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="025ce-125">Sur WDDM, l’isolation de la session 0 garantit qu’un service n’a pas accès aux postes de travail des utilisateurs comme mesure de sécurité. par conséquent, un appareil HAL de Direct3D 9 n’est jamais disponible à partir d’un service Windows.</span><span class="sxs-lookup"><span data-stu-id="025ce-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="025ce-126">Vous ne pouvez pas utiliser Direct3D 9 dans un service Windows.</span><span class="sxs-lookup"><span data-stu-id="025ce-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="025ce-127">Pour plus d’informations, consultez [l’article du support technique Microsoft 978635](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="025ce-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="025ce-128">Le tableau suivant récapitule les différences répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="025ce-128">The following table summarizes the differences listed here.</span></span>



|                 | <span data-ttu-id="025ce-129">XPDM</span><span class="sxs-lookup"><span data-stu-id="025ce-129">XPDM</span></span> | <span data-ttu-id="025ce-130">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="025ce-130">WDDM (Direct3D9)</span></span> | <span data-ttu-id="025ce-131">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="025ce-131">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="025ce-132">Bureau sécurisé</span><span class="sxs-lookup"><span data-stu-id="025ce-132">Secure Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="025ce-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="025ce-133">NULLREF</span></span>         | <span data-ttu-id="025ce-134">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-134">Yes</span></span>  | <span data-ttu-id="025ce-135">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-135">Yes</span></span>              | <span data-ttu-id="025ce-136">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-136">Yes</span></span>                          |
| <span data-ttu-id="025ce-137">COUCHE</span><span class="sxs-lookup"><span data-stu-id="025ce-137">HAL</span></span>             | <span data-ttu-id="025ce-138">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-138">No</span></span>   | <span data-ttu-id="025ce-139">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-139">No</span></span>               | <span data-ttu-id="025ce-140">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-140">Yes</span></span>                          |
| <span data-ttu-id="025ce-141">REF</span><span class="sxs-lookup"><span data-stu-id="025ce-141">REF</span></span>             | <span data-ttu-id="025ce-142">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-142">Yes</span></span>  | <span data-ttu-id="025ce-143">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-143">Yes</span></span>              | <span data-ttu-id="025ce-144">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-144">Yes</span></span>                          |
| <span data-ttu-id="025ce-145">Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="025ce-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="025ce-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="025ce-146">NULLREF</span></span>         | <span data-ttu-id="025ce-147">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-147">No</span></span>   | <span data-ttu-id="025ce-148">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-148">Yes</span></span>              | <span data-ttu-id="025ce-149">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-149">Yes</span></span>                          |
| <span data-ttu-id="025ce-150">COUCHE</span><span class="sxs-lookup"><span data-stu-id="025ce-150">HAL</span></span>             | <span data-ttu-id="025ce-151">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-151">No</span></span>   | <span data-ttu-id="025ce-152">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-152">Yes</span></span>              | <span data-ttu-id="025ce-153">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-153">Yes</span></span>                          |
| <span data-ttu-id="025ce-154">REF</span><span class="sxs-lookup"><span data-stu-id="025ce-154">REF</span></span>             | <span data-ttu-id="025ce-155">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-155">Yes</span></span>  | <span data-ttu-id="025ce-156">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-156">Yes</span></span>              | <span data-ttu-id="025ce-157">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-157">Yes</span></span>                          |
| <span data-ttu-id="025ce-158">Service Windows</span><span class="sxs-lookup"><span data-stu-id="025ce-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="025ce-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="025ce-159">NULLREF</span></span>         | <span data-ttu-id="025ce-160">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-160">No</span></span>   | <span data-ttu-id="025ce-161">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-161">No</span></span>               | <span data-ttu-id="025ce-162">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-162">No</span></span>                           |
| <span data-ttu-id="025ce-163">COUCHE</span><span class="sxs-lookup"><span data-stu-id="025ce-163">HAL</span></span>             | <span data-ttu-id="025ce-164">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-164">No</span></span>   | <span data-ttu-id="025ce-165">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-165">No</span></span>               | <span data-ttu-id="025ce-166">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-166">No</span></span>                           |
| <span data-ttu-id="025ce-167">REF</span><span class="sxs-lookup"><span data-stu-id="025ce-167">REF</span></span>             | <span data-ttu-id="025ce-168">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-168">No</span></span>   | <span data-ttu-id="025ce-169">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-169">No</span></span>               | <span data-ttu-id="025ce-170">Non</span><span class="sxs-lookup"><span data-stu-id="025ce-170">No</span></span>                           |
| <span data-ttu-id="025ce-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="025ce-171">WARP10</span></span>          | <span data-ttu-id="025ce-172">N/A</span><span class="sxs-lookup"><span data-stu-id="025ce-172">N/A</span></span>  | <span data-ttu-id="025ce-173">N/A</span><span class="sxs-lookup"><span data-stu-id="025ce-173">N/A</span></span>              | <span data-ttu-id="025ce-174">Oui</span><span class="sxs-lookup"><span data-stu-id="025ce-174">Yes</span></span>                          |



 

<span data-ttu-id="025ce-175">Pour plus d’informations sur XPDM, WDDM, Direct3D9Ex et Direct3D 10, consultez [API graphiques dans Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="025ce-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="025ce-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="025ce-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="025ce-177">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="025ce-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
