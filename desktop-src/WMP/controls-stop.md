---
title: Controls. Stop, méthode
description: La méthode Stop arrête la lecture de l’élément multimédia. | Controls. Stop, méthode
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- méthode Stop lecteur Windows Media
- méthode Stop lecteur Windows Media, classe Controls
- Controls, classe Windows Media Player, stop, méthode
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533039"
---
# <a name="controlsstop-method"></a><span data-ttu-id="3a505-107">Controls. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="3a505-107">Controls.stop method</span></span>

<span data-ttu-id="3a505-108">La méthode **Stop** arrête la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3a505-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a505-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a505-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="3a505-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a505-110">Parameters</span></span>

<span data-ttu-id="3a505-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3a505-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a505-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a505-112">Return value</span></span>

<span data-ttu-id="3a505-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3a505-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a505-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3a505-114">Remarks</span></span>

<span data-ttu-id="3a505-115">Cette méthode force le lecteur Windows Media à libérer toutes les ressources système qu’il utilise, telles que le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="3a505-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="3a505-116">Toutefois, l’élément multimédia actuel n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="3a505-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="3a505-117">Lorsque le joueur est arrêté, le suivi se rembobine au début.</span><span class="sxs-lookup"><span data-stu-id="3a505-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="3a505-118">L' **appel de la lecture commence** ensuite la lecture du clip à partir du début.</span><span class="sxs-lookup"><span data-stu-id="3a505-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="3a505-119">Pour arrêter une opération de lecture sans modifier la position actuelle, utilisez la méthode **Pause** .</span><span class="sxs-lookup"><span data-stu-id="3a505-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="3a505-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3a505-120">Examples</span></span>

<span data-ttu-id="3a505-121">L’exemple suivant crée un élément BUTTON HTML qui utilise **Stop** pour arrêter la lecture.</span><span class="sxs-lookup"><span data-stu-id="3a505-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="3a505-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3a505-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="3a505-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a505-123">Requirements</span></span>



| <span data-ttu-id="3a505-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a505-124">Requirement</span></span> | <span data-ttu-id="3a505-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a505-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a505-126">Version</span><span class="sxs-lookup"><span data-stu-id="3a505-126">Version</span></span><br/> | <span data-ttu-id="3a505-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a505-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3a505-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a505-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a505-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a505-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a505-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a505-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a505-131">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="3a505-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="3a505-132">**Contrôles. Next**</span><span class="sxs-lookup"><span data-stu-id="3a505-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="3a505-133">**Controls. pause**</span><span class="sxs-lookup"><span data-stu-id="3a505-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="3a505-134">**Contrôles. Previous**</span><span class="sxs-lookup"><span data-stu-id="3a505-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





