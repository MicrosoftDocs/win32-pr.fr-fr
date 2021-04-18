---
title: Controls. Next, méthode
description: La méthode suivante définit l’élément actuel à l’élément suivant dans la sélection.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- méthode suivante lecteur Windows Media
- méthode Next lecteur Windows Media, classe Controls
- Controls, classe Windows Media Player, méthode Next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529019"
---
# <a name="controlsnext-method"></a><span data-ttu-id="f2354-106">Controls. Next, méthode</span><span class="sxs-lookup"><span data-stu-id="f2354-106">Controls.next method</span></span>

<span data-ttu-id="f2354-107">La méthode **suivante** définit l’élément actuel à l’élément suivant dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="f2354-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2354-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2354-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="f2354-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2354-109">Parameters</span></span>

<span data-ttu-id="f2354-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2354-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2354-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2354-111">Return value</span></span>

<span data-ttu-id="f2354-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2354-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2354-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2354-113">Remarks</span></span>

<span data-ttu-id="f2354-114">Si la sélection se trouve sur la dernière entrée **lors de** l’appel de la méthode, la première entrée de la sélection devient la dernière.</span><span class="sxs-lookup"><span data-stu-id="f2354-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="f2354-115">Pour les sélections côté serveur, cette méthode passe à l’élément suivant dans la sélection côté serveur, et non à la sélection du client.</span><span class="sxs-lookup"><span data-stu-id="f2354-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="f2354-116">Lors de la lecture d’un DVD, cette méthode passe au chapitre logique suivant dans la séquence de lecture, qui peut ne pas être le chapitre suivant de la sélection.</span><span class="sxs-lookup"><span data-stu-id="f2354-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="f2354-117">Quand le DVD est toujours en cours d’exécution, cette méthode passe à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="f2354-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="f2354-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f2354-118">Examples</span></span>

<span data-ttu-id="f2354-119">L’exemple suivant crée un élément bouton HTML qui utilise **Next** pour passer à l’élément suivant dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="f2354-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="f2354-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f2354-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="f2354-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2354-121">Requirements</span></span>



| <span data-ttu-id="f2354-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2354-122">Requirement</span></span> | <span data-ttu-id="f2354-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2354-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2354-124">Version</span><span class="sxs-lookup"><span data-stu-id="f2354-124">Version</span></span><br/> | <span data-ttu-id="f2354-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f2354-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f2354-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f2354-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2354-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2354-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2354-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2354-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2354-129">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="f2354-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f2354-130">**Contrôles. Previous**</span><span class="sxs-lookup"><span data-stu-id="f2354-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="f2354-131">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="f2354-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





