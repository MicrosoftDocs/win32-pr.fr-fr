---
title: Événement Player. PlayStateChange
description: L’événement PlayStateChange se produit lorsqu’une modification est apportée à la propriété lecture.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Événement PlayStateChange lecteur Windows Media
- Événement PlayStateChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542273"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="9fc5c-106">Événement Player. PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="9fc5c-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="9fc5c-107">L’événement **PlayStateChange** se produit lorsqu’une modification est apportée à la propriété **lecture** .</span><span class="sxs-lookup"><span data-stu-id="9fc5c-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc5c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fc5c-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="9fc5c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fc5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc5c-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="9fc5c-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc5c-111">Nombre (**long**) qui spécifie le nouveau **lecture**.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="9fc5c-112">Pour obtenir un tableau des valeurs possibles, consultez [lecture](player-playstate.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc5c-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc5c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fc5c-113">Return value</span></span>

<span data-ttu-id="9fc5c-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc5c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9fc5c-115">Remarks</span></span>

<span data-ttu-id="9fc5c-116">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9fc5c-117">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="9fc5c-118">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="9fc5c-119">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="9fc5c-120">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="9fc5c-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="9fc5c-121">Examples</span></span>

<span data-ttu-id="9fc5c-122">L’exemple suivant montre un gestionnaire d’événements pour le *lecteur*. événement **playStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9fc5c-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="9fc5c-123">Un élément de texte HTML, nommé « myText », affiche le nouvel état de lecture.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="9fc5c-124">L’objet Player a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9fc5c-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="9fc5c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fc5c-125">Requirements</span></span>



| <span data-ttu-id="9fc5c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fc5c-126">Requirement</span></span> | <span data-ttu-id="9fc5c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc5c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc5c-128">Version</span><span class="sxs-lookup"><span data-stu-id="9fc5c-128">Version</span></span><br/> | <span data-ttu-id="9fc5c-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9fc5c-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9fc5c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc5c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="9fc5c-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc5c-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc5c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fc5c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc5c-133">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="9fc5c-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="9fc5c-134">**Player. lecture**</span><span class="sxs-lookup"><span data-stu-id="9fc5c-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





