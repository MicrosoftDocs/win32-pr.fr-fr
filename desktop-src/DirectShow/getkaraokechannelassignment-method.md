---
description: La méthode GetKaraokeChannelAssignment récupère une valeur qui indique comment les canaux karaoké sont affectés aux intervenants.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Méthode GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846877"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="631b2-103">Méthode GetKaraokeChannelAssignment</span><span class="sxs-lookup"><span data-stu-id="631b2-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="631b2-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="631b2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="631b2-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="631b2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="631b2-106">La `GetKaraokeChannelAssignment` méthode récupère une valeur qui indique comment les canaux karaoké sont affectés aux intervenants.</span><span class="sxs-lookup"><span data-stu-id="631b2-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="631b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="631b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="631b2-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="631b2-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="631b2-109">Spécifie le flux audio sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="631b2-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="631b2-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="631b2-110">Return Value</span></span>

<span data-ttu-id="631b2-111">Retourne un entier indiquant l’assignation de l’intervenant pour le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="631b2-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="631b2-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="631b2-112">Return code</span></span> | <span data-ttu-id="631b2-113">Description</span><span class="sxs-lookup"><span data-stu-id="631b2-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="631b2-114">2</span><span class="sxs-lookup"><span data-stu-id="631b2-114">2</span></span>           | <span data-ttu-id="631b2-115">Le flux est affecté aux haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="631b2-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="631b2-116">3</span><span class="sxs-lookup"><span data-stu-id="631b2-116">3</span></span>           | <span data-ttu-id="631b2-117">Le flux est affecté aux haut-parleurs gauche, droit et moyen.</span><span class="sxs-lookup"><span data-stu-id="631b2-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="631b2-118">4</span><span class="sxs-lookup"><span data-stu-id="631b2-118">4</span></span>           | <span data-ttu-id="631b2-119">Le flux est affecté aux haut-parleurs gauche, droite et Audio1.</span><span class="sxs-lookup"><span data-stu-id="631b2-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="631b2-120">5</span><span class="sxs-lookup"><span data-stu-id="631b2-120">5</span></span>           | <span data-ttu-id="631b2-121">Le flux est affecté aux haut-parleurs gauche, droit, moyen et Audio1.</span><span class="sxs-lookup"><span data-stu-id="631b2-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="631b2-122">6</span><span class="sxs-lookup"><span data-stu-id="631b2-122">6</span></span>           | <span data-ttu-id="631b2-123">Le flux est affecté aux haut-parleurs gauche, droite et Audio2.</span><span class="sxs-lookup"><span data-stu-id="631b2-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="631b2-124">7</span><span class="sxs-lookup"><span data-stu-id="631b2-124">7</span></span>           | <span data-ttu-id="631b2-125">Le flux est affecté aux haut-parleurs gauche, droit, moyen et Audio2.</span><span class="sxs-lookup"><span data-stu-id="631b2-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="631b2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="631b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631b2-127">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="631b2-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



