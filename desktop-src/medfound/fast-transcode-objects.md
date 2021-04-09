---
description: Cette rubrique explique comment utiliser l’API de transcodage pour encoder un fichier multimédia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Utilisation de l’API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111771"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="63a78-103">Utilisation de l’API de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-103">Using the Transcode API</span></span>

<span data-ttu-id="63a78-104">Cette rubrique explique comment utiliser l’API de transcodage pour encoder un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="63a78-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="63a78-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="63a78-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="63a78-106">Création d’une source de média</span><span class="sxs-lookup"><span data-stu-id="63a78-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="63a78-107">Création d’un profil de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="63a78-108">Attributs audio</span><span class="sxs-lookup"><span data-stu-id="63a78-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="63a78-109">Attributs vidéo</span><span class="sxs-lookup"><span data-stu-id="63a78-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="63a78-110">Attributs de conteneur</span><span class="sxs-lookup"><span data-stu-id="63a78-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="63a78-111">Création d’une topologie de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="63a78-112">Exécution de la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="63a78-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="63a78-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63a78-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="63a78-114">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="63a78-114">Overview</span></span>

<span data-ttu-id="63a78-115">Avant d’utiliser l’API de transcodage, l’application doit disposer des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="63a78-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="63a78-116">Le chemin d’accès ou l’URL d’un fichier multimédia existant qui sera à nouveau codé.</span><span class="sxs-lookup"><span data-stu-id="63a78-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="63a78-117">Nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="63a78-117">The name of the output file.</span></span>
-   <span data-ttu-id="63a78-118">Type de conteneur pour le fichier de sortie, tel que MP4 ou le format de streaming avancé (ASF).</span><span class="sxs-lookup"><span data-stu-id="63a78-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="63a78-119">Le format d'encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-119">The encoding format.</span></span> <span data-ttu-id="63a78-120">Ces informations incluent les types de médias qui décrivent les flux audio et vidéo encodés.</span><span class="sxs-lookup"><span data-stu-id="63a78-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="63a78-121">Pour utiliser l’API de transcodage, une application effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="63a78-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="63a78-122">Créer une source de média pour lire le fichier source.</span><span class="sxs-lookup"><span data-stu-id="63a78-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="63a78-123">Créez un profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-123">Create a transcode profile.</span></span> <span data-ttu-id="63a78-124">Ajoutez des attributs qui décrivent le flux audio, le flux vidéo et le conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="63a78-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="63a78-125">Utilisez le profil de transcodage pour créer une topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="63a78-126">(Pour plus d’informations sur les topologies, consultez [à propos des topologies](about-topologies.md).)</span><span class="sxs-lookup"><span data-stu-id="63a78-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="63a78-127">Définissez la topologie sur la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="63a78-128">Démarrez la session multimédia et attendez l’événement [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="63a78-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="63a78-129">Le reste de cette rubrique décrit ces étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="63a78-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="63a78-130">Création d’une source de média</span><span class="sxs-lookup"><span data-stu-id="63a78-130">Creating a Media Source</span></span>

<span data-ttu-id="63a78-131">Une source de média est un objet qui lit et analyse le fichier source.</span><span class="sxs-lookup"><span data-stu-id="63a78-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="63a78-132">Pour créer une source de média, utilisez le programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="63a78-133">Vous pouvez trouver un exemple de code dans la rubrique [à l’aide du programme de résolution source](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="63a78-134">Création d’un profil de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="63a78-135">Un *profil de transcodage* décrit le format et les paramètres utilisés pour encoder le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="63a78-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="63a78-136">Le profil de transcodage contient trois ensembles d’attributs :</span><span class="sxs-lookup"><span data-stu-id="63a78-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="63a78-137">Attributs audio : décrivent le format audio cible et les paramètres de l’encodeur audio.</span><span class="sxs-lookup"><span data-stu-id="63a78-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="63a78-138">Attributs vidéo : décrivent le format vidéo cible et les paramètres de l’encodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="63a78-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="63a78-139">Attributs de conteneur : définissez le type de conteneur de fichiers, ainsi que certains paramètres globaux d’encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="63a78-140">Pour créer un profil de transcodage, appelez la fonction [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="63a78-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="63a78-141">Cette fonction retourne un pointeur vers l’interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="63a78-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="63a78-142">L’objet de profil initial est vide ; il ne contient aucun attribut.</span><span class="sxs-lookup"><span data-stu-id="63a78-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="63a78-143">L’étape suivante consiste à ajouter les attributs qui définissent le profil.</span><span class="sxs-lookup"><span data-stu-id="63a78-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="63a78-144">Attributs audio</span><span class="sxs-lookup"><span data-stu-id="63a78-144">Audio Attributes</span></span>

<span data-ttu-id="63a78-145">Pour ajouter des attributs pour le flux audio, appelez [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="63a78-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="63a78-146">Ces attributs spécifient la façon dont le flux audio est encodé.</span><span class="sxs-lookup"><span data-stu-id="63a78-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="63a78-147">Si le fichier de sortie ne contient pas de flux audio, omettez ces attributs.</span><span class="sxs-lookup"><span data-stu-id="63a78-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="63a78-148">Les attributs audio se répartissent en deux catégories :</span><span class="sxs-lookup"><span data-stu-id="63a78-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="63a78-149">Attributs qui spécifient le format du flux encodé</span><span class="sxs-lookup"><span data-stu-id="63a78-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="63a78-150">Attributs qui spécifient d’autres paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="63a78-151">Les attributs de format sont simplement des attributs de type média, comme décrit dans la section [types de média audio](audio-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="63a78-152">Le jeu d’attributs de format exact dépend de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="63a78-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="63a78-153">(Consultez [formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md).) Voici une liste d’attributs de format audio typiques :</span><span class="sxs-lookup"><span data-stu-id="63a78-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="63a78-154">Attribut de format</span><span class="sxs-lookup"><span data-stu-id="63a78-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="63a78-155">Description</span><span class="sxs-lookup"><span data-stu-id="63a78-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="63a78-156">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="63a78-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="63a78-157">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="63a78-157">The subtype.</span></span> <span data-ttu-id="63a78-158">Consultez [GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="63a78-159">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="63a78-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="63a78-160">Nombre de canaux audio.</span><span class="sxs-lookup"><span data-stu-id="63a78-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="63a78-161">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="63a78-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="63a78-162">Nombre d’échantillons audio par seconde.</span><span class="sxs-lookup"><span data-stu-id="63a78-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="63a78-163">\_alignement de \_ \_ bloc audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="63a78-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="63a78-164">Alignement du bloc.</span><span class="sxs-lookup"><span data-stu-id="63a78-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="63a78-165">\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="63a78-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="63a78-166">Nombre moyen d’octets par seconde (vitesse de transmission encodée).</span><span class="sxs-lookup"><span data-stu-id="63a78-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="63a78-167">Les paramètres d’encodage suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="63a78-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="63a78-168">Paramètre d’encodage</span><span class="sxs-lookup"><span data-stu-id="63a78-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="63a78-169">Description</span><span class="sxs-lookup"><span data-stu-id="63a78-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="63a78-170">\_ \_ \_ encodeur d’insertion ne de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="63a78-171">Empêche l’API de transcodage d’insérer un encodeur pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="63a78-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="63a78-172">\_ENCODINGPROFILE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="63a78-173">Spécifie le modèle de conformité de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63a78-173">Specifies the device conformance template.</span></span> <span data-ttu-id="63a78-174">(S’applique uniquement aux fichiers ASF.)</span><span class="sxs-lookup"><span data-stu-id="63a78-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="63a78-175">\_QUALITYVSSPEED de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="63a78-176">Spécifie le compromis entre la qualité et la vitesse du codage.</span><span class="sxs-lookup"><span data-stu-id="63a78-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="63a78-177">Vous devez définir les attributs de format.</span><span class="sxs-lookup"><span data-stu-id="63a78-177">You must set the format attributes.</span></span> <span data-ttu-id="63a78-178">Les paramètres d’encodage sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="63a78-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="63a78-179">Une façon de trouver un format compatible avec l’encodeur consiste à appeler la fonction [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="63a78-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="63a78-180">L’encodeur souhaité est spécifié par le sous-type.</span><span class="sxs-lookup"><span data-stu-id="63a78-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="63a78-181">La fonction retourne une collection de types de médias pour cet encodeur.</span><span class="sxs-lookup"><span data-stu-id="63a78-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="63a78-182">Vous pouvez sélectionner un type dans la liste et copier les attributs dans le profil.</span><span class="sxs-lookup"><span data-stu-id="63a78-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="63a78-183">Pour obtenir un exemple de code qui utilise cette approche, consultez [Didacticiel : encodage d’un fichier WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="63a78-184">Attributs vidéo</span><span class="sxs-lookup"><span data-stu-id="63a78-184">Video Attributes</span></span>

<span data-ttu-id="63a78-185">Pour ajouter des attributs pour le flux vidéo, appelez [**IMFTranscodeProfile :: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="63a78-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="63a78-186">Ces attributs spécifient la façon dont le flux vidéo est encodé.</span><span class="sxs-lookup"><span data-stu-id="63a78-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="63a78-187">Si le fichier de sortie ne contient pas de flux vidéo, omettez ces attributs.</span><span class="sxs-lookup"><span data-stu-id="63a78-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="63a78-188">Comme avec les attributs audio, les attributs de la vidéo se répartissent en deux catégories :</span><span class="sxs-lookup"><span data-stu-id="63a78-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="63a78-189">Attributs qui spécifient le format du flux encodé</span><span class="sxs-lookup"><span data-stu-id="63a78-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="63a78-190">Attributs qui spécifient d’autres paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="63a78-191">Les attributs de format sont des attributs de type média, comme décrit dans la section [types de média vidéo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="63a78-192">Voici une liste d’attributs de format vidéo classiques :</span><span class="sxs-lookup"><span data-stu-id="63a78-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="63a78-193">Attribut de format</span><span class="sxs-lookup"><span data-stu-id="63a78-193">Format Attribute</span></span>                                                       | <span data-ttu-id="63a78-194">Description</span><span class="sxs-lookup"><span data-stu-id="63a78-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="63a78-195">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="63a78-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="63a78-196">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="63a78-196">The subtype.</span></span> <span data-ttu-id="63a78-197">Consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="63a78-198">\_fréquence d' \_ images MF MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="63a78-199">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="63a78-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="63a78-200">\_taille de \_ trame MF MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="63a78-201">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="63a78-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="63a78-202">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="63a78-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="63a78-203">Vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="63a78-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="63a78-204">\_ \_ \_ rapport hauteur/largeur des pixels \_ MF</span><span class="sxs-lookup"><span data-stu-id="63a78-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="63a78-205">Proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="63a78-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="63a78-206">Les paramètres d’encodage suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="63a78-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="63a78-207">Paramètre d’encodage</span><span class="sxs-lookup"><span data-stu-id="63a78-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="63a78-208">Description</span><span class="sxs-lookup"><span data-stu-id="63a78-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="63a78-209">\_ \_ \_ encodeur d’insertion ne de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="63a78-210">Empêche l’API de transcodage d’insérer un encodeur pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="63a78-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="63a78-211">\_ENCODINGPROFILE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="63a78-212">Spécifie le modèle de conformité de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63a78-212">Specifies the device conformance template.</span></span> <span data-ttu-id="63a78-213">(S’applique uniquement aux fichiers ASF.)</span><span class="sxs-lookup"><span data-stu-id="63a78-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="63a78-214">\_QUALITYVSSPEED de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="63a78-215">Spécifie le compromis entre la qualité et la vitesse du codage.</span><span class="sxs-lookup"><span data-stu-id="63a78-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="63a78-216">Vous devez définir les attributs de format.</span><span class="sxs-lookup"><span data-stu-id="63a78-216">You must set the format attributes.</span></span> <span data-ttu-id="63a78-217">Les paramètres d’encodage sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="63a78-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="63a78-218">Attributs de conteneur</span><span class="sxs-lookup"><span data-stu-id="63a78-218">Container Attributes</span></span>

<span data-ttu-id="63a78-219">Les attributs de conteneur définissent les caractéristiques de niveau fichier du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="63a78-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="63a78-220">Pour définir des attributs de conteneur, appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="63a78-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="63a78-221">Les attributs suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="63a78-221">The following attributes are defined.</span></span>



| <span data-ttu-id="63a78-222">Attribut</span><span class="sxs-lookup"><span data-stu-id="63a78-222">Attribute</span></span>                                                                          | <span data-ttu-id="63a78-223">Description</span><span class="sxs-lookup"><span data-stu-id="63a78-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63a78-224">\_profil d’ajustement de transcodage MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="63a78-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="63a78-225">Définit les paramètres de flux à utiliser pour la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="63a78-226">Vous pouvez définir les indicateurs pour utiliser les paramètres de la source d’entrée ou utiliser des attributs de flux personnalisés.</span><span class="sxs-lookup"><span data-stu-id="63a78-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="63a78-227">\_CONTAINERTYPE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="63a78-228">Spécifie le format de fichier du fichier de sortie, tel que MP4 ou ASF.</span><span class="sxs-lookup"><span data-stu-id="63a78-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="63a78-229">Sur la base de cette valeur, le récepteur multimédia approprié est ajouté à la topologie.</span><span class="sxs-lookup"><span data-stu-id="63a78-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="63a78-230">\_transfert de \_ \_ métadonnées d’omission de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="63a78-231">Spécifie si les métadonnées de la source sont copiées dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="63a78-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="63a78-232">\_TOPOLOGYMODE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="63a78-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="63a78-233">Spécifie si les codecs basés sur le matériel peuvent être utilisés lors du transcodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="63a78-234">\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_</span><span class="sxs-lookup"><span data-stu-id="63a78-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="63a78-235">Déverrouille un codec qui a des restrictions de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="63a78-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="63a78-236">Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="63a78-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="63a78-237">L' [attribut \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) est requis.</span><span class="sxs-lookup"><span data-stu-id="63a78-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="63a78-238">Les autres attributs de conteneur sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="63a78-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="63a78-239">Création d’une topologie de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="63a78-240">La topologie de transcodage est une topologie partielle qui contient la source du média, les codecs appropriés et le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="63a78-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="63a78-241">Pour créer la topologie de transcodage, appelez la fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) .</span><span class="sxs-lookup"><span data-stu-id="63a78-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="63a78-242">Cette fonction accepte les paramètres suivants comme entrée :</span><span class="sxs-lookup"><span data-stu-id="63a78-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="63a78-243">Pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="63a78-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="63a78-244">Nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="63a78-244">The name of the output file.</span></span>
-   <span data-ttu-id="63a78-245">Pointeur vers l’interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) du profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="63a78-246">La fonction retourne un pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .</span><span class="sxs-lookup"><span data-stu-id="63a78-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="63a78-247">Exécution de la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="63a78-247">Running the Encoding Session</span></span>

<span data-ttu-id="63a78-248">Une fois la topologie créée, vous êtes prêt à encoder le fichier.</span><span class="sxs-lookup"><span data-stu-id="63a78-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="63a78-249">Vous pouvez ignorer le profil à ce stade.</span><span class="sxs-lookup"><span data-stu-id="63a78-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="63a78-250">Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="63a78-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="63a78-251">Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="63a78-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="63a78-252">Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="63a78-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="63a78-253">Attendez l’événement [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="63a78-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="63a78-254">Appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="63a78-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="63a78-255">Attendez l’événement [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="63a78-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="63a78-256">Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="63a78-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="63a78-257">Appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="63a78-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="63a78-258">La majeure partie du temps passé à l’encodage se produit entre les étapes 3 et 4.</span><span class="sxs-lookup"><span data-stu-id="63a78-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a78-259">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63a78-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a78-260">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="63a78-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="63a78-261">À propos de la session multimédia</span><span class="sxs-lookup"><span data-stu-id="63a78-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



