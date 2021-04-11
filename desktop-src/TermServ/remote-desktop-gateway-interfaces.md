---
title: Interfaces de passerelle Bureau à distance
description: L’API Bureau à distance Gateway (passerelle des services Bureau à distance) prend en charge les interfaces suivantes. Vous pouvez utiliser ces interfaces pour implémenter des plug-ins qui fournissent une authentification et une autorisation personnalisées.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939693"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="4eee9-104">Interfaces de passerelle Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="4eee9-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="4eee9-105">L’API Bureau à distance Gateway (passerelle des services Bureau à distance) prend en charge les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="4eee9-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="4eee9-106">Vous pouvez utiliser ces interfaces pour implémenter des plug-ins qui fournissent une authentification et une autorisation personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4eee9-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="4eee9-107">Il n’existe aucune dépendance entre le plug-in d’authentification et le plug-in d’autorisation, et vous ne pouvez implémenter qu’un seul plug-in si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="4eee9-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="4eee9-108">Les plug-ins d’authentification sont [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) et [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="4eee9-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="4eee9-109">Les plug-ins d’autorisation sont [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)et [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="4eee9-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4eee9-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4eee9-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4eee9-111">**ITSGAccountingEngine**</span><span class="sxs-lookup"><span data-stu-id="4eee9-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="4eee9-112">Expose des méthodes qui fournissent des informations sur la création ou la fermeture de sessions pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="4eee9-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4eee9-113">**ITSGAuthenticateUserSink**</span><span class="sxs-lookup"><span data-stu-id="4eee9-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="4eee9-114">Expose les méthodes qui notifient la passerelle des services Bureau à distance des événements d’authentification.</span><span class="sxs-lookup"><span data-stu-id="4eee9-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="4eee9-115">**ITSGAuthenticationEngine**</span><span class="sxs-lookup"><span data-stu-id="4eee9-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="4eee9-116">Expose des méthodes qui authentifient les utilisateurs pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4eee9-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="4eee9-117">**ITSGAuthorizeConnectionSink**</span><span class="sxs-lookup"><span data-stu-id="4eee9-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="4eee9-118">Expose les méthodes qui notifient la passerelle des services Bureau à distance du résultat d’une tentative d’autorisation d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="4eee9-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4eee9-119">**ITSGAuthorizeResourceSink**</span><span class="sxs-lookup"><span data-stu-id="4eee9-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="4eee9-120">Expose les méthodes qui notifient la passerelle des services Bureau à distance du résultat d’une tentative d’autorisation d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="4eee9-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="4eee9-121">**ITSGPolicyEngine**</span><span class="sxs-lookup"><span data-stu-id="4eee9-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="4eee9-122">Expose des méthodes qui autorisent les connexions et les ressources.</span><span class="sxs-lookup"><span data-stu-id="4eee9-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




