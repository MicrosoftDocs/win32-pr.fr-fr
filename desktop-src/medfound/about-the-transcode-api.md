---
description: À propos de l’API de transcodage
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: À propos de l’API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566542"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="16e33-103">À propos de l’API de transcodage</span><span class="sxs-lookup"><span data-stu-id="16e33-103">About the Transcode API</span></span>

<span data-ttu-id="16e33-104">Le diagramme suivant montre comment l’API de transcodage est en relation avec le reste du pipeline d’encodage Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="16e33-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![diagramme qui affiche l’API de transcodage.](images/encoding08.png)

<span data-ttu-id="16e33-106">Le pipeline d’encodage contient les objets de traitement de données suivants :</span><span class="sxs-lookup"><span data-stu-id="16e33-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="16e33-107">Source du média</span><span class="sxs-lookup"><span data-stu-id="16e33-107">Media source</span></span>
-   <span data-ttu-id="16e33-108">Décodeur</span><span class="sxs-lookup"><span data-stu-id="16e33-108">Decoder</span></span>
-   <span data-ttu-id="16e33-109">Redimensionnement vidéo ou rééchantillonneur audio</span><span class="sxs-lookup"><span data-stu-id="16e33-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="16e33-110">Encodeur</span><span class="sxs-lookup"><span data-stu-id="16e33-110">Encoder</span></span>
-   <span data-ttu-id="16e33-111">Récepteur multimédia</span><span class="sxs-lookup"><span data-stu-id="16e33-111">Media sink</span></span>

<span data-ttu-id="16e33-112">Le redimensionnement vidéo est nécessaire uniquement si la taille de la vidéo de sortie diffère de la source.</span><span class="sxs-lookup"><span data-stu-id="16e33-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="16e33-113">Le rééchantillonneur audio est nécessaire uniquement si l’audio doit être rééchantillonné avant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="16e33-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="16e33-114">La paire décodeur/encodeur est requise pour le transcodage, mais pas pour remuxing.</span><span class="sxs-lookup"><span data-stu-id="16e33-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="16e33-115">La *topologie* d’encodage est l’ensemble d’objets de pipeline (source, décodeur, redimensionnement, rééchantillonneur, encodeur et récepteur multimédia), ainsi que les points de connexion entre eux.</span><span class="sxs-lookup"><span data-stu-id="16e33-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="16e33-116">Pour plus d’informations sur les topologies, consultez [topologies](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="16e33-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="16e33-117">Différents composants sont chargés de créer les différents objets de pipeline :</span><span class="sxs-lookup"><span data-stu-id="16e33-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="16e33-118">L’application utilise généralement le programme de [résolution source](source-resolver.md) pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="16e33-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="16e33-119">La [session multimédia](media-session.md) charge et configure le décodeur, le redimensionnement vidéo et le rééchantillonneur audio.</span><span class="sxs-lookup"><span data-stu-id="16e33-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="16e33-120">En interne, elle utilise le chargeur de topologie pour effectuer cette opération (voir [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="16e33-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="16e33-121">L’API de transcodage charge et configure l’encodeur et le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="16e33-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="16e33-122">Les applications avancées peuvent configurer l’encodeur et le récepteur multimédia directement, plutôt que d’utiliser l’API de transcodage.</span><span class="sxs-lookup"><span data-stu-id="16e33-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16e33-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16e33-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e33-124">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="16e33-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="16e33-125">Utilisation de l’API de transcodage</span><span class="sxs-lookup"><span data-stu-id="16e33-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



