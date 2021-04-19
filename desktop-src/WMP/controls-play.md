---
title: Controls. Play, méthode
description: La méthode Play entraîne le démarrage de la lecture de l’élément multimédia actuel ou reprend la lecture d’un élément suspendu.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Play, méthode lecteur Windows Media
- méthode Play lecteur Windows Media, classe Controls
- Controls, classe Windows Media Player, Play, méthode
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537822"
---
# <a name="controlsplay-method"></a><span data-ttu-id="ddde7-106">Controls. Play, méthode</span><span class="sxs-lookup"><span data-stu-id="ddde7-106">Controls.play method</span></span>

<span data-ttu-id="ddde7-107">La méthode **Play** entraîne le démarrage de la lecture de l’élément multimédia actuel ou reprend la lecture d’un élément suspendu.</span><span class="sxs-lookup"><span data-stu-id="ddde7-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddde7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddde7-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="ddde7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddde7-109">Parameters</span></span>

<span data-ttu-id="ddde7-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ddde7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddde7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddde7-111">Return value</span></span>

<span data-ttu-id="ddde7-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ddde7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddde7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ddde7-113">Remarks</span></span>

<span data-ttu-id="ddde7-114">Si cette méthode est appelée pendant le transfert rapide ou le rembobinage, il s’agit de la valeur des *paramètres*. la valeur **rate** est définie sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddde7-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="ddde7-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="ddde7-115">Examples</span></span>

<span data-ttu-id="ddde7-116">L’exemple suivant crée un élément BUTTON HTML qui utilise **Play** pour lire l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="ddde7-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="ddde7-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ddde7-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="ddde7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddde7-118">Requirements</span></span>



| <span data-ttu-id="ddde7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddde7-119">Requirement</span></span> | <span data-ttu-id="ddde7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddde7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddde7-121">Version</span><span class="sxs-lookup"><span data-stu-id="ddde7-121">Version</span></span><br/> | <span data-ttu-id="ddde7-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ddde7-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ddde7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ddde7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ddde7-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddde7-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddde7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddde7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddde7-126">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="ddde7-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





