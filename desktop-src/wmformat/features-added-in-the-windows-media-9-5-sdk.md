---
title: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5
description: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, interface pour le traitement propre à l’application
- Windows Media Format SDK, DirectX Video Acceleration (DXVA)
- Windows Media Format SDK, interface IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versions x64 de Windows
- Windows Media Format SDK, Windows Media Video codec d’image
- Windows Media Format SDK, codecs audio
- Windows Media Format SDK, DRM 10 pour les périphériques réseau
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, Advanced Profile codec
- Windows Media Format SDK, Sony/Philips Digital Interconnect format (S/PDIF)
- Windows Media Format SDK, formats à faible délai
- Windows Media Format SDK, mode de recherche approximatif
- Kit de développement logiciel (SDK) Windows Media format, gravure de playlist
- Windows Media Format SDK, prise en charge de plusieurs langues
- Windows Media Format SDK, Windows Media Gestionnaire de périphériques SDK
- Windows Media Format SDK, interfaces de codec
- codecs, image Windows Media Video
- gestion des droits numériques (DRM), protocole de transfert sécurisé des périphériques réseau
- DRM (gestion des droits numériques), protocole de transfert sécurisé des périphériques réseau
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- codecs, codec de profil avancé
- Sony/Philips Digital Interconnect format (S/PDIF), transfert ou transmission à l’aide de
- S/PDIF (format d’interconnexion numérique Sony/Philips), transfert ou transmission à l’aide de
- mode de recherche approximatif
- métadonnées, prise en charge de plusieurs langues
- SDK Windows Media Gestionnaire de périphériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101301"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="3bf9e-133">Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5</span><span class="sxs-lookup"><span data-stu-id="3bf9e-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="3bf9e-134">Le kit de développement logiciel (SDK) Windows Media Format 9,5 a introduit de nouvelles fonctionnalités pour améliorer la sécurité et la flexibilité du contenu.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="3bf9e-135">Les modifications suivantes ont été apportées au kit de développement logiciel depuis la version 9 Series.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="3bf9e-136">Nouvelle interface pour le traitement propre à l’application pendant l’accélération vidéo DirectX</span><span class="sxs-lookup"><span data-stu-id="3bf9e-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="3bf9e-137">Les applications de lecteur qui prennent en charge l’accélération vidéo DirectX peuvent désormais implémenter l’interface [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) pour effectuer un traitement propre à l’application pendant le décodage DirectX va.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="3bf9e-138">Le lecteur appelle la méthode de rappel [**IWMPLayerHook ::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) avant de passer des exemples vidéo compressés au processeur vidéo pour le décodage.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="3bf9e-139">Pour utiliser l’interface **IWMPlayerHook** et l’interface [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associée, vous devez avoir installé le numéro de mise à jour 888656 dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="3bf9e-140">Vous pouvez télécharger la mise à jour à partir du [site Web Microsoft](https://support.microsoft.com/?id=888656).</span><span class="sxs-lookup"><span data-stu-id="3bf9e-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="3bf9e-141">Version du kit de développement logiciel (SDK) Windows Media format pour les versions x64 de Windows</span><span class="sxs-lookup"><span data-stu-id="3bf9e-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="3bf9e-142">Une version x64 du kit de développement logiciel (SDK) du format Windows Media est disponible.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="3bf9e-143">Cette documentation s’applique à la fois aux versions 32 bits et à la version x64 du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="3bf9e-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="3bf9e-144">Toutefois, la gestion des droits numériques (DRM) n’est pas prise en charge dans le kit de développement logiciel (SDK) Windows Media format x64.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="3bf9e-145">Nouvelle version du codec d’image Windows Media Video</span><span class="sxs-lookup"><span data-stu-id="3bf9e-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="3bf9e-146">Le codec Windows Media Video 9 image v2 simplifie les exemples de calculs de géométrie pour le panoramique et le zoom.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="3bf9e-147">Le nouveau codec prend également en charge plusieurs transitions complexes entre les images.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="3bf9e-148">Nouvelle version des codecs de Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="3bf9e-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="3bf9e-149">Le kit de développement logiciel (SDK) Windows Media Format 9,5 comprend les codecs audio mis à jour suivants :</span><span class="sxs-lookup"><span data-stu-id="3bf9e-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="3bf9e-150">Windows Media Audio 9,1</span><span class="sxs-lookup"><span data-stu-id="3bf9e-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="3bf9e-151">Windows Media Audio 9,1 professionnel</span><span class="sxs-lookup"><span data-stu-id="3bf9e-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="3bf9e-152">Windows Media Audio 9,1 sans perte</span><span class="sxs-lookup"><span data-stu-id="3bf9e-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="3bf9e-153">Prise en charge du protocole Windows Media DRM 10 pour les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="3bf9e-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="3bf9e-154">Le kit de développement logiciel (SDK) Windows Media Format 9,5 prend en charge le nouveau Windows Media DRM 10 pour le protocole de transfert sécurisé de périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="3bf9e-155">Ce protocole peut être utilisé pour diffuser en continu du contenu chiffré sur un réseau local vers un périphérique de lecture, tel qu’un récepteur vidéo de type Set-Top.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="3bf9e-156">La plupart des procédures utilisées pour implémenter la prise en charge de Windows Media DRM 10 pour les périphériques réseau doivent être effectuées par l’application.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="3bf9e-157">Toutefois, vous pouvez utiliser les méthodes du kit de développement logiciel (SDK) Windows Media format pour fournir les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bf9e-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="3bf9e-158">Gérer une base de données d’appareils, y compris ceux qui sont activés pour Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="3bf9e-159">Validez les appareils pour vous assurer qu’ils sont « presque » suffisants pour le client sur le réseau pour la diffusion en continu sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="3bf9e-160">Convertit les fichiers protégés par DRM en Windows Media DRM 10 pour les flux de périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="3bf9e-161">Écrire des fichiers à l’aide de données précédemment chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="3bf9e-162">Prise en charge de nouvelles licences DRM</span><span class="sxs-lookup"><span data-stu-id="3bf9e-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="3bf9e-163">Les nouvelles licences créées à l’aide du kit de développement logiciel (SDK) Windows Media Rights Manager utilisent des niveaux de protection de sortie (OPLs) pour spécifier les droits et restrictions relatifs à la reproduction et à la copie de contenu.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="3bf9e-164">Le kit de développement logiciel (SDK) Windows Media format prend en charge la lecture des OPLs à partir d’une licence.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="3bf9e-165">Nouveau codec vidéo</span><span class="sxs-lookup"><span data-stu-id="3bf9e-165">New Video Codec</span></span>

<span data-ttu-id="3bf9e-166">Le codec de profil avancé Windows Media Video 9 s’appuie sur la haute qualité du codec Windows Media Video 9 tout en ajoutant la prise en charge de l’encodage entrelacé.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="3bf9e-167">Sortie S/PDIF</span><span class="sxs-lookup"><span data-stu-id="3bf9e-167">S/PDIF Output</span></span>

<span data-ttu-id="3bf9e-168">Le contenu encodé avec l’un des codecs Windows Media Audio Professional peut désormais être transféré ou transmis à l’aide du format S/PDIF de Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="3bf9e-169">Audio Low-Delay</span><span class="sxs-lookup"><span data-stu-id="3bf9e-169">Low-Delay Audio</span></span>

<span data-ttu-id="3bf9e-170">Les codecs Windows Media Audio 9,1 et Windows Media Audio 9,1 Professional prennent désormais en charge plusieurs formats à faible délai.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="3bf9e-171">Ces formats produisent des flux audio qui peuvent être démarrés plus rapidement, ce qui réduit la latence dans les scénarios de commutation de flux.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="3bf9e-172">La latence globale des diffusions en direct est également améliorée en utilisant des formats à faible retard.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="3bf9e-173">Mode de recherche approximatif</span><span class="sxs-lookup"><span data-stu-id="3bf9e-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="3bf9e-174">Vous pouvez maintenant rechercher une heure approximative dans un fichier ASF avec le lecteur.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="3bf9e-175">Ce mode améliore les performances lorsque vous effectuez une recherche imprécise, par exemple quand un utilisateur clique sur la barre de recherche dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="3bf9e-176">La recherche approximative retourne l’échantillon de support pour le Cleanpoint précédent au lieu de reconstruire l’exemple pour l’heure précise demandée.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="3bf9e-177">Gravure de playlist</span><span class="sxs-lookup"><span data-stu-id="3bf9e-177">Playlist Burning</span></span>

<span data-ttu-id="3bf9e-178">Windows Media DRM 10 prend en charge les droits de copie de fichiers audio dans un CD Red Book dans le cadre d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="3bf9e-179">Le kit de développement logiciel (SDK) Windows Media Format fournit des méthodes pour vérifier si les fichiers d’une sélection sont autorisés à être copiés.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="3bf9e-180">Prise en charge améliorée des Multiple-Language pour les métadonnées</span><span class="sxs-lookup"><span data-stu-id="3bf9e-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="3bf9e-181">Dans le kit de développement logiciel (SDK) Windows Media Format 9 Series, toutes les métadonnées ajoutées à un fichier ont été affectées à une liste de langues ayant reçu l’identificateur de langue de la langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="3bf9e-182">Cela provoquait des problèmes lorsque les serveurs de distribution de contenu de différents paramètres régionaux ajoutaient des métadonnées, car les utilisateurs des paramètres régionaux du serveur de distribution voient uniquement les attributs ajoutés pour leur langue.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="3bf9e-183">Le kit de développement logiciel (SDK) Windows Media Format 9,5 résout ce problème en ne créant pas de liste de langues tant qu’il n’y a pas d’attributs de deux langages présents dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="3bf9e-184">À ce stade, toutes les métadonnées sont associées aux paramètres régionaux de la deuxième langue, qui devient alors la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="3bf9e-185">De cette façon, un serveur de distribution de contenu peut conserver toutes les métadonnées d’origine d’un fichier, telles que le titre et l’auteur, tout en ajoutant des attributs pertinents pour leurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="3bf9e-186">Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques inclus dans l’installation</span><span class="sxs-lookup"><span data-stu-id="3bf9e-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="3bf9e-187">Le package d’installation du kit de développement logiciel (SDK) Windows Media Format 9,5 installe le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="3bf9e-188">La documentation du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques se trouve dans le dossier C : \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (votre dossier sera différent si vous n’installez pas le kit de développement logiciel (SDK) Windows Media format dans le dossier par défaut).</span><span class="sxs-lookup"><span data-stu-id="3bf9e-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="3bf9e-189">Documentation sur l’interface de codec</span><span class="sxs-lookup"><span data-stu-id="3bf9e-189">Codec Interface Documentation</span></span>

<span data-ttu-id="3bf9e-190">Cette documentation contient des informations sur l’utilisation du Windows Media Audio et des codecs vidéo en dehors du kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="3bf9e-191">Cette documentation a été publiée à l’origine dans le cadre d’un téléchargement à partir du Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="3bf9e-192">Les exemples d’applications qui illustrent l’utilisation directe du codec DMOs sont inclus dans l’installation du kit de développement logiciel (SDK) du format Windows Media avec les en-têtes.</span><span class="sxs-lookup"><span data-stu-id="3bf9e-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bf9e-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3bf9e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bf9e-194">**À propos du kit de développement logiciel (SDK) Windows Media format**</span><span class="sxs-lookup"><span data-stu-id="3bf9e-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




