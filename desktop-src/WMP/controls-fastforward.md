---
title: Controls. fastForward, méthode
description: La méthode fastForward démarre la lecture rapide de l’élément multimédia dans le sens avant. | Controls. fastForward, méthode
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- méthode fastForward lecteur Windows Media
- méthode fastForward lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523976"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="b3fdf-107">Controls. fastForward, méthode</span><span class="sxs-lookup"><span data-stu-id="b3fdf-107">Controls.fastForward method</span></span>

<span data-ttu-id="b3fdf-108">La méthode **fastForward** démarre la lecture rapide de l’élément multimédia dans le sens avant.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fdf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3fdf-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="b3fdf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3fdf-110">Parameters</span></span>

<span data-ttu-id="b3fdf-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3fdf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3fdf-112">Return value</span></span>

<span data-ttu-id="b3fdf-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fdf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b3fdf-114">Remarks</span></span>

<span data-ttu-id="b3fdf-115">La méthode **fastForward** lit le clip à cinq fois la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="b3fdf-116">L’appel de **fastForward** modifie les *paramètres*. propriété **rate** sur 5,0.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="b3fdf-117">Si le **taux** est modifié par la suite ou si la **lecture** ou l' **arrêt** est appelé, le lecteur Windows Media arrête le transfert rapide.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="b3fdf-118">La méthode **fastForward** ne fonctionne pas pour les diffusions en direct et certains types de média.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="b3fdf-119">Pour déterminer si vous pouvez avancer rapidement dans un clip, appelez **isAvailable**(« Fastforward »).</span><span class="sxs-lookup"><span data-stu-id="b3fdf-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="b3fdf-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="b3fdf-120">Examples</span></span>

<span data-ttu-id="b3fdf-121">L’exemple suivant crée un élément BUTTON HTML qui utilise **fastForward** pour démarrer la lecture rapide de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="b3fdf-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b3fdf-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="b3fdf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3fdf-123">Requirements</span></span>



| <span data-ttu-id="b3fdf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3fdf-124">Requirement</span></span> | <span data-ttu-id="b3fdf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3fdf-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fdf-126">Version</span><span class="sxs-lookup"><span data-stu-id="b3fdf-126">Version</span></span><br/> | <span data-ttu-id="b3fdf-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b3fdf-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3fdf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b3fdf-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3fdf-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3fdf-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3fdf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3fdf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fdf-131">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="b3fdf-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="b3fdf-132">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="b3fdf-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="b3fdf-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="b3fdf-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="b3fdf-134">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="b3fdf-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="b3fdf-135">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="b3fdf-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





