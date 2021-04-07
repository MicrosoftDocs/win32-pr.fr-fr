---
title: Utilisation de canaux authentifiés sécurisés
description: Utilisation de canaux authentifiés sécurisés
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Gestionnaire de périphériques Windows Media, authentification
- Gestionnaire de périphériques, authentification
- applications de bureau, authentification
- fournisseurs de services, authentification
- Guide de programmation, authentification
- Authentification
- Gestionnaire de périphériques Windows Media, communications sécurisées
- Gestionnaire de périphériques, communications sécurisées
- applications de bureau, communications sécurisées
- fournisseurs de services, communications sécurisées
- Guide de programmation, communications sécurisées
- communications sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028839"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="391de-115">Utilisation de canaux authentifiés sécurisés</span><span class="sxs-lookup"><span data-stu-id="391de-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="391de-116">Windows Media Gestionnaire de périphériques permet l’authentification et la communication sécurisée entre les composants en fournissant deux classes d’assistance, [CSecureChannelClient](csecurechannelclient-class.md) (pour les applications) et [CSecureChannelServer](csecurechannelserver-class.md) (pour les fournisseurs de services), et une interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (pour les deux).</span><span class="sxs-lookup"><span data-stu-id="391de-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="391de-117">Ensemble, ils composent une API pour l’utilisation de canaux authentifiés sécurisés (SAC).</span><span class="sxs-lookup"><span data-stu-id="391de-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="391de-118">SAC gère les trois tâches suivantes pour les fournisseurs de services ou les applications à l’aide de Windows Media Gestionnaire de périphériques :</span><span class="sxs-lookup"><span data-stu-id="391de-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="391de-119">Authentification du composant</span><span class="sxs-lookup"><span data-stu-id="391de-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="391de-120">Chiffrement et déchiffrement</span><span class="sxs-lookup"><span data-stu-id="391de-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="391de-121">Authentification des messages</span><span class="sxs-lookup"><span data-stu-id="391de-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="391de-122">Une application ou un fournisseur de services doit gérer l’authentification, le chiffrement et le déchiffrement des composants ; l’authentification des messages est facultative.</span><span class="sxs-lookup"><span data-stu-id="391de-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="391de-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="391de-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="391de-124">**Tâches communes aux applications et aux fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="391de-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




