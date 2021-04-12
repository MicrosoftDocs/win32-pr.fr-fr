---
title: Téléchargement du contenu multimédia
description: Téléchargement du contenu multimédia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Magasins en ligne du lecteur Windows Media, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- tapez 1 magasins en ligne, téléchargement de contenu multimédia
- Windows Media Player Online stores, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- types 1 magasins en ligne, téléchargement de contenu multimédia
- contenu multimédia, téléchargement
- Téléchargement du contenu multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381681"
---
# <a name="downloading-media-content"></a><span data-ttu-id="df462-111">Téléchargement du contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="df462-111">Downloading Media Content</span></span>

<span data-ttu-id="df462-112">Le lecteur Windows Media gère les téléchargements de fichiers musicaux pour le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="df462-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="df462-113">Un téléchargement peut être lancé lorsque la page de découverte appelle [External. Download](external-download.md) ou lorsque l’utilisateur choisit, dans le lecteur, de télécharger un ensemble de pistes.</span><span class="sxs-lookup"><span data-stu-id="df462-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="df462-114">Dans les deux cas, le lecteur Windows Media appelle [IWMPContentPartner ::D lécharger](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), en passant une liste de conteneurs de contenu qui décrit l’ensemble des pistes à télécharger et un cookie qui représente la transaction de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="df462-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="df462-115">Le plug-in de partenaire de contenu doit ensuite appeler [IWMPContentPartnerCallback ::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) une fois pour chaque piste du jeu.</span><span class="sxs-lookup"><span data-stu-id="df462-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="df462-116">Quand le plug-in appelle **DownloadTrack**, il passe un **HRESULT** dans le paramètre *hrDownload* .</span><span class="sxs-lookup"><span data-stu-id="df462-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="df462-117">Si le plug-in transmet un code de réussite dans *hrDownload*, le lecteur Windows Media télécharge la piste. Si le plug-in passe un code d’échec dans *hrDownload*, le lecteur ne télécharge pas la piste. Pour chaque appel de **Téléchargement**, le plug-in doit fournir le cookie de transaction et l’ID de la piste en question.</span><span class="sxs-lookup"><span data-stu-id="df462-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="df462-118">Pour les pistes qui sont réellement téléchargées, le plug-in doit également fournir l’URL de la piste.</span><span class="sxs-lookup"><span data-stu-id="df462-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="df462-119">Après le téléchargement d’un fichier, le lecteur Windows Media met automatiquement à jour la bibliothèque pour refléter la musique récemment achetée.</span><span class="sxs-lookup"><span data-stu-id="df462-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="df462-120">Le lecteur fournit des informations d’État au plug-in sur l’opération de téléchargement en appelant [IWMPContentPartner ::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span><span class="sxs-lookup"><span data-stu-id="df462-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="df462-121">Dans cette méthode, le lecteur fournit un **HRESULT** pour indiquer la réussite ou l’échec du téléchargement, l’ID de la piste et la chaîne de paramètres personnalisés fournie par le magasin en ligne lorsqu’il a appelé **DownloadTrack**.</span><span class="sxs-lookup"><span data-stu-id="df462-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df462-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df462-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df462-123">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="df462-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




