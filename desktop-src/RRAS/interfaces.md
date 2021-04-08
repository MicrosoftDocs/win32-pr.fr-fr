---
title: Interfaces RAS
description: Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841721"
---
# <a name="ras-interfaces"></a><span data-ttu-id="b3bc6-103">Interfaces RAS</span><span class="sxs-lookup"><span data-stu-id="b3bc6-103">RAS interfaces</span></span>

<span data-ttu-id="b3bc6-104">Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="b3bc6-105">Chaque interface possède un identificateur unique sur le routeur.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="b3bc6-106">Les interfaces actives disposent d’un adaptateur fournissant une connectivité au réseau qu’ils représentent.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="b3bc6-107">Les interfaces inactives n’ont pas d’adaptateur assurant la connectivité, sauf si un administrateur a désactivé l’interface après qu’elle avait déjà un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="b3bc6-108">Le routage d’un paquet vers un réseau représenté par une interface force le routeur à allouer un adaptateur pour cette interface et à établir une connexion de réseau étendu (WAN) au réseau distant.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="b3bc6-109">L’allocation d’un adaptateur à une interface est appelée *liaison*.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="b3bc6-110">Les interfaces sont des objets gérables.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="b3bc6-111">Chaque interface apparaît sous la forme d’une ligne dans la table d’interface de la MIB SNMP appropriée.</span><span class="sxs-lookup"><span data-stu-id="b3bc6-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>