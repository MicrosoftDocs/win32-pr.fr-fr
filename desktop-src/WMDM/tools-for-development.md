---
title: Outils de développement
description: Outils de développement
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Gestionnaire de périphériques Windows Media, outils de développement
- Gestionnaire de périphériques, outils de développement
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- Gestionnaire de périphériques Windows Media, clés
- Gestionnaire de périphériques, clés
- Windows Media Gestionnaire de périphériques, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Windows Media Gestionnaire de périphériques, kit de développement logiciel (SDK)
- Gestionnaire de périphériques, kit de développement logiciel (SDK)
- SDK Windows Media Gestionnaire de périphériques
- SDK Gestionnaire de périphériques
- SDK du lecteur Windows Media
- Windows Media Format SDK
- SDK Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106513747"
---
# <a name="tools-for-development"></a><span data-ttu-id="8adbd-118">Outils de développement</span><span class="sxs-lookup"><span data-stu-id="8adbd-118">Tools for Development</span></span>

<span data-ttu-id="8adbd-119">Cette section décrit les différents certificats et clés, bibliothèques et kits de développement logiciel (SDK) que vous devrez programmer à l’aide du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="8adbd-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="8adbd-120">Certificats et clés</span><span class="sxs-lookup"><span data-stu-id="8adbd-120">Certificates and Keys</span></span>

<span data-ttu-id="8adbd-121">Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques est fourni avec une paire clé/certificat de test (dans le fichier Key. c) qui peut être utilisée par une application ou un fournisseur de services pour utiliser les méthodes Windows Media Gestionnaire de périphériques sur du contenu non protégé.</span><span class="sxs-lookup"><span data-stu-id="8adbd-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="8adbd-122">Cette paire clé/certificat permet à l’application ou au fournisseur de services d’utiliser la plupart des fonctionnalités de Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8adbd-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="8adbd-123">Toutefois, pour développer une application ou un fournisseur de services qui peut gérer le contenu DRM protégé, vous devez demander un ou plusieurs certificats (chacun avec une clé) à partir de la page de gestion des [licences Windows Media](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="8adbd-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="8adbd-124">Des certificats sont requis pour les applications ou objets suivants :</span><span class="sxs-lookup"><span data-stu-id="8adbd-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="8adbd-125">Les fournisseurs de services qui gèrent le contenu protégé par DRM requièrent un certificat de fournisseur de services Windows Media Gestionnaire de périphériques (et une clé)</span><span class="sxs-lookup"><span data-stu-id="8adbd-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="8adbd-126">Les applications qui transfèrent du contenu protégé par DRM requièrent un certificat de transfert Windows Media Gestionnaire de périphériques (et une clé)</span><span class="sxs-lookup"><span data-stu-id="8adbd-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="8adbd-127">Les applications qui lisent du contenu protégé par DRM requièrent un certificat DRM (et une clé).</span><span class="sxs-lookup"><span data-stu-id="8adbd-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="8adbd-128">Les composants de contrôle de licence requièrent un certificat de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8adbd-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="8adbd-129">Il est fourni par un service de contrôle de licence basé sur le kit de développement logiciel (SDK) Windows Media Rights Manager, qui peut être demandé sur la page Windows Media Licensing.</span><span class="sxs-lookup"><span data-stu-id="8adbd-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="8adbd-130">Bibliothèques et en-têtes</span><span class="sxs-lookup"><span data-stu-id="8adbd-130">Libraries and Headers</span></span>

<span data-ttu-id="8adbd-131">En plus des bibliothèques et des en-têtes mentionnés dans les [fichiers d’en-tête et de bibliothèque requis pour une application](required-library-and-header-files-for-an-application.md) ou les [bibliothèques et en-têtes requis pour un fournisseur de services](required-libraries-and-headers-for-a-service-provider.md), toute application ou plug-in précédemment lié à WMDRMSDK. lib pour appeler les fonctions du SDK Windows Media Format devrait maintenant être lié à WMDRMSDKStub. lib.</span><span class="sxs-lookup"><span data-stu-id="8adbd-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="8adbd-132">Ce fichier de bibliothèque est utilisé pour accéder aux fichiers protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="8adbd-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="8adbd-133">Vous pouvez également demander cette bibliothèque à partir de la page de gestion des licences Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8adbd-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="8adbd-134">Kits de développement logiciel associés</span><span class="sxs-lookup"><span data-stu-id="8adbd-134">Related SDKs</span></span>

<span data-ttu-id="8adbd-135">Les kits de développement logiciel (SDK) Microsoft suivants fournissent des éléments dont vous pouvez avoir besoin pour concevoir des solutions pour appareils multimédias portables.</span><span class="sxs-lookup"><span data-stu-id="8adbd-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="8adbd-136">SDK requis</span><span class="sxs-lookup"><span data-stu-id="8adbd-136">SDK Required</span></span>                     | <span data-ttu-id="8adbd-137">Requis pour...</span><span class="sxs-lookup"><span data-stu-id="8adbd-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adbd-138">SDK Windows Media Gestionnaire de périphériques</span><span class="sxs-lookup"><span data-stu-id="8adbd-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="8adbd-139">Applications de lecteur multimédia pour ordinateur de bureau qui communiquent avec des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8adbd-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="8adbd-140">Applications de bureau qui peuvent échanger des fichiers ou des informations avec des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="8adbd-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="8adbd-141">Objets COM de contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="8adbd-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="8adbd-142">SDK du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="8adbd-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="8adbd-143">Plug-ins du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="8adbd-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="8adbd-144">Objets COM de contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="8adbd-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="8adbd-145">Apparences du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="8adbd-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="8adbd-146">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="8adbd-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="8adbd-147">Lecteurs audio ou vidéo capables de créer ou de lire des fichiers (en particulier les fichiers ASF)</span><span class="sxs-lookup"><span data-stu-id="8adbd-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="8adbd-148">Applications d’édition audio ou vidéo</span><span class="sxs-lookup"><span data-stu-id="8adbd-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="8adbd-149">SDK Windows Media Rights Manager</span><span class="sxs-lookup"><span data-stu-id="8adbd-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="8adbd-150">Applications ou plug-ins qui mesurent le nombre de jeux sur le bureau ou l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8adbd-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="8adbd-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8adbd-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8adbd-152">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="8adbd-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





