---
title: Événement Player. OpenStateChange
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Événement OpenStateChange lecteur Windows Media
- Événement OpenStateChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540392"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="14922-107">Événement Player. OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="14922-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="14922-108">L’événement **OpenStateChange** se produit lorsque la propriété **openState** change de valeur.</span><span class="sxs-lookup"><span data-stu-id="14922-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="14922-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14922-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="14922-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14922-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14922-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="14922-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="14922-112">**Nombre** (**long**) spécifiant le nouvel état ouvert.</span><span class="sxs-lookup"><span data-stu-id="14922-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="14922-113">Consultez [openState](player-openstate.md) pour obtenir une table de valeurs.</span><span class="sxs-lookup"><span data-stu-id="14922-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14922-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14922-114">Return value</span></span>

<span data-ttu-id="14922-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14922-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14922-116">Notes</span><span class="sxs-lookup"><span data-stu-id="14922-116">Remarks</span></span>

<span data-ttu-id="14922-117">Le lecteur Windows Media peut passer par plusieurs États ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple Rechercher le serveur, se connecter au serveur et enfin ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="14922-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="14922-118">Cet événement est déclenché chaque fois que l’état ouvert change.</span><span class="sxs-lookup"><span data-stu-id="14922-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="14922-119">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="14922-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="14922-120">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="14922-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="14922-121">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="14922-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="14922-122">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="14922-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="14922-123">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="14922-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="14922-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14922-124">Requirements</span></span>



| <span data-ttu-id="14922-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14922-125">Requirement</span></span> | <span data-ttu-id="14922-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="14922-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14922-127">Version</span><span class="sxs-lookup"><span data-stu-id="14922-127">Version</span></span><br/> | <span data-ttu-id="14922-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="14922-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="14922-129">DLL</span><span class="sxs-lookup"><span data-stu-id="14922-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="14922-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14922-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14922-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14922-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14922-132">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="14922-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="14922-133">**Player. openState**</span><span class="sxs-lookup"><span data-stu-id="14922-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





