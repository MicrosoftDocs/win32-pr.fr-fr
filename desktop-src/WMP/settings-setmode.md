---
title: Settings. setMode, méthode
description: La méthode setMode définit différents modes comme active ou inactive.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- méthode setMode lecteur Windows Media
- méthode setMode lecteur Windows Media, classe de paramètres
- Classe de paramètres lecteur Windows Media, méthode setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520893"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="6feb1-106">Settings. setMode, méthode</span><span class="sxs-lookup"><span data-stu-id="6feb1-106">Settings.setMode method</span></span>

<span data-ttu-id="6feb1-107">La méthode **setMode** définit différents modes comme active ou inactive.</span><span class="sxs-lookup"><span data-stu-id="6feb1-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6feb1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6feb1-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="6feb1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6feb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6feb1-110">*modeName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feb1-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feb1-111">**Chaîne** spécifiant le nom du mode en cours de modification, contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6feb1-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="6feb1-112">String</span><span class="sxs-lookup"><span data-stu-id="6feb1-112">String</span></span>     | <span data-ttu-id="6feb1-113">Description</span><span class="sxs-lookup"><span data-stu-id="6feb1-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6feb1-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="6feb1-114">autoRewind</span></span> | <span data-ttu-id="6feb1-115">Mode indiquant si les pistes sont rembobinées jusqu’au début après avoir été lues jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="6feb1-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="6feb1-116">L’État par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="6feb1-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="6feb1-117">loop</span><span class="sxs-lookup"><span data-stu-id="6feb1-117">loop</span></span>       | <span data-ttu-id="6feb1-118">Mode indiquant si la séquence de suivi se répète lui-même.</span><span class="sxs-lookup"><span data-stu-id="6feb1-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="6feb1-119">L’État par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="6feb1-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="6feb1-120">showFrame</span><span class="sxs-lookup"><span data-stu-id="6feb1-120">showFrame</span></span>  | <span data-ttu-id="6feb1-121">Mode indiquant si l’image clé vidéo la plus proche s’affiche à la position actuelle lorsqu’elle n’est pas lue.</span><span class="sxs-lookup"><span data-stu-id="6feb1-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="6feb1-122">L’État par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="6feb1-122">Default state is false.</span></span> <span data-ttu-id="6feb1-123">N’a aucun effet sur les pistes audio.</span><span class="sxs-lookup"><span data-stu-id="6feb1-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="6feb1-124">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="6feb1-124">shuffle</span></span>    | <span data-ttu-id="6feb1-125">Mode indiquant si les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="6feb1-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="6feb1-126">L’État par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="6feb1-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="6feb1-127">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6feb1-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6feb1-128">**Valeur booléenne** indiquant si le nouveau mode spécifié est actif ou non.</span><span class="sxs-lookup"><span data-stu-id="6feb1-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6feb1-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6feb1-129">Return value</span></span>

<span data-ttu-id="6feb1-130">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6feb1-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6feb1-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6feb1-131">Remarks</span></span>

<span data-ttu-id="6feb1-132">Lorsque le mode showFrame est actif, le joueur doit accéder au contenu Track pour récupérer l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="6feb1-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="6feb1-133">En raison des considérations relatives à la bande passante, utilisez ce mode avec précaution lors de la diffusion de contenu non local.</span><span class="sxs-lookup"><span data-stu-id="6feb1-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="6feb1-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6feb1-134">Requirements</span></span>



| <span data-ttu-id="6feb1-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6feb1-135">Requirement</span></span> | <span data-ttu-id="6feb1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6feb1-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6feb1-137">Version</span><span class="sxs-lookup"><span data-stu-id="6feb1-137">Version</span></span><br/> | <span data-ttu-id="6feb1-138">Pour les modes boucle et lecture aléatoire, le lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6feb1-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="6feb1-139">Pour les modes autoRewind et showFrame, le lecteur Windows Media 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6feb1-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="6feb1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6feb1-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="6feb1-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6feb1-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="6feb1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6feb1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6feb1-143">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="6feb1-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="6feb1-144">**Paramètres. getMode**</span><span class="sxs-lookup"><span data-stu-id="6feb1-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





