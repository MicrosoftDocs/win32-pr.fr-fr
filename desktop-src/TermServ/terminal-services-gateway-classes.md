---
title: Classes de passerelle Bureau à distance
description: Le fournisseur WMI de la passerelle Bureau à distance (passerelle des services Bureau à distance) fournit les classes suivantes.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675061"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="b3185-103">Classes de passerelle Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b3185-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="b3185-104">Le fournisseur WMI de la passerelle Bureau à distance (passerelle des services Bureau à distance) fournit les classes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b3185-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b3185-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b3185-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b3185-106">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="b3185-107">Représente une connexion entre un ordinateur client et un serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-108">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="b3185-109">Décrit une stratégie d’autorisation de connexion Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="b3185-110">Les points d’accès aux services Bureau à distance permettent de déterminer si un utilisateur est autorisé à se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-111">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="b3185-112">Décrit un ensemble de serveurs d’équilibrage de charge de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="b3185-113">Ils sont utilisés pour équilibrer la charge des connexions de passerelle Bureau à distance sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="b3185-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-114">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="b3185-115">Décrit un serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS), qui dispose d’un ensemble de stratégies d’autorisation de connexion Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-116">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="b3185-117">Décrit une stratégie d’autorisation des ressources Bureau à distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="b3185-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="b3185-118">Un RAP RD est utilisé pour déterminer si un utilisateur est autorisé à se connecter à une ressource spécifiée via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-119">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="b3185-120">Décrit un groupe de ressources, qui mappe un ensemble de ressources (noms d’ordinateur) à une entité unique.</span><span class="sxs-lookup"><span data-stu-id="b3185-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-121">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="b3185-122">Utilisé pour les opérations spécifiques au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="b3185-123">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b3185-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="b3185-124">Fournit des méthodes et des propriétés permettant d’afficher et de configurer les paramètres du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3185-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




