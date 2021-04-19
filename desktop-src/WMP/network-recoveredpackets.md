---
title: Network. recoveredPackets
description: La propriété recoveredPackets récupère le nombre de paquets récupérés.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Lecteur Windows Media Network. recoveredPackets
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542606"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="cda7e-104">Network. recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="cda7e-104">Network.recoveredPackets</span></span>

<span data-ttu-id="cda7e-105">La propriété **recoveredPackets** récupère le nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="cda7e-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda7e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cda7e-106">Syntax</span></span>

<span data-ttu-id="cda7e-107">*lecteur*. *réseau*. **recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="cda7e-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="cda7e-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="cda7e-108">Possible Values</span></span>

<span data-ttu-id="cda7e-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="cda7e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="cda7e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cda7e-110">Remarks</span></span>

<span data-ttu-id="cda7e-111">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="cda7e-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="cda7e-112">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="cda7e-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="cda7e-113">Cette propriété retourne des informations valides uniquement au moment de l’exécution et uniquement si le *joueur*. La propriété **URL** est également définie.</span><span class="sxs-lookup"><span data-stu-id="cda7e-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="cda7e-114">Elle sera égale à zéro lors de l’utilisation du protocole HTTP, qui est sans perte.</span><span class="sxs-lookup"><span data-stu-id="cda7e-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="cda7e-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="cda7e-115">Examples</span></span>

<span data-ttu-id="cda7e-116">L’exemple JScript suivant utilise le *réseau*. **recoveredPackets** pour afficher le nombre de paquets récupérés.</span><span class="sxs-lookup"><span data-stu-id="cda7e-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="cda7e-117">Les informations s’affichent dans une balise DIV HTML créée avec ID = « PR ».</span><span class="sxs-lookup"><span data-stu-id="cda7e-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="cda7e-118">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="cda7e-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="cda7e-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cda7e-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="cda7e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cda7e-120">Requirements</span></span>



| <span data-ttu-id="cda7e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cda7e-121">Requirement</span></span> | <span data-ttu-id="cda7e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cda7e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cda7e-123">Version</span><span class="sxs-lookup"><span data-stu-id="cda7e-123">Version</span></span><br/> | <span data-ttu-id="cda7e-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cda7e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cda7e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cda7e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cda7e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda7e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda7e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda7e-128">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="cda7e-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="cda7e-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="cda7e-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





