---
title: Controls. fastReverse, méthode
description: La méthode fastReverse démarre une analyse rapide de l’élément multimédia dans le sens inverse.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- méthode fastReverse lecteur Windows Media
- méthode fastReverse lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525438"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="857e4-106">Controls. fastReverse, méthode</span><span class="sxs-lookup"><span data-stu-id="857e4-106">Controls.fastReverse method</span></span>

<span data-ttu-id="857e4-107">La méthode **fastReverse** démarre une analyse rapide de l’élément multimédia dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="857e4-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="857e4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="857e4-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="857e4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="857e4-109">Parameters</span></span>

<span data-ttu-id="857e4-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="857e4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="857e4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="857e4-111">Return value</span></span>

<span data-ttu-id="857e4-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="857e4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="857e4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="857e4-113">Remarks</span></span>

<span data-ttu-id="857e4-114">La méthode **fastReverse** analyse le clip en sens inverse à cinq fois la vitesse normale, en affichant uniquement les images clés s’il s’agit d’un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="857e4-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="857e4-115">L’appel de **fastReverse** modifie les *paramètres*. propriété **rate** sur 5,0.</span><span class="sxs-lookup"><span data-stu-id="857e4-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="857e4-116">Si la **fréquence** est modifiée par la suite, ou si la **lecture** ou l' **arrêt** est appelé, le lecteur Windows Media arrête rapidement l’opération inverse.</span><span class="sxs-lookup"><span data-stu-id="857e4-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="857e4-117">Si l’élément fait partie d’une sélection, **fastReverse** s’arrête au début de la piste actuelle. Par exemple, si Track 3 se trouve dans **fastReverse**, lorsque le début de la piste 3 est atteint, le lecteur Windows Media ne passe pas à Track 2.</span><span class="sxs-lookup"><span data-stu-id="857e4-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="857e4-118">Le nombre de lecture n’est pas incrémenté lors de l’appel de **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="857e4-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="857e4-119">Si vous appelez **fastForward** alors que **fastReverse** est en vigueur, **fastReverse** sera arrêté et **fastForward** démarrera.</span><span class="sxs-lookup"><span data-stu-id="857e4-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="857e4-120">Cette méthode ne fonctionne pas pour les diffusions en direct et certains types de média.</span><span class="sxs-lookup"><span data-stu-id="857e4-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="857e4-121">Pour déterminer si vous pouvez utiliser l’inverse rapide dans un clip, appelez **isAvailable**(« FastReverse »).</span><span class="sxs-lookup"><span data-stu-id="857e4-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="857e4-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="857e4-122">Examples</span></span>

<span data-ttu-id="857e4-123">L’exemple suivant crée un élément BUTTON HTML qui utilise **fastReverse** pour démarrer la lecture rapide et inversée de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="857e4-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="857e4-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="857e4-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="857e4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="857e4-125">Requirements</span></span>



| <span data-ttu-id="857e4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="857e4-126">Requirement</span></span> | <span data-ttu-id="857e4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="857e4-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="857e4-128">Version</span><span class="sxs-lookup"><span data-stu-id="857e4-128">Version</span></span><br/> | <span data-ttu-id="857e4-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="857e4-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="857e4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="857e4-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="857e4-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857e4-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857e4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="857e4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857e4-133">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="857e4-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="857e4-134">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="857e4-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="857e4-135">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="857e4-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="857e4-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="857e4-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="857e4-137">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="857e4-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="857e4-138">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="857e4-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





