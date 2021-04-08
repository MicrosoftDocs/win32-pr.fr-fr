---
description: Configure la source de média ASF pour utiliser la recherche itérative si le fichier source n’a pas d’index.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761449"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="89e85-103">MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex, propriété</span><span class="sxs-lookup"><span data-stu-id="89e85-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="89e85-104">Configure la source de média ASF pour utiliser la recherche itérative si le fichier source n’a pas d’index.</span><span class="sxs-lookup"><span data-stu-id="89e85-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="89e85-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="89e85-105">Data type</span></span>

<span data-ttu-id="89e85-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="89e85-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="89e85-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="89e85-107">PROPVARIANT member</span></span>

<span data-ttu-id="89e85-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="89e85-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="89e85-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="89e85-109">VT\_BOOL</span></span>

<span data-ttu-id="89e85-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="89e85-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="89e85-111">Notes</span><span class="sxs-lookup"><span data-stu-id="89e85-111">Remarks</span></span>

<span data-ttu-id="89e85-112">Utilisez cette propriété pour configurer la source de média ASF.</span><span class="sxs-lookup"><span data-stu-id="89e85-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="89e85-113">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de *résolution source*.</span><span class="sxs-lookup"><span data-stu-id="89e85-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="89e85-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="89e85-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="89e85-115">La *recherche itérative* est un algorithme permettant de trouver une position dans un fichier ASF sans index.</span><span class="sxs-lookup"><span data-stu-id="89e85-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="89e85-116">Elle utilise une série de approximations, en fonction de la vitesse de transmission moyenne, pour se rapprocher progressivement du temps de recherche cible.</span><span class="sxs-lookup"><span data-stu-id="89e85-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="89e85-117">(L’algorithme est similaire à une recherche binaire.) La recherche itérative peut prendre plus de temps que la recherche par index. elle est donc désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="89e85-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="89e85-118">Si vous définissez cette propriété, utilisez les propriétés suivantes pour définir les paramètres de recherche :</span><span class="sxs-lookup"><span data-stu-id="89e85-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="89e85-119">Nombre maximal de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_</span><span class="sxs-lookup"><span data-stu-id="89e85-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="89e85-120">MFPKEY \_ ASFMediaSource \_ IterativeSeek la \_ tolérance \_ en \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="89e85-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="89e85-121">Ces propriétés définissent respectivement le nombre maximal d’itérations et la tolérance.</span><span class="sxs-lookup"><span data-stu-id="89e85-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="89e85-122">L’algorithme s’arrête lorsqu’il atteint le nombre maximal d’itérations, ou lorsqu’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89e85-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e85-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89e85-123">Requirements</span></span>



| <span data-ttu-id="89e85-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89e85-124">Requirement</span></span> | <span data-ttu-id="89e85-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="89e85-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89e85-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89e85-126">Minimum supported client</span></span><br/> | <span data-ttu-id="89e85-127">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="89e85-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="89e85-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89e85-128">Minimum supported server</span></span><br/> | <span data-ttu-id="89e85-129">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="89e85-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="89e85-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="89e85-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="89e85-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e85-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89e85-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89e85-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e85-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89e85-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




