---
title: Versions de contrôle courantes
description: Cette rubrique répertorie les versions disponibles de la bibliothèque de contrôles communs (ComCtl32.dll), décrit comment identifier la version utilisée par votre application et explique comment cibler votre application pour une version spécifique.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463963"
---
# <a name="common-control-versions"></a><span data-ttu-id="c3431-103">Versions de contrôle courantes</span><span class="sxs-lookup"><span data-stu-id="c3431-103">Common Control Versions</span></span>

<span data-ttu-id="c3431-104">Cette rubrique répertorie les versions disponibles de la bibliothèque de contrôles communs (ComCtl32.dll), décrit comment identifier la version utilisée par votre application et explique comment cibler votre application pour une version spécifique.</span><span class="sxs-lookup"><span data-stu-id="c3431-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="c3431-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3431-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c3431-106">Numéros des versions des DLL de contrôle courantes</span><span class="sxs-lookup"><span data-stu-id="c3431-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="c3431-107">Tailles de structure pour différentes versions de contrôle communes</span><span class="sxs-lookup"><span data-stu-id="c3431-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="c3431-108">Utilisation de DllGetVersion pour déterminer le numéro de version</span><span class="sxs-lookup"><span data-stu-id="c3431-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="c3431-109">Versions du projet</span><span class="sxs-lookup"><span data-stu-id="c3431-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="c3431-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3431-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="c3431-111">Numéros des versions des DLL de contrôle courantes</span><span class="sxs-lookup"><span data-stu-id="c3431-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="c3431-112">La prise en charge des contrôles communs est fournie par ComCtl32.dll, qui incluent toutes les versions 32 bits et 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3431-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="c3431-113">Chaque version successive de la DLL prend en charge les fonctionnalités et l’API des versions antérieures et ajoute de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c3431-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="c3431-114">Étant donné que différentes versions de ComCtl32.dll ont été distribuées avec Internet Explorer, la version qui est active est parfois différente de la version fournie avec le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c3431-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="c3431-115">Par conséquent, votre application doit déterminer directement la version de ComCtl32.dll présente.</span><span class="sxs-lookup"><span data-stu-id="c3431-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="c3431-116">Dans la documentation de référence des contrôles communs, de nombreux éléments de programmation spécifient un numéro de version DLL minimal pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c3431-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="c3431-117">Ce numéro de version indique que l’élément de programmation est implémenté dans cette version et les versions ultérieures de la DLL, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="c3431-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="c3431-118">Si aucun numéro de version n’est spécifié, l’élément de programmation est implémenté dans toutes les versions existantes de la DLL.</span><span class="sxs-lookup"><span data-stu-id="c3431-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="c3431-119">Le tableau suivant présente les différentes versions des DLL et la façon dont elles ont été distribuées sur les systèmes d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c3431-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="c3431-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="c3431-120">ComCtl32.dll</span></span>

<span data-ttu-id="c3431-121">Version</span><span class="sxs-lookup"><span data-stu-id="c3431-121">Version</span></span>

<span data-ttu-id="c3431-122">Plateforme de distribution</span><span class="sxs-lookup"><span data-stu-id="c3431-122">Distribution Platform</span></span>

<span data-ttu-id="c3431-123">5,81</span><span class="sxs-lookup"><span data-stu-id="c3431-123">5.81</span></span>

<span data-ttu-id="c3431-124">Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 et Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="c3431-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="c3431-125">5,82</span><span class="sxs-lookup"><span data-stu-id="c3431-125">5.82</span></span>

<span data-ttu-id="c3431-126">Windows Server 2003, Windows Vista, Windows Server 2008 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3431-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="c3431-127">6.0</span><span class="sxs-lookup"><span data-stu-id="c3431-127">6.0</span></span>

<span data-ttu-id="c3431-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3431-128">Windows Server 2003</span></span>

<span data-ttu-id="c3431-129">6.10</span><span class="sxs-lookup"><span data-stu-id="c3431-129">6.10</span></span>

<span data-ttu-id="c3431-130">Windows Vista, Windows Server 2008 et Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3431-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="c3431-131">Tailles de structure pour différentes versions de contrôle communes</span><span class="sxs-lookup"><span data-stu-id="c3431-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="c3431-132">L’amélioration continue des contrôles communs a entraîné la nécessité d’étendre un grand nombre de structures.</span><span class="sxs-lookup"><span data-stu-id="c3431-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="c3431-133">Pour cette raison, la taille des structures a changé entre les différentes versions de commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="c3431-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="c3431-134">Étant donné que la plupart des structures de contrôle courantes prennent une taille de structure comme l’un des paramètres, un message ou une fonction peut échouer si la taille n’est pas reconnue.</span><span class="sxs-lookup"><span data-stu-id="c3431-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="c3431-135">Pour y remédier, les constantes de taille de structure ont été définies pour faciliter le ciblage d’une version différente de ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="c3431-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="c3431-136">La liste suivante définit les constantes de taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="c3431-136">The following list defines the structure size constants.</span></span>



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3431-137">\_Taille HDITEM v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-137">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="c3431-138">Taille de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-138">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="c3431-139">Taille de IMAGELISTDRAWPARAMS \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-139">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="c3431-140">Taille de la structure [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) dans la version 5,9.</span><span class="sxs-lookup"><span data-stu-id="c3431-140">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="c3431-141">\_Taille LVCOLUMN v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-141">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="c3431-142">Taille de la structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-142">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="c3431-143">Taille de LVGROUP \_ v5 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-143">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="c3431-144">Taille de la structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dans la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-144">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="c3431-145">\_Taille LVHITTESTINFO v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-145">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="c3431-146">Taille de la structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-146">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c3431-147">\_Taille LVITEM v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-147">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="c3431-148">Taille de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-148">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="c3431-149">Taille de LVITEM \_ v5 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-149">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="c3431-150">Taille de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dans la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="c3431-151">Taille de LVTILEINFO \_ v5 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-151">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="c3431-152">Taille de la structure [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) dans la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-152">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="c3431-153">\_Taille MCHITTESTINFO v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-153">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="c3431-154">Taille de la structure [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-154">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c3431-155">Taille de NMLVCUSTOMDRAW \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-155">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="c3431-156">Taille de la structure [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) dans la version 4,7.</span><span class="sxs-lookup"><span data-stu-id="c3431-156">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="c3431-157">\_Taille NMTTDISPINFO v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-157">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="c3431-158">Taille de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-158">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="c3431-159">Taille de NMTVCUSTOMDRAW \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-159">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="c3431-160">Taille de la structure [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) dans la version 4,7.</span><span class="sxs-lookup"><span data-stu-id="c3431-160">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="c3431-161">\_Taille PROPSHEETHEADER v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-161">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="c3431-162">Taille de la structure [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-162">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="c3431-163">\_Taille PROPSHEETPAGE v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-163">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="c3431-164">Taille de la structure [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-164">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="c3431-165">Taille de REBARBANDINFO \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-165">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="c3431-166">Taille de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) dans la version 4,7.</span><span class="sxs-lookup"><span data-stu-id="c3431-166">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="c3431-167">Taille de REBARBANDINFO \_ V6 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-167">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="c3431-168">Taille de la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) dans la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="c3431-169">\_Taille TTTOOLINFO v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-169">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="c3431-170">Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-170">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="c3431-171">Taille de TTTOOLINFO \_ v2 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-171">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="c3431-172">Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 4,7.</span><span class="sxs-lookup"><span data-stu-id="c3431-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="c3431-173">Taille de TTTOOLINFO \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-173">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="c3431-174">Taille de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) dans la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="c3431-175">\_Taille TVINSERTSTRUCT v1 \_</span><span class="sxs-lookup"><span data-stu-id="c3431-175">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="c3431-176">Taille de la structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) dans la version 4,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-176">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="c3431-177">Utilisation de DllGetVersion pour déterminer le numéro de version</span><span class="sxs-lookup"><span data-stu-id="c3431-177">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="c3431-178">La fonction [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) peut être appelée par une application pour déterminer la version de la dll qui est présente sur le système.</span><span class="sxs-lookup"><span data-stu-id="c3431-178">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="c3431-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="c3431-179">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="c3431-180">En plus des informations fournies via [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** fournit également le numéro de correctif qui identifie le dernier Service Pack installé, ce qui offre un moyen plus robuste de comparer les numéros de version.</span><span class="sxs-lookup"><span data-stu-id="c3431-180">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="c3431-181">Étant donné que le premier membre de **DLLVERSIONINFO2** est une structure **DLLVERSIONINFO** , la structure la plus récente est à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="c3431-181">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="c3431-182">L’exemple de fonction suivant `GetVersion` charge une DLL spécifiée et tente d’appeler sa fonction [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="c3431-182">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="c3431-183">En cas de réussite, elle utilise une macro pour empaqueter les numéros de version majeure et mineure de la structure [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) dans une **valeur DWORD** qui est retournée à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="c3431-183">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="c3431-184">Si la DLL n’exporte pas **DllGetVersion**, la fonction retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c3431-184">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="c3431-185">Vous pouvez modifier la fonction pour gérer la possibilité que **DllGetVersion** retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="c3431-185">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="c3431-186">Dans ce cas, utilisez les informations contenues dans le membre **ullVersion** de la structure **DLLVERSIONINFO2** pour comparer les versions, les numéros de build et les versions de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="c3431-186">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="c3431-187">La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifie la tâche de comparaison de ces valeurs à celles de **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="c3431-187">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="c3431-188">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c3431-188">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="c3431-189">Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3431-189">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="c3431-190">L’exemple de code suivant montre comment vous pouvez utiliser `GetVersion` pour tester si ComCtl32.dll est la version 6,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c3431-190">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="c3431-191">Versions du projet</span><span class="sxs-lookup"><span data-stu-id="c3431-191">Project Versions</span></span>

<span data-ttu-id="c3431-192">Pour garantir la compatibilité de votre application avec différentes versions ciblées d’un fichier. dll, les macros de version sont présentes dans les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c3431-192">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="c3431-193">Ces macros permettent de définir, d’exclure ou de redéfinir certaines définitions pour les différentes versions de la DLL.</span><span class="sxs-lookup"><span data-stu-id="c3431-193">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="c3431-194">Pour une description détaillée de ces macros, consultez [utilisation des en-têtes Windows](/windows/desktop/WinProg/using-the-windows-headers) .</span><span class="sxs-lookup"><span data-stu-id="c3431-194">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="c3431-195">Par exemple, le nom de macro **\_ Win32 \_ IE** se trouve généralement dans les en-têtes plus anciens.</span><span class="sxs-lookup"><span data-stu-id="c3431-195">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="c3431-196">Vous êtes responsable de la définition de la macro sous la forme d’un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="c3431-196">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="c3431-197">Ce numéro de version définit la version cible de l’application qui utilise la DLL.</span><span class="sxs-lookup"><span data-stu-id="c3431-197">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="c3431-198">Le tableau suivant répertorie les numéros de version disponibles et l’effet de chacun d’entre eux sur votre application.</span><span class="sxs-lookup"><span data-stu-id="c3431-198">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="c3431-199">Version</span><span class="sxs-lookup"><span data-stu-id="c3431-199">Version</span></span> | <span data-ttu-id="c3431-200">Description</span><span class="sxs-lookup"><span data-stu-id="c3431-200">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3431-201">0x0300</span><span class="sxs-lookup"><span data-stu-id="c3431-201">0x0300</span></span>  | <span data-ttu-id="c3431-202">L’application est compatible avec ComCtl32.dll version 4,70 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-202">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="c3431-203">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,70.</span><span class="sxs-lookup"><span data-stu-id="c3431-203">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="c3431-204">0x0400</span><span class="sxs-lookup"><span data-stu-id="c3431-204">0x0400</span></span>  | <span data-ttu-id="c3431-205">L’application est compatible avec ComCtl32.dll version 4,71 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-205">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="c3431-206">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,71.</span><span class="sxs-lookup"><span data-stu-id="c3431-206">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="c3431-207">0x0401</span><span class="sxs-lookup"><span data-stu-id="c3431-207">0x0401</span></span>  | <span data-ttu-id="c3431-208">L’application est compatible avec ComCtl32.dll version 4,72 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-208">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="c3431-209">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,72.</span><span class="sxs-lookup"><span data-stu-id="c3431-209">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="c3431-210">0x0500</span><span class="sxs-lookup"><span data-stu-id="c3431-210">0x0500</span></span>  | <span data-ttu-id="c3431-211">L’application est compatible avec ComCtl32.dll version 5,80 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-211">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="c3431-212">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,80.</span><span class="sxs-lookup"><span data-stu-id="c3431-212">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="c3431-213">0x0501</span><span class="sxs-lookup"><span data-stu-id="c3431-213">0x0501</span></span>  | <span data-ttu-id="c3431-214">L’application est compatible avec ComCtl32.dll version 5,81 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-214">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="c3431-215">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,81.</span><span class="sxs-lookup"><span data-stu-id="c3431-215">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="c3431-216">0x0600</span><span class="sxs-lookup"><span data-stu-id="c3431-216">0x0600</span></span>  | <span data-ttu-id="c3431-217">L’application est compatible avec ComCtl32.dll version 6,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3431-217">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="c3431-218">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3431-218">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="c3431-219">Si vous ne définissez pas la macro **\_ Win32 \_ IE** dans votre projet, elle est automatiquement définie en tant que 0x0500.</span><span class="sxs-lookup"><span data-stu-id="c3431-219">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="c3431-220">Pour définir une valeur différente, vous pouvez ajouter les éléments suivants aux directives de compilateur dans votre fichier Make ; Remplacez 0x0400 par le numéro de version de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c3431-220">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="c3431-221">Une autre méthode consiste à ajouter une ligne semblable à la suivante dans votre code source avant d’inclure les fichiers d’en-tête de Shell.</span><span class="sxs-lookup"><span data-stu-id="c3431-221">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="c3431-222">Remplacez 0x0400 par le numéro de version de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c3431-222">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="c3431-223">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3431-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3431-224">À propos des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="c3431-224">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 