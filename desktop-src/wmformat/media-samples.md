---
title: Exemples de supports (SDK Windows Media format 11)
description: Découvrez les exemples de supports dans le kit de développement logiciel (SDK) Windows Media format 11. Un exemple de média est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, exemples de supports
- Kit de développement logiciel (SDK) Windows Media format, exemples
- ASF (Advanced Systems Format), exemples de supports
- ASF (Advanced Systems Format), exemples de supports
- ASF (Advanced Systems Format), exemples
- ASF (format avancé des systèmes), exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989070"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="37974-110">Exemples de supports (SDK Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="37974-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="37974-111">Un échantillon de support, ou échantillon, est un bloc de données multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="37974-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="37974-112">Un exemple est l’unité de base manipulée par les objets de lecture et d’écriture du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="37974-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="37974-113">Le contenu d’un exemple individuel est dicté par le type de média associé à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="37974-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="37974-114">Pour les vidéos, chaque échantillon représente un frame unique.</span><span class="sxs-lookup"><span data-stu-id="37974-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="37974-115">Pour le son, la quantité de données dans un échantillon individuel est définie dans le profil utilisé pour créer le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="37974-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="37974-116">Les exemples peuvent contenir des données non compressées, ou elles peuvent contenir des données compressées, auquel cas ils sont appelés *exemples de flux*.</span><span class="sxs-lookup"><span data-stu-id="37974-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="37974-117">Lors de la création d’un fichier ASF, vous transmettez des exemples au writer.</span><span class="sxs-lookup"><span data-stu-id="37974-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="37974-118">L’enregistreur coordonne la compression des exemples avec le codec approprié et organise les données compressées dans la section de données du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="37974-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="37974-119">Lors de la lecture, le lecteur lit les données compressées, les décompresse et fournit les données non compressées reconstruites comme exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="37974-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="37974-120">Tous les exemples utilisés par le kit de développement logiciel (SDK) de format Windows Media sont encapsulés dans un objet tampon dont la mémoire est allouée automatiquement par les composants runtime du SDK.</span><span class="sxs-lookup"><span data-stu-id="37974-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="37974-121">Vous pouvez également allouer vos propres tampons, si nécessaire, à l’aide des fonctionnalités avancées du writer et du lecteur.</span><span class="sxs-lookup"><span data-stu-id="37974-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="37974-122">**Remarque** Le terme exemple est utilisé dans ce kit de développement logiciel (SDK) pour faire référence à un exemple de support, et non à un exemple audio.</span><span class="sxs-lookup"><span data-stu-id="37974-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="37974-123">Dans l’encodage audio, un exemple fait référence à une seule valeur audio encodée.</span><span class="sxs-lookup"><span data-stu-id="37974-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="37974-124">En règle générale, la qualité de l’audio encodé est spécifiée par un nombre d’échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="37974-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="37974-125">Par exemple, le son de qualité CD est enregistré à 44 100 échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="37974-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="37974-126">Cette valeur est généralement abrégée avec la notation Hz, donc 44 100 échantillons par seconde sont 44 100 Hz ou 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="37974-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37974-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37974-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37974-128">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="37974-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="37974-129">**Interface INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="37974-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="37974-130">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="37974-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




