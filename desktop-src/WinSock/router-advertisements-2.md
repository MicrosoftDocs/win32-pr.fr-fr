---
description: Le contenu des publications de routeur IPv6 est dérivé automatiquement des itinéraires publiés dans la table de routage. Les itinéraires non publiés sont utilisés pour le routage, mais sont ignorés lors de la construction des publications de routeur.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Annonces de routeur IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531876"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="77f12-104">Annonces de routeur IPv6</span><span class="sxs-lookup"><span data-stu-id="77f12-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="77f12-105">Le contenu des publications de routeur IPv6 est dérivé automatiquement des itinéraires publiés dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="77f12-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="77f12-106">Les itinéraires non publiés sont utilisés pour le routage, mais sont ignorés lors de la construction des publications de routeur.</span><span class="sxs-lookup"><span data-stu-id="77f12-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="77f12-107">Les annonces de routeur pour IPv6 contiennent toujours une option d’adresse de couche de liaison source et une option MTU.</span><span class="sxs-lookup"><span data-stu-id="77f12-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="77f12-108">La valeur de l’option MTU est extraite de l’unité de transmission de liens actuelle de l’interface d’envoi.</span><span class="sxs-lookup"><span data-stu-id="77f12-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="77f12-109">Cette valeur peut être modifiée à l’aide de la commande IPv6 IFC MTU.</span><span class="sxs-lookup"><span data-stu-id="77f12-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="77f12-110">L’annonce de routeur n’a qu’une durée de vie de routeur différente de zéro si un itinéraire par défaut est publié.</span><span class="sxs-lookup"><span data-stu-id="77f12-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="77f12-111">Un itinéraire par défaut est un itinéraire pour le préfixe de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="77f12-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="77f12-112">Les itinéraires sur liaison publiés entraînent des options d’informations de préfixe dans les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="77f12-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="77f12-113">Si le préfixe on-Link a 64 bits, l’option informations sur le préfixe a les deux bits, et les hôtes les recevant configurent automatiquement les adresses.</span><span class="sxs-lookup"><span data-stu-id="77f12-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="77f12-114">Une interface qui envoie des annonces de routeur configure également automatiquement les adresses pour elle-même en fonction des options d’informations de préfixe qu’elle envoie.</span><span class="sxs-lookup"><span data-stu-id="77f12-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="77f12-115">Une durée de vie non âgée finie sur tous les itinéraires publiés (par exemple, 30 minutes) est recommandée.</span><span class="sxs-lookup"><span data-stu-id="77f12-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="77f12-116">Si vous décidez de retirer un itinéraire, vous pouvez modifier l’itinéraire pour avoir une durée de vie chronologique.</span><span class="sxs-lookup"><span data-stu-id="77f12-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="77f12-117">L’itinéraire vieillit au cours de plusieurs publications de routeur, puis disparaissent du routeur et des hôtes recevant les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="77f12-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="77f12-118">Les itinéraires qui hébergent les annonces par l’intermédiaire des publications de routeur et ne sont pas publiés.</span><span class="sxs-lookup"><span data-stu-id="77f12-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="77f12-119">Les adresses sont également configurées automatiquement à partir de l’ancienneté des publications de routeur.</span><span class="sxs-lookup"><span data-stu-id="77f12-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



