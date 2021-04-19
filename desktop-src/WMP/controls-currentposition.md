---
title: Controls. currentPosition
description: La propriété currentPosition spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. currentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543297"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="5dde5-104">Controls. currentPosition</span><span class="sxs-lookup"><span data-stu-id="5dde5-104">Controls.currentPosition</span></span>

<span data-ttu-id="5dde5-105">La propriété **CurrentPosition** spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.</span><span class="sxs-lookup"><span data-stu-id="5dde5-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="5dde5-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5dde5-106">Possible Values</span></span>

<span data-ttu-id="5dde5-107">Cette propriété est un **nombre** en lecture/écriture (**double**).</span><span class="sxs-lookup"><span data-stu-id="5dde5-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="5dde5-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="5dde5-108">Examples</span></span>

<span data-ttu-id="5dde5-109">L’exemple suivant utilise **CurrentPosition** pour rechercher une position fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5dde5-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="5dde5-110">Un élément bouton HTML est créé pour exécuter le code JScript.</span><span class="sxs-lookup"><span data-stu-id="5dde5-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="5dde5-111">Un élément d’entrée de texte HTML, nommé setPosition, a été créé pour accepter une valeur, en secondes, de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5dde5-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="5dde5-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5dde5-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="5dde5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dde5-113">Requirements</span></span>



| <span data-ttu-id="5dde5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dde5-114">Requirement</span></span> | <span data-ttu-id="5dde5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dde5-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5dde5-116">Version</span><span class="sxs-lookup"><span data-stu-id="5dde5-116">Version</span></span><br/> | <span data-ttu-id="5dde5-117">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5dde5-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5dde5-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5dde5-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5dde5-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dde5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dde5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dde5-121">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="5dde5-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





