---
title: Configuration requise pour que les lecteurs audio portables s’affichent dans l’Explorateur Windows
description: Configuration requise pour que les lecteurs audio portables s’affichent dans l’Explorateur Windows
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Gestionnaire de périphériques Windows Media, lecteurs audio portables
- Gestionnaire de périphériques, lecteurs audio portables
- Guide de programmation, lecteurs audio portables
- fournisseurs de services, lecteurs audio portables
- création de fournisseurs de services, de lecteurs audio portables
- lecteurs audio portables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106530782"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="bd56a-109">Configuration requise pour que les lecteurs audio portables s’affichent dans l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="bd56a-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="bd56a-110">L’extension de l’espace de noms du shell de lecteur audio portable offre aux utilisateurs Windows un moyen cohérent de gérer les périphériques audio gérés par Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="bd56a-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="bd56a-111">Si vous créez votre fournisseur de services et vos composants de pilote conformément aux instructions suivantes, votre appareil s’affiche dans l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="bd56a-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="bd56a-112">Les utilisateurs peuvent interagir avec le contenu de votre appareil de manière cohérente dans l’Explorateur Windows pour effectuer des opérations de base telles que copier, supprimer et renommer.</span><span class="sxs-lookup"><span data-stu-id="bd56a-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="bd56a-113">Les spécifications de l’interpréteur de commandes pour le fournisseur de services et les composants de pilote sont destinées à compléter les instructions générales de Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bd56a-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="bd56a-114">Fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="bd56a-114">Device Capabilities</span></span>

<span data-ttu-id="bd56a-115">Les fournisseurs de services Windows Media Gestionnaire de périphériques doivent être explicites dans leurs fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bd56a-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="bd56a-116">Si un appel n’est pas pris en charge, un code d’erreur doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="bd56a-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="bd56a-117">Les champs appropriés doivent être définis pour la présence ou l’absence de fonctionnalités au retour des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd56a-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="bd56a-118">**IMDSPStorageGlobals :: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd56a-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="bd56a-119">**IMDSPStorage :: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="bd56a-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="bd56a-120">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="bd56a-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="bd56a-121">Les fournisseurs de services doivent prendre en charge les fonctionnalités suivantes pour être compatibles avec l’interpréteur de commandes :</span><span class="sxs-lookup"><span data-stu-id="bd56a-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="bd56a-122">Copier sur l’appareil (avec prise en charge des rappels d’annulation et de progression)</span><span class="sxs-lookup"><span data-stu-id="bd56a-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="bd56a-123">Supprimer le fichier de l’appareil (avec prise en charge des rappels d’annulation et de progression)</span><span class="sxs-lookup"><span data-stu-id="bd56a-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="bd56a-124">Renommer le fichier sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="bd56a-124">Rename file on device</span></span>
-   <span data-ttu-id="bd56a-125">Rapport d’espace (espace total, espace libre, espace inutilisable)</span><span class="sxs-lookup"><span data-stu-id="bd56a-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="bd56a-126">Plug-and-Play (voir [activation de PNP pour les appareils](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="bd56a-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="bd56a-127">Format (de préférence avec prise en charge des rappels d’annulation et de progression)</span><span class="sxs-lookup"><span data-stu-id="bd56a-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="bd56a-128">Si les métadonnées sont prises en charge, les champs suivants doivent être pris en charge pour les fichiers individuels.</span><span class="sxs-lookup"><span data-stu-id="bd56a-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="bd56a-129">Si aucune donnée n’est disponible, le champ doit être initialisé en tant que chaîne vide :</span><span class="sxs-lookup"><span data-stu-id="bd56a-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="bd56a-130">Champ</span><span class="sxs-lookup"><span data-stu-id="bd56a-130">Field</span></span>        | <span data-ttu-id="bd56a-131">Constante (définie dans WMDM. idl)</span><span class="sxs-lookup"><span data-stu-id="bd56a-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="bd56a-132">Balise Metadata</span><span class="sxs-lookup"><span data-stu-id="bd56a-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="bd56a-133">Titre de la chanson</span><span class="sxs-lookup"><span data-stu-id="bd56a-133">Song Title</span></span>   | <span data-ttu-id="bd56a-134">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="bd56a-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="bd56a-135">WMDM/titre</span><span class="sxs-lookup"><span data-stu-id="bd56a-135">WMDM/Title</span></span>      |
| <span data-ttu-id="bd56a-136">Numéro de suivi</span><span class="sxs-lookup"><span data-stu-id="bd56a-136">Track Number</span></span> | <span data-ttu-id="bd56a-137">\_wszWMDMTrack g</span><span class="sxs-lookup"><span data-stu-id="bd56a-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="bd56a-138">WMDM/suivi</span><span class="sxs-lookup"><span data-stu-id="bd56a-138">WMDM/Track</span></span>      |
| <span data-ttu-id="bd56a-139">Peinture</span><span class="sxs-lookup"><span data-stu-id="bd56a-139">Artist</span></span>       | <span data-ttu-id="bd56a-140">\_wszWMDMAuthor g</span><span class="sxs-lookup"><span data-stu-id="bd56a-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="bd56a-141">WMDM/auteur</span><span class="sxs-lookup"><span data-stu-id="bd56a-141">WMDM/Author</span></span>     |
| <span data-ttu-id="bd56a-142">Album</span><span class="sxs-lookup"><span data-stu-id="bd56a-142">Album</span></span>        | <span data-ttu-id="bd56a-143">\_wszWMDMAlbumTitle g</span><span class="sxs-lookup"><span data-stu-id="bd56a-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="bd56a-144">WMDM/AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="bd56a-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="bd56a-145">Year</span><span class="sxs-lookup"><span data-stu-id="bd56a-145">Year</span></span>         | <span data-ttu-id="bd56a-146">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="bd56a-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="bd56a-147">WMDM/an</span><span class="sxs-lookup"><span data-stu-id="bd56a-147">WMDM/Year</span></span>       |
| <span data-ttu-id="bd56a-148">Genre</span><span class="sxs-lookup"><span data-stu-id="bd56a-148">Genre</span></span>        | <span data-ttu-id="bd56a-149">\_wszWMDMGenre g</span><span class="sxs-lookup"><span data-stu-id="bd56a-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="bd56a-150">WMDM/genre</span><span class="sxs-lookup"><span data-stu-id="bd56a-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="bd56a-151">Accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="bd56a-151">Concurrency</span></span>

<span data-ttu-id="bd56a-152">Les pilotes en mode noyau pour Windows Media Gestionnaire de périphériques doivent être robustes pour gérer l’accès simultané.</span><span class="sxs-lookup"><span data-stu-id="bd56a-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="bd56a-153">Par exemple, un utilisateur peut accéder simultanément à l’appareil à l’aide de l’interpréteur de commandes et du lecteur multimédia, ou simplement à l’aide de plusieurs fenêtres dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="bd56a-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="bd56a-154">Dans le cadre de la gestion de l’accès concurrentiel, les pilotes ne doivent pas supposer, juste parce que le fournisseur de services est chargé, que l’appareil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bd56a-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="bd56a-155">Au lieu de cela, ils doivent implémenter un mécanisme de verrouillage pour sérialiser l’accès à l’appareil en fonction des besoins des opérations individuelles.</span><span class="sxs-lookup"><span data-stu-id="bd56a-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="bd56a-156">Interface utilisateur du service</span><span class="sxs-lookup"><span data-stu-id="bd56a-156">UI</span></span>

<span data-ttu-id="bd56a-157">Les fournisseurs de services pour Windows Media Gestionnaire de périphériques ne doivent afficher aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd56a-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="bd56a-158">Toutes les erreurs doivent être retournées par les appels de méthode en tant que Gestionnaire de périphériques des codes d’erreur Windows Media spécifiques chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="bd56a-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="bd56a-159">Activation dans l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="bd56a-159">Enabling in the Shell</span></span>

<span data-ttu-id="bd56a-160">Si votre package remplit toutes les conditions requises de l’interpréteur de commandes, vous pouvez autoriser l’affichage de votre appareil dans l’interpréteur de commandes en définissant la valeur *ShowInShell* sur 1 sous les paramètres de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bd56a-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="bd56a-161">Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bd56a-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd56a-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd56a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd56a-163">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="bd56a-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




