---
title: Network. receivedPackets
description: La propriété receivedPackets récupère le nombre de paquets reçus.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Lecteur Windows Media Network. receivedPackets
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535329"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="85381-104">Network. receivedPackets</span><span class="sxs-lookup"><span data-stu-id="85381-104">Network.receivedPackets</span></span>

<span data-ttu-id="85381-105">La propriété **receivedPackets** récupère le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="85381-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="85381-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85381-106">Syntax</span></span>

<span data-ttu-id="85381-107">*lecteur*. *réseau*. **receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="85381-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="85381-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="85381-108">Possible Values</span></span>

<span data-ttu-id="85381-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="85381-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="85381-110">Notes</span><span class="sxs-lookup"><span data-stu-id="85381-110">Remarks</span></span>

<span data-ttu-id="85381-111">Chaque fois que la lecture du clip est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="85381-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="85381-112">Elle n’est pas réinitialisée si la lecture du fichier est suspendue.</span><span class="sxs-lookup"><span data-stu-id="85381-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="85381-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="85381-113">Examples</span></span>

<span data-ttu-id="85381-114">L’exemple JScript suivant utilise le *réseau*. **receivedPackets** pour afficher le nombre de paquets reçus.</span><span class="sxs-lookup"><span data-stu-id="85381-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="85381-115">Les informations sont affichées dans une balise DIV HTML créée avec l’ID = « RP ».</span><span class="sxs-lookup"><span data-stu-id="85381-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="85381-116">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="85381-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="85381-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="85381-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="85381-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85381-118">Requirements</span></span>



| <span data-ttu-id="85381-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85381-119">Requirement</span></span> | <span data-ttu-id="85381-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="85381-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85381-121">Version</span><span class="sxs-lookup"><span data-stu-id="85381-121">Version</span></span><br/> | <span data-ttu-id="85381-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85381-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="85381-123">DLL</span><span class="sxs-lookup"><span data-stu-id="85381-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="85381-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85381-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85381-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85381-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85381-126">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="85381-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





