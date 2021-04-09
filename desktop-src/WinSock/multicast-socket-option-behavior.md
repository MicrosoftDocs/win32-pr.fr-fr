---
description: Cette page décrit le comportement des options de socket de multidiffusion en fonction des différents États des paramètres d’option de Socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportement des options de socket de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033978"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="f3904-103">Comportement des options de socket de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="f3904-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="f3904-104">Cette page décrit le comportement des options de socket de multidiffusion en fonction des différents États des paramètres d’option de Socket.</span><span class="sxs-lookup"><span data-stu-id="f3904-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="f3904-105">Par exemple, cette page décrit le comportement lorsque l' \_ option de \_ Socket d’appartenance source d’ajout d’adresses IP \_ est définie sur un socket pour lequel l’option d’appartenance à une source d’ajout d’adresses IP \_ \_ \_ a déjà été définie avec la paire groupe/source spécifiée sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="f3904-106">Il est autorisé à appeler IP \_ Add \_ source \_ membership sur le même groupe sur une autre interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="f3904-107">Cette page vous aide à concevoir et à dépanner les applications de multidiffusion Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="f3904-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f3904-108">Option de socket initiale</span><span class="sxs-lookup"><span data-stu-id="f3904-108">Initial socket option</span></span></th>
<th><span data-ttu-id="f3904-109">Option de socket suivante en conflit</span><span class="sxs-lookup"><span data-stu-id="f3904-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="f3904-110">Erreur retournée</span><span class="sxs-lookup"><span data-stu-id="f3904-110">Error returned</span></span></th>
<th><span data-ttu-id="f3904-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3904-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="f3904-112">IP_ADD_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f3904-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f3904-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-115">N’appelez pas IP_ADD_MEMBERSHIP avec le même groupe plusieurs fois sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3904-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-118">N’appelez pas IP_ADD_SOURCE_MEMBERSHIP avec le même groupe précédemment appelé avec IP_ADD_MEMBERSHIP sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f3904-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-120">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-121">Utilisez à la place IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="f3904-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f3904-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-123">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-124">Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f3904-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-126">Tout appel ultérieur sur la même paire groupe/groupe/source</span><span class="sxs-lookup"><span data-stu-id="f3904-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="f3904-127">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-128">La création d’appels d’option de socket sur une paire groupe ou groupe/source qui n’est pas actuellement dans la liste d’inclusion (en raison de la suppression de l’appartenance, ou autre) entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="f3904-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="f3904-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f3904-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f3904-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-132">N’appelez pas IP_ADD_MEMBERSHIP avec le même groupe précédemment appelé avec IP_ADD_SOURCE_MEMBERSHIP sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3904-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-135">N’appelez pas IP_ADD_SOURCE_MEMBERSHIP avec la même paire groupe/source précédemment appelée avec IP_ADD_SOURCE_MEMBERSHIP sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f3904-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-137">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-138">Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f3904-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f3904-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f3904-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-141">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-142">Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3904-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-145">Retourne une erreur lors de la tentative de suppression d’une paire groupe/source qui ne figure pas dans la liste d’inclusion sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f3904-146">IP_BLOCK_SOURCE $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f3904-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f3904-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-149">Retourne une erreur lors de la tentative de blocage d’une paire groupe/source déjà bloquée sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3904-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-151">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-152">Utilisez à la place IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="f3904-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f3904-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="f3904-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="f3904-154">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="f3904-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="f3904-155">Utilisez à la place IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="f3904-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f3904-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="f3904-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="f3904-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="f3904-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="f3904-159">Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’est pas dans la liste bloquée sur la même interface réseau.</span><span class="sxs-lookup"><span data-stu-id="f3904-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



