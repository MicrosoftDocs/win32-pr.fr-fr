---
description: AppInit_DLLs dans Windows 7 et Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088707"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="1caab-103">\_DLL AppInit dans Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1caab-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="1caab-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="1caab-104">Platform</span></span>

<span data-ttu-id="1caab-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1caab-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1caab-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1caab-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1caab-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1caab-107">Feature Impact</span></span>

 <span data-ttu-id="1caab-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="1caab-108">**Severity** - Low</span></span>  
<span data-ttu-id="1caab-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="1caab-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="1caab-110">Description</span><span class="sxs-lookup"><span data-stu-id="1caab-110">Description</span></span>

<span data-ttu-id="1caab-111">\_Les DLL AppInit sont un mécanisme qui permet de charger une liste arbitraire de dll dans chaque processus en mode utilisateur sur le système.</span><span class="sxs-lookup"><span data-stu-id="1caab-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="1caab-112">Microsoft modifie la fonction des DLL AppInit dans Windows 7 et Windows Server 2008 R2 afin d’ajouter une nouvelle exigence de signature de code.</span><span class="sxs-lookup"><span data-stu-id="1caab-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="1caab-113">Cela vous aidera à améliorer la fiabilité et les performances du système, ainsi qu’à améliorer la visibilité de l’origine des logiciels.</span><span class="sxs-lookup"><span data-stu-id="1caab-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="1caab-114">Configuration</span><span class="sxs-lookup"><span data-stu-id="1caab-114">Configuration</span></span>

<span data-ttu-id="1caab-115">Les valeurs stockées sous la \_ \_ clé Windows du logiciel HKEY local machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ dans le registre déterminent le comportement de l' \_ infrastructure des DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="1caab-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="1caab-116">Le tableau ci-dessous décrit les valeurs de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="1caab-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1caab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1caab-117">Value</span></span></th>
<th><span data-ttu-id="1caab-118">Description</span><span class="sxs-lookup"><span data-stu-id="1caab-118">Description</span></span></th>
<th><span data-ttu-id="1caab-119">Exemples de valeurs</span><span class="sxs-lookup"><span data-stu-id="1caab-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="1caab-120">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1caab-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1caab-121">Active ou désactive globalement AppInit_DLLs. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1caab-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1caab-122">0x0 – AppInit_DLLs sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="1caab-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1caab-123">0x1 – AppInit_DLLs sont activés.</span><span class="sxs-lookup"><span data-stu-id="1caab-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="1caab-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="1caab-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="1caab-125">Espace ou liste délimitée par des virgules des dll à charger.</span><span class="sxs-lookup"><span data-stu-id="1caab-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="1caab-126">Le chemin d’accès complet à la DLL doit être spécifié à l’aide de noms courts.</span><span class="sxs-lookup"><span data-stu-id="1caab-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="1caab-127">C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="1caab-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="1caab-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1caab-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="1caab-129">Charge uniquement les dll signées par code. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1caab-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="1caab-130">0x0 – charger les dll.</span><span class="sxs-lookup"><span data-stu-id="1caab-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1caab-131">0x1 : charge uniquement les dll signées par le code.</span><span class="sxs-lookup"><span data-stu-id="1caab-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="1caab-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="1caab-132">**Windows 7**</span></span>

<span data-ttu-id="1caab-133">Toutes les dll qui sont chargées par l' \_ infrastructure des DLL AppInit doivent être signées par un code.</span><span class="sxs-lookup"><span data-stu-id="1caab-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="1caab-134">Dans l’intérêt de la compatibilité des applications, le système d’exploitation Windows 7 charge toutes les DLL AppInit.</span><span class="sxs-lookup"><span data-stu-id="1caab-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="1caab-135">Toutefois, Microsoft recommande à tous les développeurs d’applications de signer le code de leurs dll pour contribuer à l’amélioration de la fiabilité de Windows et à la préparation de la mise en œuvre de la signature de code dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="1caab-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="1caab-136">La \_ clé de Registre RequireSignedAppInit dll contrôle ce comportement et sa valeur sur Windows 7 est définie par défaut sur 0.</span><span class="sxs-lookup"><span data-stu-id="1caab-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="1caab-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1caab-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="1caab-138">Toutes les dll qui sont chargées par l' \_ infrastructure des DLL AppInit doivent être signées par un code.</span><span class="sxs-lookup"><span data-stu-id="1caab-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="1caab-139">La \_ clé de Registre RequireSignedAppInit dll contrôle ce comportement et sa valeur sur Windows Server 2008 R2 est définie sur 1 par défaut.</span><span class="sxs-lookup"><span data-stu-id="1caab-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1caab-140">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="1caab-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="1caab-141">DLL AppInit dans Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1caab-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
