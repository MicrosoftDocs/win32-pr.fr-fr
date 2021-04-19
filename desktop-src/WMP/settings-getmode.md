---
title: Settings. getMode, méthode
description: La méthode getMode détermine si le mode de boucle ou le mode de lecture aléatoire est actif.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- méthode getMode lecteur Windows Media
- méthode getMode lecteur Windows Media, classe de paramètres
- Classe de paramètres lecteur Windows Media, méthode getMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520894"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="9e746-106">Settings. getMode, méthode</span><span class="sxs-lookup"><span data-stu-id="9e746-106">Settings.getMode method</span></span>

<span data-ttu-id="9e746-107">La méthode **getMode** détermine si le mode de boucle ou le mode de lecture aléatoire est actif.</span><span class="sxs-lookup"><span data-stu-id="9e746-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e746-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e746-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="9e746-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e746-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e746-110">*modeName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e746-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e746-111">**Chaîne** spécifiant le nom du mode en question, contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9e746-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="9e746-112">String</span><span class="sxs-lookup"><span data-stu-id="9e746-112">String</span></span>     | <span data-ttu-id="9e746-113">Description</span><span class="sxs-lookup"><span data-stu-id="9e746-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e746-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="9e746-114">autoRewind</span></span> | <span data-ttu-id="9e746-115">Les suivis sont redémarrés au début après avoir été lus jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="9e746-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="9e746-116">loop</span><span class="sxs-lookup"><span data-stu-id="9e746-116">loop</span></span>       | <span data-ttu-id="9e746-117">La séquence de suivi se répète lui-même.</span><span class="sxs-lookup"><span data-stu-id="9e746-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="9e746-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="9e746-118">showFrame</span></span>  | <span data-ttu-id="9e746-119">L’image clé la plus proche s’affiche à la position actuelle lorsqu’elle n’est pas lue.</span><span class="sxs-lookup"><span data-stu-id="9e746-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="9e746-120">Ce mode n’est pas pertinent pour les pistes audio.</span><span class="sxs-lookup"><span data-stu-id="9e746-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="9e746-121">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="9e746-121">shuffle</span></span>    | <span data-ttu-id="9e746-122">Les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="9e746-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e746-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e746-123">Return value</span></span>

<span data-ttu-id="9e746-124">Cette méthode retourne une valeur **booléenne** indiquant si le mode spécifié est actif.</span><span class="sxs-lookup"><span data-stu-id="9e746-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e746-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e746-125">Requirements</span></span>



| <span data-ttu-id="9e746-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e746-126">Requirement</span></span> | <span data-ttu-id="9e746-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e746-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e746-128">Version</span><span class="sxs-lookup"><span data-stu-id="9e746-128">Version</span></span><br/> | <span data-ttu-id="9e746-129">Pour les modes boucle et lecture aléatoire, le lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9e746-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="9e746-130">Pour les modes autoRewind et showFrame, le lecteur Windows Media 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9e746-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="9e746-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e746-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e746-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e746-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="9e746-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e746-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e746-134">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="9e746-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="9e746-135">**Paramètres. setMode**</span><span class="sxs-lookup"><span data-stu-id="9e746-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





