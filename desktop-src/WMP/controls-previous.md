---
title: Controls. Previous, méthode
description: La méthode précédente définit l’élément actuel à l’élément précédent dans la sélection.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- méthode précédente lecteur Windows Media
- méthode Previous lecteur Windows Media, classe de contrôles
- Controls, classe Windows Media Player, méthode Previous
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530995"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="bcb54-106">Controls. Previous, méthode</span><span class="sxs-lookup"><span data-stu-id="bcb54-106">Controls.previous method</span></span>

<span data-ttu-id="bcb54-107">La méthode **précédente** définit l’élément actuel à l’élément précédent dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="bcb54-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb54-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcb54-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="bcb54-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcb54-109">Parameters</span></span>

<span data-ttu-id="bcb54-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bcb54-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcb54-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcb54-111">Return value</span></span>

<span data-ttu-id="bcb54-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bcb54-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb54-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bcb54-113">Remarks</span></span>

<span data-ttu-id="bcb54-114">Si la sélection se trouve sur la première entrée lors de l’appel de la méthode **précédente** , la dernière entrée de la sélection deviendra celle en cours.</span><span class="sxs-lookup"><span data-stu-id="bcb54-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="bcb54-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="bcb54-115">Examples</span></span>

<span data-ttu-id="bcb54-116">L’exemple suivant crée un élément BUTTON HTML qui utilise **Previous** pour accéder à l’élément précédent dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="bcb54-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="bcb54-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bcb54-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="bcb54-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcb54-118">Requirements</span></span>



| <span data-ttu-id="bcb54-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcb54-119">Requirement</span></span> | <span data-ttu-id="bcb54-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcb54-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb54-121">Version</span><span class="sxs-lookup"><span data-stu-id="bcb54-121">Version</span></span><br/> | <span data-ttu-id="bcb54-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bcb54-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bcb54-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb54-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bcb54-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb54-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb54-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcb54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb54-126">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="bcb54-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="bcb54-127">**Contrôles. Next**</span><span class="sxs-lookup"><span data-stu-id="bcb54-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="bcb54-128">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="bcb54-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





