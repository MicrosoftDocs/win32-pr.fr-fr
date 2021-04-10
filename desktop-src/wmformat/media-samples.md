---
title: Exemples de supports (SDK Windows Media format 11)
description: Exemples de supports
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
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941610"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="54e48-109">Exemples de supports (SDK Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="54e48-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="54e48-110">Un échantillon de support, ou échantillon, est un bloc de données multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="54e48-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="54e48-111">Un exemple est l’unité de base manipulée par les objets de lecture et d’écriture du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="54e48-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="54e48-112">Le contenu d’un exemple individuel est dicté par le type de média associé à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="54e48-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="54e48-113">Pour les vidéos, chaque échantillon représente un frame unique.</span><span class="sxs-lookup"><span data-stu-id="54e48-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="54e48-114">Pour le son, la quantité de données dans un échantillon individuel est définie dans le profil utilisé pour créer le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="54e48-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="54e48-115">Les exemples peuvent contenir des données non compressées, ou elles peuvent contenir des données compressées, auquel cas ils sont appelés *exemples de flux*.</span><span class="sxs-lookup"><span data-stu-id="54e48-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="54e48-116">Lors de la création d’un fichier ASF, vous transmettez des exemples au writer.</span><span class="sxs-lookup"><span data-stu-id="54e48-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="54e48-117">L’enregistreur coordonne la compression des exemples avec le codec approprié et organise les données compressées dans la section de données du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="54e48-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="54e48-118">Lors de la lecture, le lecteur lit les données compressées, les décompresse et fournit les données non compressées reconstruites comme exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="54e48-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="54e48-119">Tous les exemples utilisés par le kit de développement logiciel (SDK) de format Windows Media sont encapsulés dans un objet tampon dont la mémoire est allouée automatiquement par les composants runtime du SDK.</span><span class="sxs-lookup"><span data-stu-id="54e48-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="54e48-120">Vous pouvez également allouer vos propres tampons, si nécessaire, à l’aide des fonctionnalités avancées du writer et du lecteur.</span><span class="sxs-lookup"><span data-stu-id="54e48-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="54e48-121">**Remarque** Le terme exemple est utilisé dans ce kit de développement logiciel (SDK) pour faire référence à un exemple de support, et non à un exemple audio.</span><span class="sxs-lookup"><span data-stu-id="54e48-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="54e48-122">Dans l’encodage audio, un exemple fait référence à une seule valeur audio encodée.</span><span class="sxs-lookup"><span data-stu-id="54e48-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="54e48-123">En règle générale, la qualité de l’audio encodé est spécifiée par un nombre d’échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="54e48-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="54e48-124">Par exemple, le son de qualité CD est enregistré à 44 100 échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="54e48-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="54e48-125">Cette valeur est généralement abrégée avec la notation Hz, donc 44 100 échantillons par seconde sont 44 100 Hz ou 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="54e48-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54e48-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54e48-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e48-127">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="54e48-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="54e48-128">**Interface INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="54e48-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="54e48-129">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="54e48-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




