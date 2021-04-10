---
title: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series
description: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, lecteurs synchrones
- Kit de développement logiciel (SDK) Windows Media format, indexation basée sur des trames
- Windows Media Format SDK, codes temporels SMPTE
- Kit de développement logiciel (SDK) Windows Media format, filtres DirectShow
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalité d’écriture DRM
- Windows Media Format SDK, récepteurs de fichiers
- Windows Media Format SDK, DirectX Video Acceleration (DXVA)
- Windows Media Format SDK, audio multicanal
- Windows Media Format SDK, filigrane
- Windows Media Format SDK, prise en charge de plusieurs langues
- Windows Media Format SDK, modèles de conformité des appareils
- Windows Media Format SDK, énumérations de codec
- Windows Media Format SDK, exclusion mutuelle
- Windows Media Format SDK, débit binaire multiple (MBR)
- Windows Media Format SDK, transcodage avec la recompression intelligente
- Windows Media Format SDK, recompression intelligente
- Windows Media Format SDK, recompression
- Windows Media Format SDK, métadonnées
- Windows Media Format SDK, proportions de pixels dynamiques
- Windows Media Format SDK, flux vidéo entrelacés
- Windows Media Format SDK, encodage en deux passes
- Windows Media Format SDK, WMStub. lib
- lecteurs synchrones, à propos de
- indexation basée sur des frames
- Codes temporels SMPTE, à propos de
- Filtres DirectShow
- récepteurs de fichiers, améliorations
- audio multicanal, à propos de
- filigrane, à propos de
- codecs, énumérations
- exclusion mutuelle, à propos de
- gestion des droits numériques (DRM), capacité d’écriture
- DRM (gestion des droits numériques), capacité d’écriture
- DirectX Video Acceleration (DXVA), à propos de
- DXVA (DirectX Video Acceleration), à propos de
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- débit binaire multiple (MBR), à propos de
- MBR (vitesses de transmission multiples), à propos de
- transcodage avec recompression intelligente
- recompression intelligente
- recompression
- métadonnées, Windows Media Format SDK
- proportions de pixels dynamiques
- flux vidéo entrelacés
- encodage en deux passes, à propos de
- 2-encodage Pass, à propos de
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196835"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="159d5-153">Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series</span><span class="sxs-lookup"><span data-stu-id="159d5-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="159d5-154">Le kit de développement logiciel (SDK) Windows Media Format 9 a introduit de nombreuses améliorations et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="159d5-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="159d5-155">Cette section fournit une vue d’ensemble de ces fonctionnalités pour les utilisateurs qui migrent à partir d’une version antérieure du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="159d5-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="159d5-156">Lecture synchrone</span><span class="sxs-lookup"><span data-stu-id="159d5-156">Synchronous Reading</span></span>

<span data-ttu-id="159d5-157">Vous pouvez lire des fichiers ASF avec des appels synchrones.</span><span class="sxs-lookup"><span data-stu-id="159d5-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="159d5-158">Lors de la lecture d’un fichier de façon synchrone, vous pouvez modifier les paramètres du lecteur pendant sa lecture.</span><span class="sxs-lookup"><span data-stu-id="159d5-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="159d5-159">Les opérations de lecture synchrones du kit de développement logiciel (SDK) ne prennent pas en charge la lecture des fichiers sur Internet, mais vous pouvez utiliser l’interface COM standard, **IStream**, pour lire à partir de sources personnalisées.</span><span class="sxs-lookup"><span data-stu-id="159d5-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="159d5-160">Indexation basée sur des frames</span><span class="sxs-lookup"><span data-stu-id="159d5-160">Frame-based Indexing</span></span>

<span data-ttu-id="159d5-161">Vous pouvez indexer des fichiers ASF basés sur des images vidéo.</span><span class="sxs-lookup"><span data-stu-id="159d5-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="159d5-162">Le lecteur et le lecteur synchrone peuvent rechercher un frame d’un flux vidéo et synchroniser les autres flux avec ce frame.</span><span class="sxs-lookup"><span data-stu-id="159d5-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="159d5-163">Indexation et recherche avec le code temporel SMPTE</span><span class="sxs-lookup"><span data-stu-id="159d5-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="159d5-164">Le kit de développement logiciel (SDK) Windows Media format vous permet de stocker des codes temporels SMPTE dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="159d5-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="159d5-165">Les fichiers peuvent être indexés par code temporel SMPTE, et le lecteur asynchrone et le lecteur synchrone peuvent rechercher des entrées d’index de code temporel SMPTE.</span><span class="sxs-lookup"><span data-stu-id="159d5-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="159d5-166">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="159d5-166">DirectShow Filters</span></span>

<span data-ttu-id="159d5-167">Le kit de développement logiciel (SDK) du format Windows Media comprend deux filtres de® Microsoft DirectShow qui permettent aux applications DirectShow de lire et d’écrire des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="159d5-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="159d5-168">DirectShow permet également aux applications de capturer des données à partir de périphériques audio vidéo et de décompresser des données à partir de différents formats avant de les encoder en tant que contenu Windows Media.</span><span class="sxs-lookup"><span data-stu-id="159d5-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="159d5-169">Profils améliorés</span><span class="sxs-lookup"><span data-stu-id="159d5-169">Enhanced Profiles</span></span>

<span data-ttu-id="159d5-170">Les profils peuvent contenir des informations de partage de bande passante et des informations de hiérarchisation de flux.</span><span class="sxs-lookup"><span data-stu-id="159d5-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="159d5-171">Le partage de bande passante vous permet de spécifier que deux flux ou plus, indépendamment de leurs vitesses de transmission individuelles, n’utiliseront jamais plus d’une quantité de bande passante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="159d5-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="159d5-172">Les données de partage de bande passante dans un profil sont purement informatifs. elle n’est pas appliquée par aucune logique dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="159d5-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="159d5-173">La hiérarchisation des flux vous permet de spécifier un ordre de priorité pour les flux dans un profil.</span><span class="sxs-lookup"><span data-stu-id="159d5-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="159d5-174">S’il n’y a pas suffisamment de bande passante lors de la lecture pour diffuser correctement le fichier, les flux de priorité les plus bas peuvent être ignorés afin d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="159d5-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="159d5-175">Fonctionnalité d’écriture DRM</span><span class="sxs-lookup"><span data-stu-id="159d5-175">DRM Writing Capability</span></span>

<span data-ttu-id="159d5-176">En plus de la prise en charge de la lecture DRM existante, le kit de développement logiciel (SDK) Windows Media Format 9 Series a ajouté la prise en charge de l’écriture de fichiers ASF avec la protection DRM version 1 ou DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="159d5-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="159d5-177">Cette nouvelle fonctionnalité permet des scénarios « DRM en direct », tels que la diffusion en continu à l’affichage de la diffusion d’événements sportifs ou de concerts en direct.</span><span class="sxs-lookup"><span data-stu-id="159d5-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="159d5-178">Récepteur de fichiers amélioré</span><span class="sxs-lookup"><span data-stu-id="159d5-178">Enhanced File Sink</span></span>

<span data-ttu-id="159d5-179">Plusieurs nouvelles fonctionnalités de récepteur de fichiers ont été ajoutées à la version 9 Series du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="159d5-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="159d5-180">Vous pouvez configurer le récepteur de fichiers pour désactiver l’indexation automatique des fichiers ASF nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="159d5-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="159d5-181">Vous avez également la possibilité de le configurer pour l’entrée et la sortie non mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="159d5-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="159d5-182">Accélération vidéo DirectX</span><span class="sxs-lookup"><span data-stu-id="159d5-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="159d5-183">DirectX Video Acceleration (DXVA) est une technologie qui permet la lecture d’une vidéo à débit élevé (qualité DVD ou meilleure) sur des machines moins puissantes avec des cartes graphiques compatibles DXVA.</span><span class="sxs-lookup"><span data-stu-id="159d5-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="159d5-184">Vous pouvez utiliser l’objet lecteur de ce kit de développement logiciel (SDK) pour activer l’accélération vidéo DirectX, si le matériel le prend en charge, lors de la lecture de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="159d5-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="159d5-185">Audio multicanal</span><span class="sxs-lookup"><span data-stu-id="159d5-185">Multichannel Audio</span></span>

<span data-ttu-id="159d5-186">Vous pouvez encoder et lire de l’audio multicanal.</span><span class="sxs-lookup"><span data-stu-id="159d5-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="159d5-187">Le codec Windows Media Audio 9 Professional prend en charge les formats avec 6 canaux et 8 canaux, ainsi que le stéréo haute définition.</span><span class="sxs-lookup"><span data-stu-id="159d5-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="159d5-188">Le filigranage</span><span class="sxs-lookup"><span data-stu-id="159d5-188">Watermarking</span></span>

<span data-ttu-id="159d5-189">Vous pouvez encoder des fichiers ASF avec des filigranes numériques pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="159d5-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="159d5-190">Tous les systèmes de filigrane sont différents dans leur approche, mais ils incorporent tous l’identification dans le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="159d5-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="159d5-191">Le filigrane est effectué à l’aide d’objets DMOs Media et® DirectX tiers spéciaux.</span><span class="sxs-lookup"><span data-stu-id="159d5-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="159d5-192">Prise en charge de plusieurs langues dans les fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="159d5-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="159d5-193">Vous pouvez prendre en charge plusieurs langues dans des fichiers ASF, à la fois dans les flux et dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="159d5-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="159d5-194">Par exemple, vous pouvez créer un fichier vidéo avec des flux audio dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="159d5-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="159d5-195">Lors de la lecture, l’utilisateur peut sélectionner la langue à utiliser, ou votre application peut interroger les informations système sur l’ordinateur en train de jouer et sélectionner une langue automatiquement.</span><span class="sxs-lookup"><span data-stu-id="159d5-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="159d5-196">Les attributs de métadonnées peuvent également être entrés plusieurs fois, avec les valeurs dans des langues différentes.</span><span class="sxs-lookup"><span data-stu-id="159d5-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="159d5-197">Modèles de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="159d5-197">Device Conformance Templates</span></span>

<span data-ttu-id="159d5-198">Pour faciliter le ciblage du contenu sur des appareils clients spécifiques, les codecs Windows Media prennent désormais en charge les modèles de conformité des appareils.</span><span class="sxs-lookup"><span data-stu-id="159d5-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="159d5-199">Chaque modèle contient une plage de paramètres définie et des fonctionnalités de codec qui doivent être utilisées pour les médias destinés à une catégorie particulière de plateformes.</span><span class="sxs-lookup"><span data-stu-id="159d5-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="159d5-200">Les profils système ne sont plus pris en charge avec les dernières versions des codecs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="159d5-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="159d5-201">Tous les profils doivent être personnalisés en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="159d5-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="159d5-202">Vous pouvez utiliser des modèles de conformité des appareils pour vous aider à concevoir vos profils.</span><span class="sxs-lookup"><span data-stu-id="159d5-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="159d5-203">Énumération de codec développée</span><span class="sxs-lookup"><span data-stu-id="159d5-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="159d5-204">L’objet gestionnaire de profils peut interroger les codecs vidéo et Windows Media Audio pour les formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="159d5-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="159d5-205">Vous pouvez définir des paramètres pour les formats récupérés.</span><span class="sxs-lookup"><span data-stu-id="159d5-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="159d5-206">Par exemple, vous pouvez récupérer tous les formats de taux de bits variables basés sur la qualité pris en charge par le codec Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="159d5-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="159d5-207">Exclusion mutuelle améliorée</span><span class="sxs-lookup"><span data-stu-id="159d5-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="159d5-208">Vous pouvez créer des enregistrements nommés contenant plusieurs flux dans un objet d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="159d5-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="159d5-209">Vous pouvez également nommer des objets d’exclusion mutuelle pour faciliter leur identification.</span><span class="sxs-lookup"><span data-stu-id="159d5-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="159d5-210">Cela vous permet de créer des couches d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="159d5-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="159d5-211">Par exemple, un fichier peut contenir des flux qui sont mutuellement exclusifs par vitesse de transmission et par langue.</span><span class="sxs-lookup"><span data-stu-id="159d5-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="159d5-212">L’exclusion mutuelle basée sur le langage implique des groupes de flux, chaque groupe constitué de flux dans la même langue mais mutuellement exclusifs par vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="159d5-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="159d5-213">Prise en charge de plusieurs vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="159d5-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="159d5-214">La prise en charge de l’exclusion mutuelle est incluse pour l’audio à débit binaire multiple (MBR) et pour la vidéo avec des flux de différentes tailles d’image.</span><span class="sxs-lookup"><span data-stu-id="159d5-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="159d5-215">Attributs pour les flux</span><span class="sxs-lookup"><span data-stu-id="159d5-215">Attributes for Streams</span></span>

<span data-ttu-id="159d5-216">Vous pouvez affecter des attributs à des flux individuels dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="159d5-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="159d5-217">Vous devez toujours utiliser des attributs de niveau fichier pour les fichiers MP3.</span><span class="sxs-lookup"><span data-stu-id="159d5-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="159d5-218">Cette fonctionnalité n’ajoute aucune méthode au kit de développement logiciel (SDK), mais les méthodes existantes acceptent désormais des numéros de flux autres que zéro.</span><span class="sxs-lookup"><span data-stu-id="159d5-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="159d5-219">Transcodage avec recompression intelligente</span><span class="sxs-lookup"><span data-stu-id="159d5-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="159d5-220">La recompression intelligente vous permet de transcoder des fichiers audio Windows Media d’un débit élevé vers une vitesse de transmission inférieure, avec une qualité supérieure à celle obtenue précédemment.</span><span class="sxs-lookup"><span data-stu-id="159d5-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="159d5-221">Prise en charge des métadonnées étendues</span><span class="sxs-lookup"><span data-stu-id="159d5-221">Expanded Metadata Support</span></span>

<span data-ttu-id="159d5-222">Le kit de développement logiciel (SDK) Windows Media Format fournit les nouvelles fonctionnalités de métadonnées suivantes :</span><span class="sxs-lookup"><span data-stu-id="159d5-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="159d5-223">Balises de métadonnées basées sur l’index, permettant l’activation de plusieurs balises portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="159d5-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="159d5-224">Possibilité de lire les attributs d’en-tête DRM sans fichier WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="159d5-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="159d5-225">Attributs avec plus de 64 kilo-octets de données associées.</span><span class="sxs-lookup"><span data-stu-id="159d5-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="159d5-226">Attributs dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="159d5-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="159d5-227">Des dizaines de nouveaux attributs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="159d5-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="159d5-228">Proportions de pixels dynamiques</span><span class="sxs-lookup"><span data-stu-id="159d5-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="159d5-229">Les flux vidéo composés de différents types de contenu peuvent être pris en compte en identifiant les proportions de pixels des exemples disparates dans le flux.</span><span class="sxs-lookup"><span data-stu-id="159d5-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="159d5-230">Cela permet à l’application de jouer de fournir une meilleure lecture de ce contenu.</span><span class="sxs-lookup"><span data-stu-id="159d5-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="159d5-231">Flux vidéo entrelacés</span><span class="sxs-lookup"><span data-stu-id="159d5-231">Interlaced Video Streams</span></span>

<span data-ttu-id="159d5-232">Les versions précédentes du kit de développement logiciel (SDK) du format Windows Media ont permis de coder le contenu [*entrelacé*](wmformat-glossary.md) dans un flux vidéo d’analyse progressive.</span><span class="sxs-lookup"><span data-stu-id="159d5-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="159d5-233">À compter du kit de développement logiciel (SDK) Windows Media Format 9 Series, vous pouvez encoder une vidéo entrelacée tout en conservant son format entrelacé.</span><span class="sxs-lookup"><span data-stu-id="159d5-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="159d5-234">Cela peut entraîner une amélioration de la lecture, en particulier sur les appareils entrelacés, tels que les groupes de télévision.</span><span class="sxs-lookup"><span data-stu-id="159d5-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="159d5-235">Encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="159d5-235">Two-Pass Encoding</span></span>

<span data-ttu-id="159d5-236">Les nouveaux codecs Windows Media activent l’encodage en deux passes.</span><span class="sxs-lookup"><span data-stu-id="159d5-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="159d5-237">Le contenu encodé en deux passes peut obtenir une sortie de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="159d5-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="159d5-238">Nouveau codec vocal</span><span class="sxs-lookup"><span data-stu-id="159d5-238">New Speech Codec</span></span>

<span data-ttu-id="159d5-239">Ce kit de développement logiciel (SDK) comprend le nouveau codec vocal Windows Media Audio 9 qui est optimisé pour l’encodage de la voix humaine tout en utilisant un faible taux de bits.</span><span class="sxs-lookup"><span data-stu-id="159d5-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="159d5-240">Ce codec offre également des performances supérieures pour le contenu mixte musical-Voice.</span><span class="sxs-lookup"><span data-stu-id="159d5-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="159d5-241">Durée de l’image vidéo accessible</span><span class="sxs-lookup"><span data-stu-id="159d5-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="159d5-242">Vous pouvez faire en sorte que l’objet writer de ce kit de développement logiciel (SDK) fournisse la durée des images vidéo au lecteur.</span><span class="sxs-lookup"><span data-stu-id="159d5-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="159d5-243">Streaming HTML</span><span class="sxs-lookup"><span data-stu-id="159d5-243">Streaming HTML</span></span>

<span data-ttu-id="159d5-244">Avec la version précédente de ce kit de développement logiciel (SDK), vous avez pu utiliser une commande de script pour signaler à votre application d’ouvrir une page Web.</span><span class="sxs-lookup"><span data-stu-id="159d5-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="159d5-245">À compter du kit de développement logiciel (SDK) Windows Media Format 9 Series, vous pouvez stocker les composants des pages Web dans vos fichiers ASF pour vous assurer qu’il n’y a aucun décalage dans les présentations.</span><span class="sxs-lookup"><span data-stu-id="159d5-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="159d5-246">WMStub. lib n’est plus nécessaire pour l’environnement de génération</span><span class="sxs-lookup"><span data-stu-id="159d5-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="159d5-247">Les paramètres d’environnement de build pour le kit de développement logiciel (SDK) du format Windows Media ont changé à partir du kit de développement logiciel Windows Media Format 9 Series.</span><span class="sxs-lookup"><span data-stu-id="159d5-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="159d5-248">Vous n’avez plus besoin d’inclure WMStub. lib pour les applications utilisant ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="159d5-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="159d5-249">Toutefois, les applications compatibles DRM doivent toujours obtenir et signer un contrat de licence distinct, et obtenir une bibliothèque statique unique auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="159d5-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="159d5-250">wmla@microsoft.comPour plus d’informations sur la bibliothèque DRM et le contrat de licence, contactez.</span><span class="sxs-lookup"><span data-stu-id="159d5-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="159d5-251">Pour plus d’informations sur la génération de projets avec ce kit de développement logiciel (SDK), consultez [fichiers de bibliothèque et paramètres du compilateur](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="159d5-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="159d5-252">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="159d5-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="159d5-253">**À propos du kit de développement logiciel (SDK) Windows Media format**</span><span class="sxs-lookup"><span data-stu-id="159d5-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




