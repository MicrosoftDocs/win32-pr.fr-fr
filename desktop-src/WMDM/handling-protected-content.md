---
title: Gestion du contenu protégé
description: Gestion du contenu protégé
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- applications de bureau, certificats
- fournisseurs de services, certificats
- Guide de programmation, certificats
- certificates
- Gestionnaire de périphériques Windows Media, fournisseur de contenu sécurisé (SCP)
- Gestionnaire de périphériques, fournisseur de contenu sécurisé (SCP)
- applications de bureau, fournisseur de contenu sécurisé (SCP)
- fournisseurs de services, fournisseur de contenu sécurisé (SCP)
- Guide de programmation, fournisseur de contenu sécurisé (SCP)
- fournisseur de contenu sécurisé (SCP)
- SCP (Secure Content Provider)
- Gestionnaire de périphériques Windows Media, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- applications de bureau, contenu protégé par DRM
- fournisseurs de services, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379801"
---
# <a name="handling-protected-content"></a><span data-ttu-id="bfbba-122">Gestion du contenu protégé</span><span class="sxs-lookup"><span data-stu-id="bfbba-122">Handling Protected Content</span></span>

<span data-ttu-id="bfbba-123">Si vous créez une application ou un fournisseur de services qui consomme du contenu protégé par la gestion des droits numériques (DRM) Windows Media, vous devez disposer d’une paire clé/certificat émise par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bfbba-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="bfbba-124">Pour savoir où obtenir ce certificat, consultez [outils de développement](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="bfbba-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="bfbba-125">Si vous n’envisagez pas de gérer le contenu protégé, vous pouvez utiliser la clé factice et le certificat fournis avec ce kit de développement logiciel (SDK) dans un fichier nommé Key. c.</span><span class="sxs-lookup"><span data-stu-id="bfbba-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="bfbba-126">Pour tout fichier protégé par la technologie DRM, Windows Media Gestionnaire de périphériques nécessite la présence d’un fournisseur de contenu sécurisé (SCP) pour ce format de fichier.</span><span class="sxs-lookup"><span data-stu-id="bfbba-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="bfbba-127">Microsoft fournit un module SCP pour les fichiers WMA et WMV.</span><span class="sxs-lookup"><span data-stu-id="bfbba-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="bfbba-128">Si votre application ou fournisseur de services gère le contenu DRM protégé d’un autre format, vous devez fournir votre propre module SCP.</span><span class="sxs-lookup"><span data-stu-id="bfbba-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="bfbba-129">Un module SCP est un objet COM qui implémente toutes les [interfaces des fournisseurs de contenu sécurisés](interfaces-for-secure-content-providers.md).</span><span class="sxs-lookup"><span data-stu-id="bfbba-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="bfbba-130">Une application peut envoyer du contenu protégé par DRM à des appareils basés sur Windows Media DRM 10 pour les périphériques portables ou sur des DRM d’appareils mobiles (PDDRM).</span><span class="sxs-lookup"><span data-stu-id="bfbba-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="bfbba-131">Toutefois, vous pouvez uniquement créer un fournisseur de services pour les appareils basés sur PDDRM ; vous ne pouvez pas créer un fournisseur de services pour les appareils basés sur Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="bfbba-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="bfbba-132">Ces derniers appareils peuvent uniquement utiliser le fournisseur de services MTP fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bfbba-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="bfbba-133">Les appareils basés sur PDDRM peuvent uniquement prendre en charge les licences pour le contenu acheté.</span><span class="sxs-lookup"><span data-stu-id="bfbba-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="bfbba-134">Les licences qui ont des conditions d’expiration de délai sont uniquement prises en charge par les appareils basés sur Windows Media DRM 10 pour les appareils mobiles, qui ont des exigences particulières, telles que l’horloge sécurisée et l’individualisation.</span><span class="sxs-lookup"><span data-stu-id="bfbba-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="bfbba-135">Le kit de développement logiciel (SDK) Windows Media DRM 10 pour appareils mobiles fournit des détails sur la configuration requise des appareils pour prendre en charge la technologie version 10.</span><span class="sxs-lookup"><span data-stu-id="bfbba-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="bfbba-136">Avant d’envoyer du contenu DRM à l’appareil, une application doit vérifier plusieurs éléments :</span><span class="sxs-lookup"><span data-stu-id="bfbba-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="bfbba-137">Que l’appareil prend en charge la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="bfbba-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="bfbba-138">La version de la technologie DRM prise en charge (version 10 ou antérieure).</span><span class="sxs-lookup"><span data-stu-id="bfbba-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="bfbba-139">Si l’appareil est basé sur la version 10, tous ses composants sont à jour (par exemple, l’horloge sécurisée et toutes les exigences d’individualisation).</span><span class="sxs-lookup"><span data-stu-id="bfbba-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="bfbba-140">Tous les appels de méthode pour répondre à ces questions sont faits par le client et gérés par les Gestionnaire de périphériques Windows Media et le composant fournisseur de contenu sécurisé. le fournisseur de services ne gère aucun de ces appels.</span><span class="sxs-lookup"><span data-stu-id="bfbba-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="bfbba-141">Si l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles, il peut toujours être en mesure de consommer du contenu protégé (en fonction de la licence de contenu et de la conception de l’appareil), mais tout contenu qui lui est envoyé disposera d’une licence d’utilisation simplifiée avec des droits limités (par exemple, pas de délai d’expiration).</span><span class="sxs-lookup"><span data-stu-id="bfbba-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="bfbba-142">Pour obtenir des exemples montrant comment une application vérifie si un appareil peut gérer du contenu protégé et s’il doit mettre à jour ses composants DRM, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="bfbba-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="bfbba-143">Pour plus d’informations sur la création d’un fournisseur de services pouvant gérer du contenu protégé, consultez [gestion du contenu protégé dans le fournisseur de services](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bfbba-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="bfbba-144">Un grand nombre de méthodes de transfert de fichiers ou de droits Windows Media Gestionnaire de périphériques échouent (souvent avec une valeur de **HRESULT** mystérieuse) lors de la gestion des fichiers protégés par DRM avec un débogueur attaché.</span><span class="sxs-lookup"><span data-stu-id="bfbba-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="bfbba-145">Par conséquent, vous devez utiliser d’autres méthodes pour déboguer votre code, telles que la journalisation des sorties dans un Windows Form ou un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bfbba-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="bfbba-146">Pour plus d’informations sur les options de journalisation, consultez Activation de la [journalisation](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="bfbba-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="bfbba-147">Si vous exécutez un débogueur sur du contenu protégé, une méthode retourne l’un des codes d’erreur répertoriés dans les [codes d’erreur](error-codes.md)de la section DRM, ou éventuellement un code d’erreur inconnu.</span><span class="sxs-lookup"><span data-stu-id="bfbba-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="bfbba-148">Si vous recevez des valeurs de **HRESULT** mystérieuses lors de l’exécution d’un débogueur sur du contenu ou des méthodes protégés, la protection DRM peut en être la cause.</span><span class="sxs-lookup"><span data-stu-id="bfbba-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bfbba-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bfbba-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbba-150">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="bfbba-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




