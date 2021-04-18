---
title: Interfaces pour les fournisseurs de contenu sécurisés
description: Interfaces pour les fournisseurs de contenu sécurisés
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Gestionnaire de périphériques Windows Media, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Référence de programmation, contenu protégé par DRM
- référence pour Windows Media Gestionnaire de périphériques, contenu protégé par DRM
- Contenu protégé par DRM
- Gestionnaire de périphériques Windows Media, fournisseur de contenu sécurisé (SCP)
- Gestionnaire de périphériques, fournisseur de contenu sécurisé (SCP)
- Référence de programmation, fournisseur de contenu sécurisé (SCP)
- référence pour Windows Media Gestionnaire de périphériques, Secure Content Provider (SCP)
- fournisseur de contenu sécurisé (SCP)
- SCP (Secure Content Provider)
- Gestionnaire de périphériques Windows Media, interfaces SCP
- Gestionnaire de périphériques, interfaces SCP
- Référence de programmation, interfaces SCP
- référence pour les Gestionnaire de périphériques Windows Media, les interfaces SCP
- Interfaces SCP, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511832"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="4e873-119">Interfaces pour les fournisseurs de contenu sécurisés</span><span class="sxs-lookup"><span data-stu-id="4e873-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="4e873-120">Un fournisseur de contenu sécurisé (SCP) est un composant de plug-in qui permet à Windows Media Gestionnaire de périphériques de transférer et de demander des informations de droits à un contenu protégé par DRM.</span><span class="sxs-lookup"><span data-stu-id="4e873-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="4e873-121">Microsoft fournit un composant SCP qui peut gérer des fichiers WMA et WMV protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="4e873-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="4e873-122">Si votre appareil ou votre application utilise le contenu protégé par DRM d’autres formats, il doit créer un composant SCP en implémentant toutes ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="4e873-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="4e873-123">Dans le cas contraire, vous n’aurez pas besoin d’utiliser ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="4e873-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="4e873-124">Interface</span><span class="sxs-lookup"><span data-stu-id="4e873-124">Interface</span></span>                                                  | <span data-ttu-id="4e873-125">Description</span><span class="sxs-lookup"><span data-stu-id="4e873-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e873-126">**ISCPSecureAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="4e873-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="4e873-127">Interface principale du fournisseur de contenu sécurisé.</span><span class="sxs-lookup"><span data-stu-id="4e873-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="4e873-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="4e873-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="4e873-129">Étend **ISCPSecureAuthenticate** en fournissant un moyen d’obtenir un objet de session.</span><span class="sxs-lookup"><span data-stu-id="4e873-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4e873-130">**ISCPSecureExchange**</span><span class="sxs-lookup"><span data-stu-id="4e873-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="4e873-131">Utilisé pour échanger du contenu sécurisé et des droits associés au contenu.</span><span class="sxs-lookup"><span data-stu-id="4e873-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="4e873-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="4e873-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="4e873-133">Étend **ISCPSecureExchange** en fournissant une nouvelle version de la méthode **TransferContainerData** .</span><span class="sxs-lookup"><span data-stu-id="4e873-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="4e873-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="4e873-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="4e873-135">Étend **ISCPSecureExchange2** en fournissant des performances d’échange de données améliorées et une méthode de rappel de transfert complet.</span><span class="sxs-lookup"><span data-stu-id="4e873-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="4e873-136">**ISCPSecureQuery**</span><span class="sxs-lookup"><span data-stu-id="4e873-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="4e873-137">Interrogé par Windows Media Gestionnaire de périphériques pour déterminer la propriété du contenu sécurisé.</span><span class="sxs-lookup"><span data-stu-id="4e873-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="4e873-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="4e873-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="4e873-139">Étend **ISCPSecureQuery** via une fonctionnalité qui détermine si le fournisseur de contenu sécurisé est responsable du contenu et, le cas échéant, fournit une URL pour mettre à jour les composants révoqués et déterminer les composants qui ont été révoqués.</span><span class="sxs-lookup"><span data-stu-id="4e873-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="4e873-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="4e873-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="4e873-141">Étend **ISCPSecureQuery2** en fournissant un ensemble de nouvelles méthodes pour récupérer les droits et prendre une décision sur un canal clair.</span><span class="sxs-lookup"><span data-stu-id="4e873-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="4e873-142">**ISCPSession**</span><span class="sxs-lookup"><span data-stu-id="4e873-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="4e873-143">Fournit une gestion efficace de l’État commun pour plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="4e873-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




