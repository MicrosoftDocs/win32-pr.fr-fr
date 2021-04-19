---
title: Controls. pause, méthode
description: La méthode pause interrompt la lecture de l’élément multimédia. | Controls. pause, méthode
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- méthode pause lecteur Windows Media
- méthode pause lecteur Windows Media, classe contrôles
- Controls, classe Windows Media Player, pause, méthode
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540611"
---
# <a name="controlspause-method"></a><span data-ttu-id="c75a6-107">Controls. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="c75a6-107">Controls.pause method</span></span>

<span data-ttu-id="c75a6-108">La méthode **Pause** interrompt la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="c75a6-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75a6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c75a6-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="c75a6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c75a6-110">Parameters</span></span>

<span data-ttu-id="c75a6-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c75a6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c75a6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c75a6-112">Return value</span></span>

<span data-ttu-id="c75a6-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c75a6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75a6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c75a6-114">Remarks</span></span>

<span data-ttu-id="c75a6-115">Lorsqu’un fichier est en pause, le lecteur Windows Media n’accorde aucune ressource système, telle que le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="c75a6-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="c75a6-116">Certains types de média ne peuvent pas être suspendus, tels que les flux en direct.</span><span class="sxs-lookup"><span data-stu-id="c75a6-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="c75a6-117">Pour déterminer si un type de média particulier peut être suspendu, utilisez des *contrôles*. **isAvailable ('Pause')**.</span><span class="sxs-lookup"><span data-stu-id="c75a6-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="c75a6-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="c75a6-118">Examples</span></span>

<span data-ttu-id="c75a6-119">L’exemple suivant crée un élément bouton HTML qui utilise **Pause** pour suspendre la lecture.</span><span class="sxs-lookup"><span data-stu-id="c75a6-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="c75a6-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c75a6-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="c75a6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c75a6-121">Requirements</span></span>



| <span data-ttu-id="c75a6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c75a6-122">Requirement</span></span> | <span data-ttu-id="c75a6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c75a6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c75a6-124">Version</span><span class="sxs-lookup"><span data-stu-id="c75a6-124">Version</span></span><br/> | <span data-ttu-id="c75a6-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c75a6-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c75a6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c75a6-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c75a6-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c75a6-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75a6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c75a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75a6-129">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="c75a6-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c75a6-130">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="c75a6-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





