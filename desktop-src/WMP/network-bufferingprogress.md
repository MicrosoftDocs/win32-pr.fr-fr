---
title: Network. bufferingProgress
description: La propriété bufferingProgress récupère le pourcentage d’achèvement de la mise en mémoire tampon.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Lecteur Windows Media Network. bufferingProgress
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532799"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="15106-104">Network. bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="15106-104">Network.bufferingProgress</span></span>

<span data-ttu-id="15106-105">La propriété **bufferingProgress** récupère le pourcentage d’achèvement de la mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="15106-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="15106-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15106-106">Syntax</span></span>

<span data-ttu-id="15106-107">*lecteur*. *réseau*. **bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="15106-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="15106-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="15106-108">Possible Values</span></span>

<span data-ttu-id="15106-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="15106-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="15106-110">Notes</span><span class="sxs-lookup"><span data-stu-id="15106-110">Remarks</span></span>

<span data-ttu-id="15106-111">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="15106-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="15106-112">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="15106-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="15106-113">La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="15106-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="15106-114">Cette propriété retourne des informations valides uniquement au moment de l’exécution, lorsque le *joueur*. La propriété **URL** est définie.</span><span class="sxs-lookup"><span data-stu-id="15106-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="15106-115">Utilisez l’événement *Player*. \* \* \* \* Buffering \* \* \* \* pour déterminer à quel moment la mise en mémoire tampon démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="15106-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="15106-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="15106-116">Examples</span></span>

<span data-ttu-id="15106-117">L’exemple JScript suivant utilise le *réseau*. **bufferingProgress** pour afficher le pourcentage de la mise en mémoire tampon terminée.</span><span class="sxs-lookup"><span data-stu-id="15106-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="15106-118">Les informations s’affichent dans une balise DIV HTML créée avec ID = « BP ».</span><span class="sxs-lookup"><span data-stu-id="15106-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="15106-119">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="15106-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="15106-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="15106-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="15106-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15106-121">Requirements</span></span>



| <span data-ttu-id="15106-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15106-122">Requirement</span></span> | <span data-ttu-id="15106-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="15106-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15106-124">Version</span><span class="sxs-lookup"><span data-stu-id="15106-124">Version</span></span><br/> | <span data-ttu-id="15106-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="15106-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="15106-126">DLL</span><span class="sxs-lookup"><span data-stu-id="15106-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="15106-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15106-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15106-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15106-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15106-129">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="15106-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="15106-130">**Player. Buffering (événement)**</span><span class="sxs-lookup"><span data-stu-id="15106-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="15106-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="15106-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





