---
title: Événement Player. MediaChange
description: L’événement MediaChange se produit lorsqu’un élément multimédia change. | Événement Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Événement MediaChange lecteur Windows Media
- Événement MediaChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533431"
---
# <a name="playermediachange-event"></a><span data-ttu-id="f76aa-107">Événement Player. MediaChange</span><span class="sxs-lookup"><span data-stu-id="f76aa-107">Player.MediaChange event</span></span>

<span data-ttu-id="f76aa-108">L’événement **MediaChange** se produit lorsqu’un élément multimédia change.</span><span class="sxs-lookup"><span data-stu-id="f76aa-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76aa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f76aa-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="f76aa-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f76aa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76aa-111">*Item*</span><span class="sxs-lookup"><span data-stu-id="f76aa-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="f76aa-112">Objet **multimédia** représentant l’élément qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="f76aa-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76aa-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f76aa-113">Return value</span></span>

<span data-ttu-id="f76aa-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f76aa-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f76aa-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f76aa-115">Remarks</span></span>

<span data-ttu-id="f76aa-116">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="f76aa-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="f76aa-117">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="f76aa-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="f76aa-118">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f76aa-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f76aa-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="f76aa-119">Examples</span></span>

<span data-ttu-id="f76aa-120">L’exemple JScript suivant utilise un élément HTML DIV, nommé MediaName, pour afficher le nom de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="f76aa-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="f76aa-121">Le code met à jour le texte de la balise DIV avec chaque occurrence de l’événement **mediaChange** .</span><span class="sxs-lookup"><span data-stu-id="f76aa-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="f76aa-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f76aa-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f76aa-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f76aa-123">Requirements</span></span>



| <span data-ttu-id="f76aa-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f76aa-124">Requirement</span></span> | <span data-ttu-id="f76aa-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f76aa-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f76aa-126">Version</span><span class="sxs-lookup"><span data-stu-id="f76aa-126">Version</span></span><br/> | <span data-ttu-id="f76aa-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f76aa-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f76aa-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f76aa-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f76aa-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f76aa-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76aa-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f76aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76aa-131">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="f76aa-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





