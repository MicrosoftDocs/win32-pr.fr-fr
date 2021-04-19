---
title: THEMe. playSound
description: La méthode playSound lit le fichier son spécifié.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THÈME. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528140"
---
# <a name="themeplaysound"></a><span data-ttu-id="a42cf-104">THEMe. playSound</span><span class="sxs-lookup"><span data-stu-id="a42cf-104">THEME.playSound</span></span>

<span data-ttu-id="a42cf-105">La méthode **playSound** lit le fichier son spécifié.</span><span class="sxs-lookup"><span data-stu-id="a42cf-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="a42cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a42cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a42cf-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="a42cf-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="a42cf-108">**Chaîne** spécifiant le nom du fichier son à lire.</span><span class="sxs-lookup"><span data-stu-id="a42cf-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a42cf-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a42cf-109">Return Value</span></span>

<span data-ttu-id="a42cf-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a42cf-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a42cf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a42cf-111">Remarks</span></span>

<span data-ttu-id="a42cf-112">Cette méthode vous permet d’ajouter des effets sonores à une apparence, par exemple, en cas de clic sur les boutons.</span><span class="sxs-lookup"><span data-stu-id="a42cf-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="a42cf-113">Le son est lu par le système d’exploitation directement et non par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a42cf-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="a42cf-114">Cela signifie que le son ne peut pas être contrôlé avec les paramètres et les méthodes du lecteur Windows Media, mais il peut être lu pendant que le lecteur Windows Media lit un autre fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="a42cf-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="a42cf-115">Cette méthode prend en charge uniquement les fichiers WAV.</span><span class="sxs-lookup"><span data-stu-id="a42cf-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="a42cf-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a42cf-116">Requirements</span></span>



| <span data-ttu-id="a42cf-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a42cf-117">Requirement</span></span> | <span data-ttu-id="a42cf-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a42cf-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a42cf-119">Version</span><span class="sxs-lookup"><span data-stu-id="a42cf-119">Version</span></span><br/> | <span data-ttu-id="a42cf-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a42cf-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a42cf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a42cf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a42cf-122">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="a42cf-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





