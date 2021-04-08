---
title: Nouveautés de Windows Media Player 12
description: Cette rubrique répertorie les nouvelles fonctionnalités du lecteur Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, nouveautés
- Windows Media Player, nouvelles fonctionnalités
- Kit de développement logiciel (SDK), lecteur Windows Media 12
- SDK (kit de développement logiciel), lecteur Windows Media 12
- documentation, kit de développement logiciel (SDK) lecteur Windows Media 12
- nouveautés, lecteur Windows Media 12
- nouvelles fonctionnalités, lecteur Windows Media 12
- interfaces, nouvelles fonctionnalités dans le lecteur Windows Media 12
- attributs, nouvelles fonctionnalités dans le lecteur Windows Media 12
- métadonnées, nouvelles fonctionnalités dans le lecteur Windows Media 12
- énumérations, nouvelles fonctionnalités dans le lecteur Windows Media 12
- indicateurs, nouvelles fonctionnalités dans le lecteur Windows Media 12
- interfaces, déconseillées dans le lecteur Windows Media 12
- méthodes, déconseillées dans le lecteur Windows Media 11 et non dans 12
- versions de Windows Media Player, nouvelles fonctionnalités de la version 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101372"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="0e22d-118">Nouveautés de Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="0e22d-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="0e22d-119">Cette rubrique répertorie les nouvelles fonctionnalités du lecteur Windows Media 12.</span><span class="sxs-lookup"><span data-stu-id="0e22d-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="0e22d-120">Nouvelles interfaces</span><span class="sxs-lookup"><span data-stu-id="0e22d-120">New Interfaces</span></span>

-   [<span data-ttu-id="0e22d-121">**IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="0e22d-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="0e22d-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="0e22d-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="0e22d-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="0e22d-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="0e22d-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="0e22d-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="0e22d-125">Nouveaux attributs</span><span class="sxs-lookup"><span data-stu-id="0e22d-125">New Attributes</span></span>

<span data-ttu-id="0e22d-126">Les nouveaux attributs suivants pour les éléments multimédias sont disponibles par le biais des interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) et [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .</span><span class="sxs-lookup"><span data-stu-id="0e22d-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="0e22d-127">**AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="0e22d-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="0e22d-128">**AlternateSourceURL**</span><span class="sxs-lookup"><span data-stu-id="0e22d-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="0e22d-129">**DLNASourceURI**</span><span class="sxs-lookup"><span data-stu-id="0e22d-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="0e22d-130">**DLNAServerUDN**</span><span class="sxs-lookup"><span data-stu-id="0e22d-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="0e22d-131">**DTCPIPHost**</span><span class="sxs-lookup"><span data-stu-id="0e22d-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="0e22d-132">**DTCPIPPort**</span><span class="sxs-lookup"><span data-stu-id="0e22d-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="0e22d-133">**Id_bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="0e22d-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="0e22d-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="0e22d-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="0e22d-135">Nouvelles métadonnées de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0e22d-135">New Device Metadata</span></span>

<span data-ttu-id="0e22d-136">Les nouveaux éléments de métadonnées d’appareil suivants peuvent être récupérés en appelant [**IWMPSyncDevice :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="0e22d-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="0e22d-137">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="0e22d-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="0e22d-138">**SkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="0e22d-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="0e22d-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="0e22d-139">**SyncFilter**</span></span>

<span data-ttu-id="0e22d-140">Les nouveaux éléments de métadonnées d’appareil suivants peuvent être définis en appelant [**IWMPSyncDevice2 :: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span><span class="sxs-lookup"><span data-stu-id="0e22d-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="0e22d-141">**AutoSyncDefaultRules**</span><span class="sxs-lookup"><span data-stu-id="0e22d-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="0e22d-142">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="0e22d-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="0e22d-143">**IncludeSkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="0e22d-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="0e22d-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="0e22d-144">**SyncFilter**</span></span>
-   <span data-ttu-id="0e22d-145">**SyncOnConnect**</span><span class="sxs-lookup"><span data-stu-id="0e22d-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="0e22d-146">Nouveau membre de l’énumération</span><span class="sxs-lookup"><span data-stu-id="0e22d-146">New Enumeration Member</span></span>

<span data-ttu-id="0e22d-147">L’énumération [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) a le nouveau membre suivant.</span><span class="sxs-lookup"><span data-stu-id="0e22d-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="0e22d-148">**wmpssEstimating**</span><span class="sxs-lookup"><span data-stu-id="0e22d-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="0e22d-149">Nouvel indicateur</span><span class="sxs-lookup"><span data-stu-id="0e22d-149">New Flag</span></span>

<span data-ttu-id="0e22d-150">La méthode [**IWMPGraphCreation :: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) prend en charge le nouvel indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="0e22d-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="0e22d-151">**les \_ indicateurs WMPGC \_ utilisent un \_ \_ graphique personnalisé**</span><span class="sxs-lookup"><span data-stu-id="0e22d-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="0e22d-152">Interface dépréciée</span><span class="sxs-lookup"><span data-stu-id="0e22d-152">Deprecated Interface</span></span>

<span data-ttu-id="0e22d-153">L’interface suivante est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0e22d-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="0e22d-154">**IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="0e22d-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="0e22d-155">Méthodes qui ne sont plus dépréciées</span><span class="sxs-lookup"><span data-stu-id="0e22d-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="0e22d-156">Les méthodes suivantes ont été déconseillées dans le kit de développement logiciel (SDK) du lecteur Windows Media 11, mais ne sont plus dépréciées.</span><span class="sxs-lookup"><span data-stu-id="0e22d-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="0e22d-157">**IWMPGraphCreation::GraphCreationPreRender**</span><span class="sxs-lookup"><span data-stu-id="0e22d-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="0e22d-158">**IWMPGraphCreation::GraphCreationPostRender**</span><span class="sxs-lookup"><span data-stu-id="0e22d-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="0e22d-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e22d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e22d-160">À propos du kit de développement logiciel (SDK) Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="0e22d-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




