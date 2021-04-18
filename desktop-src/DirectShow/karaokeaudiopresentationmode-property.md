---
description: La propriété KaraokeAudioPresentationMode définit ou récupère la combinaison d’orateurs de droite à gauche pour les canaux karaoké auxiliaires.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propriété KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513093"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="eba7d-103">Propriété KaraokeAudioPresentationMode</span><span class="sxs-lookup"><span data-stu-id="eba7d-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="eba7d-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eba7d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eba7d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eba7d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eba7d-106">La `KaraokeAudioPresentationMode` propriété définit ou récupère la combinaison d’orateurs de droite à gauche pour les canaux karaoké auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="eba7d-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="eba7d-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eba7d-107">Return Value</span></span>

<span data-ttu-id="eba7d-108">Retourne une valeur entière contenant un jeu d’indicateurs binaires indiquant comment les canaux karaoké auxiliaires sont downmixeds aux haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="eba7d-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba7d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="eba7d-109">Remarks</span></span>

<span data-ttu-id="eba7d-110">Cette propriété est en lecture/écriture avec une valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="eba7d-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="eba7d-111">Les canaux audio étant de base zéro, les canaux 0 et 1 représentent généralement les canaux de haut-parleur droit et gauche et les canaux 2 à 4 sont les trois canaux karaoké auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="eba7d-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="eba7d-112">Lorsque l’objet MSWebDVD passe en mode karaoké, il désactive automatiquement les canaux 2 et supérieurs.</span><span class="sxs-lookup"><span data-stu-id="eba7d-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="eba7d-113">Utilisez des **opérations or au niveau du** bit pour définir le bit approprié afin d’envoyer un canal auxiliaire vers le haut-parleur gauche, le haut-parleur droit, les deux haut-parleurs (bits sur) ou aucun orateur (les deux bits sont désactivés).</span><span class="sxs-lookup"><span data-stu-id="eba7d-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="eba7d-114">Ces bits sont désactivés par défaut chaque fois que le navigateur DVD passe en mode karaoké.</span><span class="sxs-lookup"><span data-stu-id="eba7d-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="eba7d-115">La valeur des bits et leurs actions correspondantes sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="eba7d-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="eba7d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eba7d-116">Value</span></span>  | <span data-ttu-id="eba7d-117">Description</span><span class="sxs-lookup"><span data-stu-id="eba7d-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="eba7d-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="eba7d-118">0x0004</span></span> | <span data-ttu-id="eba7d-119">Downmix canal 2 vers le haut-parleur gauche</span><span class="sxs-lookup"><span data-stu-id="eba7d-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="eba7d-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="eba7d-120">0x0008</span></span> | <span data-ttu-id="eba7d-121">Downmix canal 3 vers le haut-parleur gauche</span><span class="sxs-lookup"><span data-stu-id="eba7d-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="eba7d-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="eba7d-122">0x0010</span></span> | <span data-ttu-id="eba7d-123">Downmix canal 4 vers le haut-parleur gauche</span><span class="sxs-lookup"><span data-stu-id="eba7d-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="eba7d-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="eba7d-124">0x0400</span></span> | <span data-ttu-id="eba7d-125">Downmix canal 2 vers le haut-parleur droit</span><span class="sxs-lookup"><span data-stu-id="eba7d-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="eba7d-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="eba7d-126">0x0800</span></span> | <span data-ttu-id="eba7d-127">Downmix canal 3 vers le haut-parleur droit</span><span class="sxs-lookup"><span data-stu-id="eba7d-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="eba7d-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="eba7d-128">0x1000</span></span> | <span data-ttu-id="eba7d-129">Downmix canal 4 vers le haut-parleur droit</span><span class="sxs-lookup"><span data-stu-id="eba7d-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



