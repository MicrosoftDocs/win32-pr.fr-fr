---
title: Événement Player. CurrentItemChange
description: L’événement CurrentItemChange se produit lorsque Controls. currentItem change.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Événement CurrentItemChange lecteur Windows Media
- Événement CurrentItemChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542757"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="0e1ce-106">Événement Player. CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="0e1ce-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="0e1ce-107">L’événement **CurrentItemChange** se produit lorsque *contrôle*. modifications de **CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="0e1ce-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e1ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e1ce-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="0e1ce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e1ce-109">Parameters</span></span>

<span data-ttu-id="0e1ce-110">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0e1ce-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e1ce-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e1ce-111">Return value</span></span>

<span data-ttu-id="0e1ce-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0e1ce-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="0e1ce-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e1ce-113">Examples</span></span>

<span data-ttu-id="0e1ce-114">L’exemple JScript suivant montre un gestionnaire d’événements pour le *lecteur*. événement **currentItemChange** .</span><span class="sxs-lookup"><span data-stu-id="0e1ce-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="0e1ce-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0e1ce-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="0e1ce-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e1ce-116">Requirements</span></span>



| <span data-ttu-id="0e1ce-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e1ce-117">Requirement</span></span> | <span data-ttu-id="0e1ce-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e1ce-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e1ce-119">Version</span><span class="sxs-lookup"><span data-stu-id="0e1ce-119">Version</span></span><br/> | <span data-ttu-id="0e1ce-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0e1ce-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0e1ce-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0e1ce-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e1ce-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e1ce-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e1ce-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e1ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e1ce-124">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="0e1ce-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="0e1ce-125">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="0e1ce-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





