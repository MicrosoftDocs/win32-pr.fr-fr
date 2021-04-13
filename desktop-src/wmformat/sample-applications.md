---
title: Exemples d’applications du SDK Windows Media format
description: Exemples d’applications du SDK Windows Media format
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, exemples d’applications
- gestion des droits numériques (DRM), exemples d’applications
- DRM (gestion des droits numériques), exemples d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464075"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="dae2b-106">Exemples d’applications du SDK Windows Media format</span><span class="sxs-lookup"><span data-stu-id="dae2b-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="dae2b-107">L’exemple de code fourni avec ce kit de développement logiciel (SDK) se présente sous la forme de projets pour Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="dae2b-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="dae2b-108">La plupart des exemples sont en C++, mais ManagedWMFSDKWrapper et ManagedMetadataEdit requièrent C#.</span><span class="sxs-lookup"><span data-stu-id="dae2b-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="dae2b-109">Ces exemples ne fonctionneront pas si le kit de développement logiciel (SDK) Windows Media format ou le SDK Windows Player n’a pas été installé.</span><span class="sxs-lookup"><span data-stu-id="dae2b-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="dae2b-110">Les informations d’utilisation de chaque exemple sont contenues dans un fichier de readme.txt dans chaque répertoire d’exemple.</span><span class="sxs-lookup"><span data-stu-id="dae2b-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dae2b-111">SAML</span><span class="sxs-lookup"><span data-stu-id="dae2b-111">Samle</span></span></th>
<th><span data-ttu-id="dae2b-112">Description</span><span class="sxs-lookup"><span data-stu-id="dae2b-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dae2b-113">AudioPlayer</span><span class="sxs-lookup"><span data-stu-id="dae2b-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="dae2b-114">Lit les fichiers Windows Media, y compris les fichiers protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="dae2b-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="dae2b-115">Elle est contrôlée par le biais d’une interface graphique utilisateur, et les commandes incluent Play, pause, Seek et Stop.</span><span class="sxs-lookup"><span data-stu-id="dae2b-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="dae2b-116">Il peut lire des fichiers locaux ou des fichiers lus à partir d’Internet (y compris ceux de la sortie sur Internet à l’aide de l’exemple WMVNetWrite).</span><span class="sxs-lookup"><span data-stu-id="dae2b-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dae2b-117">Les parties DRM de cet exemple ne sont pas prises en charge sur les versions x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="dae2b-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-118">DRMHeader</span><span class="sxs-lookup"><span data-stu-id="dae2b-118">DRMHeader</span></span></td>
<td><span data-ttu-id="dae2b-119">DRMHeader est une application console qui utilise l’interface <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> de l’éditeur de métadonnées pour lire les attributs DRM des fichiers sans les lier à la bibliothèque statique DRM.</span><span class="sxs-lookup"><span data-stu-id="dae2b-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dae2b-120">Cet exemple n’est pas pris en charge sur les versions x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="dae2b-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-121">DRMShow</span><span class="sxs-lookup"><span data-stu-id="dae2b-121">DRMShow</span></span></td>
<td><span data-ttu-id="dae2b-122">DRMShow est une application console qui montre comment lire les propriétés <a href="wmformat-glossary.md"><em>DRM</em></a> d’un fichier Windows Media à l’aide de la méthode <strong>IWMDRMReader :: GetDRMProperty</strong> . Cet exemple illustre l’utilisation de la méthode <strong>IWMDRMReader :: GetDRMProperty</strong> et des propriétés qui peuvent être récupérées à partir du lecteur DRM.</span><span class="sxs-lookup"><span data-stu-id="dae2b-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="dae2b-123">Il ne montre pas comment acquérir une licence pour du contenu protégé par DRM.</span><span class="sxs-lookup"><span data-stu-id="dae2b-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="dae2b-124">Cet exemple requiert la génération de la bibliothèque de stubs DRM WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="dae2b-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dae2b-125">Cet exemple n’est pas pris en charge sur les versions x64 de Windows.</span><span class="sxs-lookup"><span data-stu-id="dae2b-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="dae2b-126">Lorsque vous acquérez WMStubDRM. lib auprès de Microsoft, la bibliothèque se voit attribuer un niveau de sécurité d’application.</span><span class="sxs-lookup"><span data-stu-id="dae2b-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="dae2b-127">Si le niveau de sécurité de la bibliothèque que vous recevez n’est pas suffisant pour lire un fichier protégé, cet exemple affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="dae2b-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-128">DirectShowInterop/DSCopy</span><span class="sxs-lookup"><span data-stu-id="dae2b-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="dae2b-129">Transcode un ou plusieurs fichiers en fichier ASF à l’aide du filtre de l’enregistreur ASF DirectShow DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dae2b-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="dae2b-130">Le fichier d’entrée peut être n’importe quel format compressé ou non compressé pris en charge par DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dae2b-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-131">DirectShowInterop/DSPlay</span><span class="sxs-lookup"><span data-stu-id="dae2b-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="dae2b-132">Cet exemple est un lecteur de fichiers multimédias audio/vidéo interactif avec prise en charge de <a href="wmformat-glossary.md"><em>DRM</em></a> .</span><span class="sxs-lookup"><span data-stu-id="dae2b-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="dae2b-133">Il utilise le filtre de lecteur ASF WM de DirectShow pour lire les fichiers Windows Media (ASF, WMA, WMV) sans protection DRM et les fichiers qui utilisent DRM à un niveau de 100 ou plus.</span><span class="sxs-lookup"><span data-stu-id="dae2b-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="dae2b-134">Pour plus d’informations, consultez readme.txt dans le répertoire de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="dae2b-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-135">DirectShowInterop/DSSeekFm</span><span class="sxs-lookup"><span data-stu-id="dae2b-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="dae2b-136">Cet exemple montre comment utiliser le filtre de lecteur ASF DirectShow DirectShow pour lire du contenu ASF dans un graphique de filtre DirectShow et comment utiliser la prise en charge de la recherche de frame dans le kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dae2b-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-137">Géré/WMFSDKWrapper</span><span class="sxs-lookup"><span data-stu-id="dae2b-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="dae2b-138">Cet assembly géré sert de wrapper utilisé par les exemples de code managé pour accéder à certaines interfaces de métadonnées de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="dae2b-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-139">Géré/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="dae2b-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="dae2b-140">Cette application C# peut être utilisée pour afficher et modifier des métadonnées à partir de fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dae2b-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="dae2b-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="dae2b-142">Il s’agit d’une version C++ de l’application MetadataEdit managée.</span><span class="sxs-lookup"><span data-stu-id="dae2b-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-143">ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="dae2b-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="dae2b-144">Cet exemple d’application console montre comment lire des données à partir de <strong>IStream</strong> avec WMReader.</span><span class="sxs-lookup"><span data-stu-id="dae2b-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="dae2b-145">La source <strong>IStream</strong> a été implémentée pour utiliser un fichier au format Windows Media (WMA/WMV/ASF).</span><span class="sxs-lookup"><span data-stu-id="dae2b-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dae2b-146">Cet exemple n’indique pas comment traiter les exemples de supports provenant de WMReader.</span><span class="sxs-lookup"><span data-stu-id="dae2b-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="dae2b-147">Pour obtenir des exemples de traitement audio/vidéo ou d’autres types d’exemples de médias, reportez-vous à d’autres exemples, par exemple AudioPlayer, qui sont inclus dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dae2b-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-148">UncompAVIToWMV</span><span class="sxs-lookup"><span data-stu-id="dae2b-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="dae2b-149">Cet exemple d’application console montre le code nécessaire pour compresser un fichier AVI dans un fichier WMV.</span><span class="sxs-lookup"><span data-stu-id="dae2b-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="dae2b-150">Il montre comment fusionner des exemples pour des flux audio et vidéo à partir de plusieurs fichiers AVI et les fusionner dans des flux similaires ou créer un flux basé sur le profil de flux source.</span><span class="sxs-lookup"><span data-stu-id="dae2b-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="dae2b-151">Il montre également comment créer un flux arbitraire, effectuer un encodage multipasse, ajouter du code temporel SMPTE et appliquer la protection DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="dae2b-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-152">WMGenProfile/exe</span><span class="sxs-lookup"><span data-stu-id="dae2b-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="dae2b-153">Cet exemple a été mis à jour à partir de la version 7,1.</span><span class="sxs-lookup"><span data-stu-id="dae2b-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="dae2b-154">Il s’agit désormais d’une application de boîte de dialogue MFC.</span><span class="sxs-lookup"><span data-stu-id="dae2b-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="dae2b-155">L’exemple WMGenProfile illustre l’utilisation de la bibliothèque statique WMGenProfile.</span><span class="sxs-lookup"><span data-stu-id="dae2b-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="dae2b-156">Il sert également d’outil pour la création de profils.</span><span class="sxs-lookup"><span data-stu-id="dae2b-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="dae2b-157">Cet outil est destiné aux développeurs familiarisés avec le format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dae2b-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="dae2b-158">L’interface utilisateur n’a pas été testée pour l’expérience utilisateur et n’est pas censée être une recommandation sur la façon de présenter ces informations à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dae2b-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-159">WMGenProfile/lib</span><span class="sxs-lookup"><span data-stu-id="dae2b-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="dae2b-160">L’exemple de bibliothèque GenProfile illustre la création de profils.</span><span class="sxs-lookup"><span data-stu-id="dae2b-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="dae2b-161">Il montre comment créer des flux et des types de médias pour différents types de flux (audio, vidéo, script, image, transfert de fichiers et Web).</span><span class="sxs-lookup"><span data-stu-id="dae2b-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="dae2b-162">Il ne montre pas comment utiliser des profils système ou comment convertir des profils système en profils qui spécifient les codecs de série Windows Media Audio et Video 9.</span><span class="sxs-lookup"><span data-stu-id="dae2b-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-163">WMProp</span><span class="sxs-lookup"><span data-stu-id="dae2b-163">WMProp</span></span></td>
<td><span data-ttu-id="dae2b-164">Cette application console montre comment récupérer des attributs à l’aide de l’objet de l’éditeur de métadonnées et des informations de profil du lecteur.</span><span class="sxs-lookup"><span data-stu-id="dae2b-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-165">WMStats</span><span class="sxs-lookup"><span data-stu-id="dae2b-165">WMStats</span></span></td>
<td><span data-ttu-id="dae2b-166">Cette application console affiche les statistiques sur les lecteurs et les rédacteurs.</span><span class="sxs-lookup"><span data-stu-id="dae2b-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="dae2b-167">Plusieurs instances de WMStats peuvent également être utilisées simultanément sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dae2b-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="dae2b-168">Démarrez une instance en tant que serveur pour envoyer le flux au réseau, puis exécutez une deuxième instance en tant que client pour vérifier que le serveur est correctement diffusé.</span><span class="sxs-lookup"><span data-stu-id="dae2b-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-169">WMSyncReader</span><span class="sxs-lookup"><span data-stu-id="dae2b-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="dae2b-170">Cet exemple d’application console montre comment lire un fichier multimédia à l’aide de <strong>IWMSyncReader</strong> sans créer de thread supplémentaire ou à l’aide de rappels.</span><span class="sxs-lookup"><span data-stu-id="dae2b-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="dae2b-171">Les fonctionnalités suivantes sont implémentées : lecture des exemples compressés ou décompressés</span><span class="sxs-lookup"><span data-stu-id="dae2b-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="dae2b-172">Recherche basée sur le temps</span><span class="sxs-lookup"><span data-stu-id="dae2b-172">Time-based seeking</span></span><br/> <span data-ttu-id="dae2b-173">Recherche basée sur des frames</span><span class="sxs-lookup"><span data-stu-id="dae2b-173">Frame-based seeking</span></span><br/> <span data-ttu-id="dae2b-174">Source dérivée <strong>IStream</strong></span><span class="sxs-lookup"><span data-stu-id="dae2b-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-175">WMVAppend</span><span class="sxs-lookup"><span data-stu-id="dae2b-175">WMVAppend</span></span></td>
<td><span data-ttu-id="dae2b-176">Cette application console prend deux fichiers Windows Media pour l’entrée et tente de créer un fichier de sortie avec le contenu du premier suivi du deuxième.</span><span class="sxs-lookup"><span data-stu-id="dae2b-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="dae2b-177">L’exemple compare les profils des deux fichiers d’entrée pour s’assurer qu’ils sont suffisamment similaires pour être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="dae2b-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="dae2b-178">Si ce n’est pas le cas, un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="dae2b-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="dae2b-179">Par exemple, un message d’erreur se produit lorsqu’un fichier est audio uniquement et le second est un fichier vidéo audio ou lorsque deux fichiers audio ont des vitesses de transmission différentes. L’exemple accepte des sources à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="dae2b-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="dae2b-180">Toutefois, lors de la comparaison des profils des deux sources VBR, l’exemple ignore la différence de vitesse de transmission moyenne, car deux flux VBR auront des taux de bits moyens différents, même s’ils ont été créés à l’aide du même profil.</span><span class="sxs-lookup"><span data-stu-id="dae2b-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="dae2b-181">WMVAppend ne peut pas comparer le taux binaire de pointe des flux VBR basés sur un taux binaire non restreint, ou le niveau de qualité des flux VBR basés sur la qualité, car ces informations n’existent pas dans les fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="dae2b-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="dae2b-182">C’est la responsabilité de l’utilisateur de s’assurer que deux fichiers sources sont créés à l’aide du même profil.</span><span class="sxs-lookup"><span data-stu-id="dae2b-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="dae2b-183">Dans le cas contraire, vous pouvez créer un contenu non valide.</span><span class="sxs-lookup"><span data-stu-id="dae2b-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-184">WMVCopy</span><span class="sxs-lookup"><span data-stu-id="dae2b-184">WMVCopy</span></span></td>
<td><span data-ttu-id="dae2b-185">Cet exemple montre le code nécessaire pour copier un fichier WMV.</span><span class="sxs-lookup"><span data-stu-id="dae2b-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="dae2b-186">Il montre comment lire et écrire des exemples compressés, lire des attributs d’en-tête et des scripts, et modifier les attributs d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="dae2b-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dae2b-187">WMVNetWrite</span><span class="sxs-lookup"><span data-stu-id="dae2b-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="dae2b-188">Cette application console montre comment un fichier Windows Media est diffusé en continu sur Internet.</span><span class="sxs-lookup"><span data-stu-id="dae2b-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="dae2b-189">L’exemple requiert la spécification d’un port, puis le fichier peut être lu à l’aide d’un lecteur.</span><span class="sxs-lookup"><span data-stu-id="dae2b-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dae2b-190">WMVRecompress</span><span class="sxs-lookup"><span data-stu-id="dae2b-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="dae2b-191">Cette application console montre comment recompresser un fichier WMV.</span><span class="sxs-lookup"><span data-stu-id="dae2b-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="dae2b-192">Il illustre la lecture des exemples non compressés, l’écriture d’exemples non compressés et l’encodage à plusieurs passes, la sortie multicanaux et la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="dae2b-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="dae2b-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dae2b-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae2b-194">**À propos du kit de développement logiciel (SDK) Windows Media format**</span><span class="sxs-lookup"><span data-stu-id="dae2b-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="dae2b-195">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="dae2b-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





