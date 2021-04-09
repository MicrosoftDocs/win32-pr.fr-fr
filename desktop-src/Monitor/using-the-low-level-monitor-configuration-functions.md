---
title: Utilisation des fonctions de configuration de l’analyseur de Low-Level
description: Utilisation des fonctions de configuration de l’analyseur de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- surveiller, fonctions
- surveiller, fonctions de configuration de bas niveau
- surveiller, DDC/CI
- surveiller, afficher l’interface de commande de canal de données
- configuration de l’analyse, fonctions de configuration de bas niveau
- configuration de l’analyse, fonctions
- configuration de l’analyse, DDC/CI
- configuration de l’analyse, affichage de l’interface de commande du canal de données
- fonctions de configuration de bas niveau
- Afficher l’interface de commande du canal de données
- DDC/CI
- Jeu de commandes de contrôle du moniteur VESA (MCCS)
- Jeu de commandes du contrôle d’analyse (MCCS)
- MCCS (jeu de commandes du contrôle du moniteur)
- Panneau de configuration virtuel (VCP)
- VCP (panneau de configuration virtuel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940935"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="800b0-119">Utilisation des fonctions de configuration de l’analyseur de Low-Level</span><span class="sxs-lookup"><span data-stu-id="800b0-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="800b0-120">Avant d’utiliser les fonctions de configuration de l’analyse de bas niveau, vous devez vous familiariser avec ces normes :</span><span class="sxs-lookup"><span data-stu-id="800b0-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="800b0-121">Afficher l’interface de commande de canal de données (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="800b0-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="800b0-122">Jeu de commandes de contrôle du moniteur VESA (MCCS)</span><span class="sxs-lookup"><span data-stu-id="800b0-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="800b0-123">Les fonctions de bas niveau fonctionnent en obtenant et en définissant les valeurs des codes du panneau de configuration virtuel (VCP).</span><span class="sxs-lookup"><span data-stu-id="800b0-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="800b0-124">Un code VCP peut être *continu* ou *incontinu*.</span><span class="sxs-lookup"><span data-stu-id="800b0-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="800b0-125">Les codes continus peuvent supposer toute valeur comprise entre zéro et une valeur maximale spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="800b0-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="800b0-126">Les codes non continus prennent en charge un ensemble défini de valeurs, qui est également spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="800b0-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="800b0-127">Pour utiliser les fonctions de configuration de l’analyse de bas niveau, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="800b0-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="800b0-128">Obtenez un handle **HMONITOR** en appelant [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) ou [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span><span class="sxs-lookup"><span data-stu-id="800b0-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="800b0-129">Appelez [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) pour connaître le nombre d’analyses physiques associées au descripteur **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="800b0-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="800b0-130">Appelez [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) pour obtenir la liste des descripteurs des analyses physiques.</span><span class="sxs-lookup"><span data-stu-id="800b0-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="800b0-131">Appelez [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) pour obtenir la longueur de la chaîne de fonctionnalités DDC/ci d’un moniteur.</span><span class="sxs-lookup"><span data-stu-id="800b0-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="800b0-132">La chaîne de fonctionnalités est une chaîne ASCII qui contient des informations statiques sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="800b0-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="800b0-133">Une partie de la chaîne répertorie les codes VCP pris en charge par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="800b0-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="800b0-134">La chaîne répertorie également les valeurs prises en charge par les codes VCP qui ne sont pas continus.</span><span class="sxs-lookup"><span data-stu-id="800b0-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="800b0-135">Allouez une mémoire tampon pour stocker la chaîne de fonctionnalités et appelez [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) pour obtenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="800b0-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="800b0-136">Analyser la chaîne de fonctionnalités pour déterminer les codes VCP pris en charge par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="800b0-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="800b0-137">Pour un code VCP continu, appelez [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) pour obtenir les valeurs actuelles et maximales du code.</span><span class="sxs-lookup"><span data-stu-id="800b0-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="800b0-138">Pour un code VCP non continu, analysez la chaîne Capabilities pour obtenir les valeurs prises en charge.</span><span class="sxs-lookup"><span data-stu-id="800b0-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="800b0-139">Appelez [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) pour définir une nouvelle valeur pour un code VCP.</span><span class="sxs-lookup"><span data-stu-id="800b0-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="800b0-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="800b0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="800b0-141">**Utilisation de la configuration de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="800b0-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 