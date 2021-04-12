---
title: À propos des versions de modèle objet
description: À propos des versions de modèle objet
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versions
- Windows Media Player Object Model (version)
- modèle objet, versions
- Contrôle ActiveX du lecteur Windows Media, versions pour le modèle objet
- Contrôle ActiveX, versions pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, versions pour le modèle objet
- Windows Media Player Mobile, versions pour le modèle objet
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381682"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="012d2-111">À propos des versions de modèle objet</span><span class="sxs-lookup"><span data-stu-id="012d2-111">About the Object Model Versions</span></span>

<span data-ttu-id="012d2-112">Le lecteur Windows Media 7,0 a introduit un nouveau modèle d’objet.</span><span class="sxs-lookup"><span data-stu-id="012d2-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="012d2-113">Ce modèle objet a été étendu avec le lecteur Windows Media 7,1, le lecteur Windows Media pour Windows XP, le lecteur Windows Media série 9, le lecteur Windows Media 10, le lecteur Windows Media 11 et le lecteur Windows Media 12.</span><span class="sxs-lookup"><span data-stu-id="012d2-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="012d2-114">Chaque rubrique de la référence de modèle objet comprend une section spécifications qui détaille la configuration minimale requise pour la propriété, la méthode ou l’événement individuel.</span><span class="sxs-lookup"><span data-stu-id="012d2-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="012d2-115">Les listes suivantes détaillent les nouveaux objets, méthodes, propriétés et événements qui ont été ajoutés pour chaque version depuis la version 7,0.</span><span class="sxs-lookup"><span data-stu-id="012d2-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="012d2-116">Ces listes incluent également de nouvelles interfaces, méthodes et événements C++.</span><span class="sxs-lookup"><span data-stu-id="012d2-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="012d2-117">Lorsqu’une interface nouvelle ou mise à jour est également exposée en tant qu’objet, seul l’objet est répertorié.</span><span class="sxs-lookup"><span data-stu-id="012d2-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="012d2-118">Pour localiser l’interface, reportez-vous à la [Référence du modèle objet pour C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="012d2-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="012d2-119">En règle générale, vous devez simplement ajouter le préfixe IWMP au nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="012d2-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="012d2-120">Si une nouvelle interface étend une interface existante, vous devrez peut-être Rechercher le numéro de version le plus récent.</span><span class="sxs-lookup"><span data-stu-id="012d2-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="012d2-121">Par exemple, le lecteur Windows Media série 9 a introduit de nouvelles propriétés et méthodes disponibles à partir de l’objet [**Settings**](settings-object.md) .</span><span class="sxs-lookup"><span data-stu-id="012d2-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="012d2-122">En C++, ces derniers sont disponibles via l’interface [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , qui étend [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span><span class="sxs-lookup"><span data-stu-id="012d2-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="012d2-123">Ajouté pour le lecteur Windows Media 7,1</span><span class="sxs-lookup"><span data-stu-id="012d2-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="012d2-124">**Propriété Player. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="012d2-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="012d2-125">Ajouté pour le lecteur Windows Media pour Windows XP</span><span class="sxs-lookup"><span data-stu-id="012d2-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="012d2-126">**Controls. Step, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="012d2-127">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="012d2-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="012d2-128">**Propriété Media. Error**</span><span class="sxs-lookup"><span data-stu-id="012d2-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="012d2-129">**Événement Player. DomainChange**</span><span class="sxs-lookup"><span data-stu-id="012d2-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="012d2-130">**Événement Player. MediaError**</span><span class="sxs-lookup"><span data-stu-id="012d2-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="012d2-131">**Événement Player. OpenPlaylistSwitch**</span><span class="sxs-lookup"><span data-stu-id="012d2-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="012d2-132">**Propriété Player. windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="012d2-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="012d2-133">Ajouté pour le lecteur Windows Media 9</span><span class="sxs-lookup"><span data-stu-id="012d2-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="012d2-134">**Méthode ClosedCaption. getSAMILangID**</span><span class="sxs-lookup"><span data-stu-id="012d2-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="012d2-135">**Méthode ClosedCaption. getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="012d2-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="012d2-136">**Méthode ClosedCaption. getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="012d2-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="012d2-137">**ClosedCaption. SAMILangCount, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="012d2-138">**ClosedCaption. SAMIStyleCount, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="012d2-139">**Controls. audioLanguageCount, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="012d2-140">**Controls. currentAudioLanguage, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="012d2-141">**Controls. currentAudioLanguageIndex, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="012d2-142">**Controls. currentPositionTimecode, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="012d2-143">**Controls. getAudioLanguageDescription, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="012d2-144">**Controls. getAudioLanguageID, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="012d2-145">**Controls. getLanguageName, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="012d2-146">**ErrorItem. condition, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="012d2-147">**External. appColorLight, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="012d2-148">**External. OnColorChange, événement**</span><span class="sxs-lookup"><span data-stu-id="012d2-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="012d2-149">**External. version, propriété**</span><span class="sxs-lookup"><span data-stu-id="012d2-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="012d2-150">**IWMPEvents ::P événement layerDockedStateChange**</span><span class="sxs-lookup"><span data-stu-id="012d2-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="012d2-151">**IWMPEvents ::P événement layerReconnect**</span><span class="sxs-lookup"><span data-stu-id="012d2-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="012d2-152">**Événement IWMPEvents :: SwitchedToControl**</span><span class="sxs-lookup"><span data-stu-id="012d2-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="012d2-153">**Événement IWMPEvents :: SwitchedToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="012d2-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="012d2-154">**Interface IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="012d2-155">**Interface IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="012d2-156">**Interface IWMPSkinManager**</span><span class="sxs-lookup"><span data-stu-id="012d2-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="012d2-157">**Méthode Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="012d2-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="012d2-158">**Méthode Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="012d2-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="012d2-159">**Objet MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="012d2-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="012d2-160">**Objet MetadataText**</span><span class="sxs-lookup"><span data-stu-id="012d2-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="012d2-161">**Événement Player. AudioLanguageChange**</span><span class="sxs-lookup"><span data-stu-id="012d2-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="012d2-162">**Propriété Player. isRemote**</span><span class="sxs-lookup"><span data-stu-id="012d2-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="012d2-163">**Événement Player. MediaCollectionAttributeStringChanged**</span><span class="sxs-lookup"><span data-stu-id="012d2-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="012d2-164">**Player. newMedia, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="012d2-165">**Player. newPlaylist, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="012d2-166">**Player. openPlayer, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="012d2-167">**Propriété Player. playerApplication**</span><span class="sxs-lookup"><span data-stu-id="012d2-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="012d2-168">**Événement Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="012d2-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="012d2-169">**Objet PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="012d2-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="012d2-170">**Propriété Settings. defaultAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="012d2-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="012d2-171">**Propriété Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="012d2-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="012d2-172">**Settings. requestMediaAccessRights, méthode**</span><span class="sxs-lookup"><span data-stu-id="012d2-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="012d2-173">Ajouté pour le lecteur Windows Media 10</span><span class="sxs-lookup"><span data-stu-id="012d2-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="012d2-174">**Interface IWMPGraphCreation**</span><span class="sxs-lookup"><span data-stu-id="012d2-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="012d2-175">**Interface IWMPPlayerServices2**</span><span class="sxs-lookup"><span data-stu-id="012d2-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="012d2-176">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="012d2-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="012d2-177">**Interface IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="012d2-178">**Énumération WMPDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="012d2-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="012d2-179">**Énumération WMPSyncState**</span><span class="sxs-lookup"><span data-stu-id="012d2-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="012d2-180">Ajouté pour le lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="012d2-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="012d2-181">**Interface IWMPCdromBurn**</span><span class="sxs-lookup"><span data-stu-id="012d2-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="012d2-182">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="012d2-183">**Interface IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="012d2-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="012d2-184">**Interface IWMPCdromRip (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="012d2-185">**Interface IWMPEvents3**</span><span class="sxs-lookup"><span data-stu-id="012d2-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="012d2-186">**Interface IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="012d2-187">**Interface IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="012d2-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="012d2-188">**Interface IWMPLibrary (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="012d2-189">**Interface IWMPLibraryServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="012d2-190">**Interface IWMPLibraryServices (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="012d2-191">**Interface IWMPLibrarySharingServices**</span><span class="sxs-lookup"><span data-stu-id="012d2-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="012d2-192">**Interface IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="012d2-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="012d2-193">**Interface IWMPMediaCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="012d2-194">**Interface IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="012d2-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="012d2-195">**Interface IWMPQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="012d2-196">**Interface IWMPRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="012d2-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="012d2-197">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="012d2-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="012d2-198">**Interface IWMPStringCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="012d2-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="012d2-199">**Interface IWMPSyncDevice2**</span><span class="sxs-lookup"><span data-stu-id="012d2-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="012d2-200">**Interface IWMPVideoRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="012d2-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="012d2-201">**Objet Query**</span><span class="sxs-lookup"><span data-stu-id="012d2-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="012d2-202">**Énumération WMPBurnFormat**</span><span class="sxs-lookup"><span data-stu-id="012d2-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="012d2-203">**Énumération WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="012d2-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="012d2-204">**Énumération WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="012d2-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="012d2-205">**Énumération WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="012d2-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="012d2-206">Ajouté pour le lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="012d2-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="012d2-207">**Interface IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="012d2-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="012d2-208">**Interface IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="012d2-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="012d2-209">**Interface IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="012d2-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="012d2-210">**Interface IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="012d2-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="012d2-211">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="012d2-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="012d2-212">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="012d2-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="012d2-213">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="012d2-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




