---
title: Network. receptionQuality
description: La propriété receptionQuality récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Lecteur Windows Media Network. receptionQuality
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526815"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="7e012-104">Network. receptionQuality</span><span class="sxs-lookup"><span data-stu-id="7e012-104">Network.receptionQuality</span></span>

<span data-ttu-id="7e012-105">La propriété **receptionQuality** récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="7e012-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e012-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e012-106">Syntax</span></span>

<span data-ttu-id="7e012-107">*lecteur*. *réseau*. **receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="7e012-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7e012-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7e012-108">Possible Values</span></span>

<span data-ttu-id="7e012-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="7e012-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e012-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7e012-110">Remarks</span></span>

<span data-ttu-id="7e012-111">Le nombre de paquets reçus, perdus et récupérés pendant la diffusion en continu est analysé une fois par seconde.</span><span class="sxs-lookup"><span data-stu-id="7e012-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="7e012-112">**receptionQuality** est le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.</span><span class="sxs-lookup"><span data-stu-id="7e012-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="7e012-113">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="7e012-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="7e012-114">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="7e012-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="7e012-115">Cette propriété retourne des informations valides uniquement au moment de l’exécution et uniquement si le *joueur*. La propriété **URL** est également définie.</span><span class="sxs-lookup"><span data-stu-id="7e012-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="7e012-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="7e012-116">Examples</span></span>

<span data-ttu-id="7e012-117">L’exemple JScript suivant utilise le *réseau*. **receptionQuality** pour afficher le pourcentage de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="7e012-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="7e012-118">Les informations sont affichées dans une balise DIV HTML créée avec ID = "RQ".</span><span class="sxs-lookup"><span data-stu-id="7e012-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="7e012-119">L’exemple utilise un minuteur avec un intervalle de 30 secondes pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7e012-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="7e012-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7e012-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="7e012-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e012-121">Requirements</span></span>



| <span data-ttu-id="7e012-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e012-122">Requirement</span></span> | <span data-ttu-id="7e012-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e012-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e012-124">Version</span><span class="sxs-lookup"><span data-stu-id="7e012-124">Version</span></span><br/> | <span data-ttu-id="7e012-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7e012-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7e012-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7e012-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e012-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e012-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e012-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e012-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e012-129">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="7e012-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="7e012-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7e012-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





