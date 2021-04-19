---
description: Architecture DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Architecture DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515523"
---
# <a name="dmo-architecture"></a><span data-ttu-id="03d61-103">Architecture DMO</span><span class="sxs-lookup"><span data-stu-id="03d61-103">DMO Architecture</span></span>

<span data-ttu-id="03d61-104">Cette section décrit l’architecture globale d’un DMO.</span><span class="sxs-lookup"><span data-stu-id="03d61-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="03d61-105">**Flux**</span><span class="sxs-lookup"><span data-stu-id="03d61-105">**Streams**</span></span>

<span data-ttu-id="03d61-106">Un objet DMO est un objet qui prend des entrées *m* et produit *n* sorties.</span><span class="sxs-lookup"><span data-stu-id="03d61-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="03d61-107">Les entrées et les sorties sont appelées des *flux*.</span><span class="sxs-lookup"><span data-stu-id="03d61-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="03d61-108">Chaque DMO a au moins un flux.</span><span class="sxs-lookup"><span data-stu-id="03d61-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="03d61-109">Les flux ne sont pas des objets ; ils sont simplement référencés sur le numéro d’index DMO.</span><span class="sxs-lookup"><span data-stu-id="03d61-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="03d61-110">Le nombre de flux est défini au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="03d61-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="03d61-111">**Types de médias**</span><span class="sxs-lookup"><span data-stu-id="03d61-111">**Media Types**</span></span>

<span data-ttu-id="03d61-112">Toutes les données sont tapées à l’aide d’un *type de média*, qui définit comment interpréter le contenu des données.</span><span class="sxs-lookup"><span data-stu-id="03d61-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="03d61-113">Par exemple, la vidéo RGB 320 x 240 24 bits est un type ; 44,1-kilohertz (kHz) audio stéréo 16 bits est un autre type.</span><span class="sxs-lookup"><span data-stu-id="03d61-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="03d61-114">Les types de supports sont décrits à l’aide de la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="03d61-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="03d61-115">Avant que le client puisse traiter des données, il doit définir le type de support pour chaque flux de données dans la méthode DMO.</span><span class="sxs-lookup"><span data-stu-id="03d61-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="03d61-116">En règle générale, un flux peut accepter une plage de types de médias.</span><span class="sxs-lookup"><span data-stu-id="03d61-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="03d61-117">Certains DMOs prennent en charge un plus grand nombre de types que d’autres.</span><span class="sxs-lookup"><span data-stu-id="03d61-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="03d61-118">Les interfaces DMO définissent les méthodes pour que le client Découvre les types pris en charge.</span><span class="sxs-lookup"><span data-stu-id="03d61-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="03d61-119">Par exemple, un DMO peut prendre en charge la vidéo RVB en toute profondeur, tandis qu’un autre peut prendre en charge uniquement la couleur RVB 24 bits.</span><span class="sxs-lookup"><span data-stu-id="03d61-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="03d61-120">En outre, un DMO peut être limité à certaines combinaisons d’entrées et de sorties.</span><span class="sxs-lookup"><span data-stu-id="03d61-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="03d61-121">Par exemple, si le type d’entrée est vidéo 16 bits, le flux de sortie peut nécessiter la même profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="03d61-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="03d61-122">Le client peut énumérer les types préférés de chaque flux, puis tester des combinaisons spécifiques.</span><span class="sxs-lookup"><span data-stu-id="03d61-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="03d61-123">**Mémoires tampons**</span><span class="sxs-lookup"><span data-stu-id="03d61-123">**Buffers**</span></span>

<span data-ttu-id="03d61-124">Dans le modèle DMO par défaut, le client alloue des mémoires tampons d’entrée et de sortie distinctes.</span><span class="sxs-lookup"><span data-stu-id="03d61-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="03d61-125">Il remplit les tampons d’entrée avec les données et les remet à la solution DMO, et le DMO écrit de nouvelles données dans les mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="03d61-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="03d61-126">Si vous le souhaitez, un module DMO peut prendre en charge le traitement « sur place ».</span><span class="sxs-lookup"><span data-stu-id="03d61-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="03d61-127">Avec le traitement sur place, DMO écrit la sortie directement dans la mémoire tampon d’entrée, sur les données d’origine.</span><span class="sxs-lookup"><span data-stu-id="03d61-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="03d61-128">Le traitement sur place élimine la nécessité de mémoires tampons distinctes.</span><span class="sxs-lookup"><span data-stu-id="03d61-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="03d61-129">D’un autre côté, il modifie les données d’origine, ce qui peut ne pas être acceptable pour certaines applications.</span><span class="sxs-lookup"><span data-stu-id="03d61-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="03d61-130">Le modèle de mise en mémoire tampon par défaut (non sur place) est pris en charge via l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="03d61-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="03d61-131">Toutes les DMOs doivent implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="03d61-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="03d61-132">Si un module DMO prend en charge le traitement sur place, il expose également l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="03d61-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="03d61-133">Le client est responsable de l’allocation de toutes les mémoires tampons, à la fois en entrée et en sortie.</span><span class="sxs-lookup"><span data-stu-id="03d61-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03d61-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03d61-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d61-135">À propos de DMOs</span><span class="sxs-lookup"><span data-stu-id="03d61-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



