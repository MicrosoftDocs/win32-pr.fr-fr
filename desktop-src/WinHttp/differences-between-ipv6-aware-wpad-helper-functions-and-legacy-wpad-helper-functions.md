---
title: IPv6-Aware et fonctions d’assistance WPAD existantes
description: Différences entre les fonctions d’assistance WPAD IPv6-Aware et les fonctions d’assistance WPAD héritées
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524364"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="e326a-103">IPv6-Aware et fonctions d’assistance WPAD existantes</span><span class="sxs-lookup"><span data-stu-id="e326a-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="e326a-104">Les tableaux suivants expliquent les différences entre les nouvelles fonctions d’assistance WPAD et les fonctions d’assistance WPAD héritées.</span><span class="sxs-lookup"><span data-stu-id="e326a-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="e326a-105">Les nouvelles fonctions sont marquées d’un astérisque.</span><span class="sxs-lookup"><span data-stu-id="e326a-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e326a-106">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-106">Functions</span></span></th>
<th><span data-ttu-id="e326a-107">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-107">Input</span></span></th>
<th><span data-ttu-id="e326a-108">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-108">Output</span></span></th>
<th><span data-ttu-id="e326a-109">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e326a-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="e326a-110">dnsResolve</span></span></td>
<td><span data-ttu-id="e326a-111">Host</span><span class="sxs-lookup"><span data-stu-id="e326a-111">Host</span></span></td>
<td><span data-ttu-id="e326a-112">Adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="e326a-113">La fonction ex renverra une liste de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="e326a-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="e326a-114">Nécessaire, car les adresses IPv6 ou IPv4 peuvent avoir plusieurs adresses monodiffusion pour une seule interface. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e326a-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e326a-115">dnsResolveEx\*</span><span class="sxs-lookup"><span data-stu-id="e326a-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="e326a-116">Host</span><span class="sxs-lookup"><span data-stu-id="e326a-116">Host</span></span></td>
<td><span data-ttu-id="e326a-117">Liste des adresses IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e326a-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-118">Functions</span></span></th>
<th><span data-ttu-id="e326a-119">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-119">Input</span></span></th>
<th><span data-ttu-id="e326a-120">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-120">Output</span></span></th>
<th><span data-ttu-id="e326a-121">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e326a-122">isResolveable</span><span class="sxs-lookup"><span data-stu-id="e326a-122">isResolveable</span></span></td>
<td><span data-ttu-id="e326a-123">Hôte IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-123">IPv4 host</span></span></td>
<td><span data-ttu-id="e326a-124">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="e326a-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="e326a-125">La fonction ex retourne la valeur TRUE si un hôte peut résoudre une adresse IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="e326a-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="e326a-126">La fonction héritée retourne la valeur TRUE uniquement si l’hôte est résolu en une adresse IPv4. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e326a-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e326a-127">isResolveableEx\*</span><span class="sxs-lookup"><span data-stu-id="e326a-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="e326a-128">Hôte IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="e326a-129">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="e326a-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e326a-130">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-130">Functions</span></span></th>
<th><span data-ttu-id="e326a-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-131">Input</span></span></th>
<th><span data-ttu-id="e326a-132">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-132">Output</span></span></th>
<th><span data-ttu-id="e326a-133">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e326a-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="e326a-134">myIPAddress</span></span></td>
<td><span data-ttu-id="e326a-135">aucun</span><span class="sxs-lookup"><span data-stu-id="e326a-135">none</span></span></td>
<td><span data-ttu-id="e326a-136">Adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="e326a-137">La fonction ex renverra une liste de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="e326a-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="e326a-138">Nécessaire, car les adresses IPv6 ou IPv4 peuvent avoir plusieurs adresses monodiffusion pour une seule interface $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e326a-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e326a-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="e326a-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="e326a-140">aucun</span><span class="sxs-lookup"><span data-stu-id="e326a-140">none</span></span></td>
<td><span data-ttu-id="e326a-141">Liste des adresses IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e326a-142">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-142">Functions</span></span></th>
<th><span data-ttu-id="e326a-143">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-143">Input</span></span></th>
<th><span data-ttu-id="e326a-144">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-144">Output</span></span></th>
<th><span data-ttu-id="e326a-145">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e326a-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="e326a-146">isInNet</span></span></td>
<td><span data-ttu-id="e326a-147">Hôte, modèle d’adresse IP séparée par des points, masque d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e326a-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="e326a-148">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="e326a-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="e326a-149">Indiquez une version IP agnostique pour déterminer si une adresse IP se trouve dans un sous-réseau donné.</span><span class="sxs-lookup"><span data-stu-id="e326a-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="e326a-150">En outre, la notation de masque dans IPv4 est dépréciée. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e326a-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e326a-151">isInNetEx\*</span><span class="sxs-lookup"><span data-stu-id="e326a-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="e326a-152">Préfixe IP de l’adresse IP</span><span class="sxs-lookup"><span data-stu-id="e326a-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="e326a-153">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="e326a-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="e326a-154">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-154">Functions</span></span>           | <span data-ttu-id="e326a-155">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-155">Input</span></span>                       | <span data-ttu-id="e326a-156">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-156">Output</span></span>                             | <span data-ttu-id="e326a-157">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e326a-158">sortIPAddressList\*</span><span class="sxs-lookup"><span data-stu-id="e326a-158">sortIPAddressList\*</span></span> | <span data-ttu-id="e326a-159">Liste des adresses IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="e326a-160">Liste triée des adresses IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="e326a-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="e326a-161">Il n’existe pas de fonction héritée équivalente, car les fonctions héritées ne retournaient qu’une seule adresse IPv4. par conséquent, il n’était pas nécessaire de trier.</span><span class="sxs-lookup"><span data-stu-id="e326a-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="e326a-162">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e326a-162">Functions</span></span>          | <span data-ttu-id="e326a-163">Entrée</span><span class="sxs-lookup"><span data-stu-id="e326a-163">Input</span></span> | <span data-ttu-id="e326a-164">Output</span><span class="sxs-lookup"><span data-stu-id="e326a-164">Output</span></span>                     | <span data-ttu-id="e326a-165">Motif de modification</span><span class="sxs-lookup"><span data-stu-id="e326a-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e326a-166">getClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="e326a-166">getClientVersion\*</span></span> | <span data-ttu-id="e326a-167">aucun</span><span class="sxs-lookup"><span data-stu-id="e326a-167">none</span></span>  | <span data-ttu-id="e326a-168">Numéro de version du moteur WPAD</span><span class="sxs-lookup"><span data-stu-id="e326a-168">WPAD engine version number</span></span> | <span data-ttu-id="e326a-169">Actuellement, cette fonction retourne la version 1,0.</span><span class="sxs-lookup"><span data-stu-id="e326a-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="e326a-170">Nous avons ajouté cette fonction pour permettre aux administrateurs informatiques de mettre à jour leur WPAD pour qu’ils fonctionnent avec différentes versions du moteur WPAD sans causer de ruptures à leur déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="e326a-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="e326a-171">Cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e326a-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



