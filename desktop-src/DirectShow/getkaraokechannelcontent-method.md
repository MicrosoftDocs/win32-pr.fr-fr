---
description: La méthode GetKaraokeChannelContent récupère une valeur qui indique le type de contenu dans le canal karaoké spécifié dans le flux spécifié.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Méthode GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512862"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="86637-103">Méthode GetKaraokeChannelContent</span><span class="sxs-lookup"><span data-stu-id="86637-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="86637-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="86637-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86637-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="86637-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86637-106">La `GetKaraokeChannelContent` méthode récupère une valeur qui indique le type de contenu dans le canal karaoké spécifié dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="86637-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="86637-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86637-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86637-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="86637-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="86637-109">Spécifie le flux audio sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="86637-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="86637-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="86637-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="86637-111">Spécifie le canal sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="86637-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="86637-112">Les valeurs possibles pour chaque canal sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="86637-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="86637-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="86637-113">Value</span></span>  | <span data-ttu-id="86637-114">Description</span><span class="sxs-lookup"><span data-stu-id="86637-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="86637-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="86637-115">0x0001</span></span> | <span data-ttu-id="86637-116">Guide vocal 1</span><span class="sxs-lookup"><span data-stu-id="86637-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="86637-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="86637-117">0x0002</span></span> | <span data-ttu-id="86637-118">Guide vocal 2</span><span class="sxs-lookup"><span data-stu-id="86637-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="86637-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="86637-119">0x0004</span></span> | <span data-ttu-id="86637-120">Guide mélodie 1</span><span class="sxs-lookup"><span data-stu-id="86637-120">Guide Melody 1</span></span> |
| <span data-ttu-id="86637-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="86637-121">0x0008</span></span> | <span data-ttu-id="86637-122">Guide mélodie 2</span><span class="sxs-lookup"><span data-stu-id="86637-122">Guide Melody 2</span></span> |
| <span data-ttu-id="86637-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="86637-123">0x0010</span></span> | <span data-ttu-id="86637-124">Guide mélodie A</span><span class="sxs-lookup"><span data-stu-id="86637-124">Guide Melody A</span></span> |
| <span data-ttu-id="86637-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="86637-125">0x0020</span></span> | <span data-ttu-id="86637-126">Guide mélodie B</span><span class="sxs-lookup"><span data-stu-id="86637-126">Guide Melody B</span></span> |
| <span data-ttu-id="86637-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="86637-127">0x0040</span></span> | <span data-ttu-id="86637-128">Effet sonore A</span><span class="sxs-lookup"><span data-stu-id="86637-128">Sound Effect A</span></span> |
| <span data-ttu-id="86637-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="86637-129">0x0080</span></span> | <span data-ttu-id="86637-130">Effet sonore B</span><span class="sxs-lookup"><span data-stu-id="86637-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86637-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86637-131">Return Value</span></span>

<span data-ttu-id="86637-132">Retourne une valeur entière dont les bits individuels spécifient le contenu du canal karaoké.</span><span class="sxs-lookup"><span data-stu-id="86637-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="86637-133">Notes</span><span class="sxs-lookup"><span data-stu-id="86637-133">Remarks</span></span>

<span data-ttu-id="86637-134">La numérotation des canaux audio DVD est basée sur zéro, donc les canaux 2, 3 et 4 sont les canaux karaoké auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="86637-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="86637-135">Une fois la méthode retournée, effectuez une opération and au niveau du bit sur *icontent* pour déterminer le contenu de chaque canal.</span><span class="sxs-lookup"><span data-stu-id="86637-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="86637-136">Étant donné qu’un seul canal peut avoir plusieurs types de contenu enregistrés, vous devez tester toutes les valeurs possibles même si une correspondance est trouvée.</span><span class="sxs-lookup"><span data-stu-id="86637-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="86637-137">Une fois que l’utilisateur a connaissance du contenu de chaque canal, il doit être en mesure d’ajuster le volume ou d’activer ou de désactiver les canaux individuels en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="86637-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="86637-138">Implémentez cette fonctionnalité dans votre application à l’aide de la propriété [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="86637-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="86637-139">Pour lire des disques karaoké, le décodeur audio sur le système de l’utilisateur doit être compatible avec l’implémentation du karaoké DirectShow 8.</span><span class="sxs-lookup"><span data-stu-id="86637-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



