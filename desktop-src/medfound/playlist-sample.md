---
description: Exemple de sélection
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Exemple de sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544735"
---
# <a name="playlist-sample"></a><span data-ttu-id="bc6cf-103">Exemple de sélection</span><span class="sxs-lookup"><span data-stu-id="bc6cf-103">Playlist Sample</span></span>

<span data-ttu-id="bc6cf-104">Montre comment utiliser Microsoft Media Foundation pour lire une séquence de fichiers audio dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="bc6cf-105">L’exemple utilise la [source de Sequencer](sequencer-source.md) pour créer et gérer la sélection.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="bc6cf-106">Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="bc6cf-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="bc6cf-107">API illustrées</span><span class="sxs-lookup"><span data-stu-id="bc6cf-107">APIs Demonstrated</span></span>

<span data-ttu-id="bc6cf-108">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc6cf-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="bc6cf-109">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="bc6cf-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="bc6cf-110">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="bc6cf-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="bc6cf-111">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="bc6cf-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="bc6cf-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="bc6cf-112">Usage</span></span>

<span data-ttu-id="bc6cf-113">L’exemple playlist génère une application Windows.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="bc6cf-114">Pour créer une sélection, sélectionnez **Ajouter à la sélection** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="bc6cf-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="bc6cf-115">Dans la boîte de dialogue **ouvrir un fichier** , sélectionnez un ou plusieurs fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="bc6cf-116">Les fichiers sont ajoutés à la sélection.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="bc6cf-117">Pour lire la séquence, cliquez sur **lire**.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="bc6cf-118">Pour suspendre le segment actuel, cliquez sur **suspendre**.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="bc6cf-119">Pour arrêter le segment actuel, cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="bc6cf-120">Pour passer à un fichier, double-cliquez sur l’élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="bc6cf-121">Pour supprimer un fichier de la sélection, sélectionnez l’élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="bc6cf-122">Sélectionnez ensuite **supprimer de la sélection** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="bc6cf-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6cf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc6cf-123">Requirements</span></span>



| <span data-ttu-id="bc6cf-124">Produit</span><span class="sxs-lookup"><span data-stu-id="bc6cf-124">Product</span></span>                                                        | <span data-ttu-id="bc6cf-125">Version</span><span class="sxs-lookup"><span data-stu-id="bc6cf-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bc6cf-126">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="bc6cf-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bc6cf-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc6cf-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bc6cf-128">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="bc6cf-128">Downloading the Sample</span></span>

<span data-ttu-id="bc6cf-129">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="bc6cf-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="bc6cf-130">Emplacement</span><span class="sxs-lookup"><span data-stu-id="bc6cf-130">Location</span></span>                                                     | <span data-ttu-id="bc6cf-131">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="bc6cf-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="bc6cf-132">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="bc6cf-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="bc6cf-133">*Racine* \\ du SDK Exemples \\ de \\ playlist mediafoundation Multimedia \\</span><span class="sxs-lookup"><span data-stu-id="bc6cf-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bc6cf-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc6cf-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc6cf-135">[Exemple BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc6cf-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bc6cf-136">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc6cf-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="bc6cf-137">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="bc6cf-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
