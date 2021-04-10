---
title: Convention de travail de BITS du lecteur Windows Media
description: Le lecteur Windows Media peut automatiquement télécharger et ajouter des éléments multimédias numériques à la bibliothèque si vous utilisez Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player Online stores, Service de transfert intelligent en arrière-plan (BITS)
- magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- type 2 magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan (BITS)
- BITS (Service de transfert intelligent en arrière-plan)
- Windows Media Player Online stores, Convention de travail BITS
- magasins en ligne, Convention de travail BITS
- type 2 magasins en ligne, Convention de travail BITS
- Convention de travail BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199336"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="c9a49-112">Convention de travail de BITS du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="c9a49-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="c9a49-113">Le lecteur Windows Media peut automatiquement télécharger et ajouter des éléments multimédias numériques à la bibliothèque si vous utilisez [service de transfert intelligent en arrière-plan (bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span><span class="sxs-lookup"><span data-stu-id="c9a49-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="c9a49-114">Pour tirer parti de cette fonctionnalité, vous devez ajouter votre travail à la file d’attente de transfert BITS et appeler **méthode ibackgroundcopyjob :: SetDescription**, en fournissant une chaîne de description qui utilise le format correct.</span><span class="sxs-lookup"><span data-stu-id="c9a49-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="c9a49-115">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="c9a49-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c9a49-116">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c9a49-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c9a49-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9a49-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="c9a49-118">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9a49-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a49-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="c9a49-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-120">Valeur 32 bits générée de manière aléatoire, utilisée par le lecteur Windows Media pour identifier le service.</span><span class="sxs-lookup"><span data-stu-id="c9a49-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Moteur*</span><span class="sxs-lookup"><span data-stu-id="c9a49-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-122">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c9a49-122">The provider name.</span></span> <span data-ttu-id="c9a49-123">Cette valeur doit correspondre à un nom de clé de magasin en ligne valide.</span><span class="sxs-lookup"><span data-stu-id="c9a49-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span><span class="sxs-lookup"><span data-stu-id="c9a49-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-125">Nom de l’artiste principal de l’album.</span><span class="sxs-lookup"><span data-stu-id="c9a49-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span><span class="sxs-lookup"><span data-stu-id="c9a49-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-127">Titre de l’album.</span><span class="sxs-lookup"><span data-stu-id="c9a49-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span><span class="sxs-lookup"><span data-stu-id="c9a49-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-129">Numéro de piste du CD.</span><span class="sxs-lookup"><span data-stu-id="c9a49-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Bonhomme*</span><span class="sxs-lookup"><span data-stu-id="c9a49-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-131">Titre du contenu.</span><span class="sxs-lookup"><span data-stu-id="c9a49-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Macauley*</span><span class="sxs-lookup"><span data-stu-id="c9a49-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-133">Durée du contenu.</span><span class="sxs-lookup"><span data-stu-id="c9a49-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c9a49-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Audience*</span><span class="sxs-lookup"><span data-stu-id="c9a49-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="c9a49-135">Évaluation du contenu.</span><span class="sxs-lookup"><span data-stu-id="c9a49-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9a49-136">Notes</span><span class="sxs-lookup"><span data-stu-id="c9a49-136">Remarks</span></span>

<span data-ttu-id="c9a49-137">Lorsque le lecteur Windows Media 10 ou version ultérieure utilise le service BITS pour télécharger du contenu, il énumère les travaux dans la file d’attente de transfert et inspecte la chaîne de description de chaque travail.</span><span class="sxs-lookup"><span data-stu-id="c9a49-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="c9a49-138">Si la chaîne de description correspond à la Convention attendue, le lecteur Windows Media télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="c9a49-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="c9a49-139">Vous devez ajouter un seul fichier multimédia numérique à télécharger pour chaque travail BITS.</span><span class="sxs-lookup"><span data-stu-id="c9a49-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="c9a49-140">Une fois que vous avez démarré une tâche BITS à l’aide de cette Convention, vous devez laisser le lecteur Windows Media terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="c9a49-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="c9a49-141">Le lecteur Windows Media va également supprimer le travail de la file d’attente BITS, déplacer le fichier téléchargé vers l’emplacement où la musique extraite est enregistrée et ajouter le fichier téléchargé à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c9a49-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="c9a49-142">Le paramètre *ServiceId* doit contenir une valeur différente de zéro 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c9a49-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="c9a49-143">Nous vous recommandons d’utiliser la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour créer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c9a49-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="c9a49-144">Le nom de fichier que vous spécifiez à l’aide du paramètre *LocalName* de **méthode ibackgroundcopyjob :: AddFile** doit avoir une extension de nom de fichier. WMA,. wmv,. mp3 ou. ASF.</span><span class="sxs-lookup"><span data-stu-id="c9a49-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="c9a49-145">Les paramètres restants sont conçus pour contenir des valeurs de métadonnées relatives au contenu.</span><span class="sxs-lookup"><span data-stu-id="c9a49-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="c9a49-146">Vous pouvez récupérer ces valeurs à partir de votre page Web de boutique en ligne à l’aide de **DownloadItem. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="c9a49-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="c9a49-147">Vous pouvez récupérer la collection de téléchargements appropriée en appelant **downloadmanager. getDownloadCollection** et  en fournissant ServiceId *comme paramètre de* l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="c9a49-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="c9a49-148">Le lecteur Windows Media inspecte la file d’attente BITS régulièrement pendant que le lecteur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c9a49-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="c9a49-149">Pour vous assurer que le lecteur Windows Media recherche les travaux de téléchargement dans la file d’attente BITS, vous devez créer une valeur dans la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="c9a49-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="c9a49-150">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ services**</span><span class="sxs-lookup"><span data-stu-id="c9a49-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="c9a49-151">La valeur doit être créée comme suit.</span><span class="sxs-lookup"><span data-stu-id="c9a49-151">The value should be created as follows.</span></span>



| <span data-ttu-id="c9a49-152">Nom</span><span class="sxs-lookup"><span data-stu-id="c9a49-152">Name</span></span>                | <span data-ttu-id="c9a49-153">Type</span><span class="sxs-lookup"><span data-stu-id="c9a49-153">Type</span></span>      | <span data-ttu-id="c9a49-154">Description</span><span class="sxs-lookup"><span data-stu-id="c9a49-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a49-155">**RefreshDownload**</span><span class="sxs-lookup"><span data-stu-id="c9a49-155">**RefreshDownload**</span></span> | <span data-ttu-id="c9a49-156">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="c9a49-156">**DWORD**</span></span> | <span data-ttu-id="c9a49-157">Spécifie si le lecteur Windows Media doit inspecter la file d’attente BITS pour les travaux de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="c9a49-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="c9a49-158">Si la valeur est égale à zéro, le lecteur n’inspecte pas la file d’attente BITS.</span><span class="sxs-lookup"><span data-stu-id="c9a49-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="c9a49-159">Le joueur doit inspecter la file d’attente si la valeur est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c9a49-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="c9a49-160">Vous pouvez utiliser la syntaxe alternative suivante pour ajouter des tâches BITS qui ne se terminent pas par le lecteur Windows Media, mais pour lesquelles il affiche simplement des informations d’État :</span><span class="sxs-lookup"><span data-stu-id="c9a49-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="c9a49-161">Lorsque vous utilisez la syntaxe précédente, vous devez écrire du code pour terminer le téléchargement BITS, organiser le contenu sur l’ordinateur de l’utilisateur et ajouter le contenu à la bibliothèque, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="c9a49-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9a49-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9a49-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9a49-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="c9a49-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="c9a49-164">**DownloadItem. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c9a49-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="c9a49-165">**DownloadManager.getDownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="c9a49-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="c9a49-166">**Référence pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="c9a49-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 