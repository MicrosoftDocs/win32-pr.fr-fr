---
title: Network. downloadProgress
description: La propriété downloadProgress récupère le pourcentage de téléchargement effectué.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Lecteur Windows Media Network. downloadProgress
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539597"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="a1673-104">Network. downloadProgress</span><span class="sxs-lookup"><span data-stu-id="a1673-104">Network.downloadProgress</span></span>

<span data-ttu-id="a1673-105">La propriété **downloadProgress** récupère le pourcentage de téléchargement effectué.</span><span class="sxs-lookup"><span data-stu-id="a1673-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1673-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1673-106">Syntax</span></span>

<span data-ttu-id="a1673-107">*lecteur*. *réseau*. **downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="a1673-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a1673-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a1673-108">Possible Values</span></span>

<span data-ttu-id="a1673-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="a1673-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1673-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a1673-110">Remarks</span></span>

<span data-ttu-id="a1673-111">Lorsque le contrôle du lecteur Windows Media est connecté à un fichier multimédia qui peut être lu et téléchargé en même temps, la propriété **downloadProgress** retourne le pourcentage du fichier total téléchargé.</span><span class="sxs-lookup"><span data-stu-id="a1673-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="a1673-112">Cette fonctionnalité n’est actuellement prise en charge que sur les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="a1673-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="a1673-113">Les formats de fichier suivants peuvent être téléchargés et lus simultanément :</span><span class="sxs-lookup"><span data-stu-id="a1673-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="a1673-114">ASF (Advanced Systems Format)</span><span class="sxs-lookup"><span data-stu-id="a1673-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="a1673-115">Audio Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="a1673-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="a1673-116">Vidéo Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="a1673-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="a1673-117">MP3</span><span class="sxs-lookup"><span data-stu-id="a1673-117">MP3</span></span>
-   <span data-ttu-id="a1673-118">MPEG4</span><span class="sxs-lookup"><span data-stu-id="a1673-118">MPEG</span></span>
-   <span data-ttu-id="a1673-119">WAV</span><span class="sxs-lookup"><span data-stu-id="a1673-119">WAV</span></span>
-   <span data-ttu-id="a1673-120">Certains fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="a1673-120">Some AVI files</span></span>

<span data-ttu-id="a1673-121">Utilisez le *lecteur*. Événement de **mise en mémoire tampon** pour déterminer à quel moment le téléchargement commence et se termine.</span><span class="sxs-lookup"><span data-stu-id="a1673-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="a1673-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1673-122">Examples</span></span>

<span data-ttu-id="a1673-123">L’exemple JScript suivant utilise le *réseau*. **downloadProgress** pour afficher le pourcentage de téléchargement effectué.</span><span class="sxs-lookup"><span data-stu-id="a1673-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="a1673-124">Les informations s’affichent dans une balise DIV HTML créée avec ID = « DP ».</span><span class="sxs-lookup"><span data-stu-id="a1673-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="a1673-125">L’exemple utilise un minuteur avec un intervalle de 1 seconde pour mettre à jour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a1673-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="a1673-126">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a1673-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a1673-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1673-127">Requirements</span></span>



| <span data-ttu-id="a1673-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1673-128">Requirement</span></span> | <span data-ttu-id="a1673-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1673-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1673-130">Version</span><span class="sxs-lookup"><span data-stu-id="a1673-130">Version</span></span><br/> | <span data-ttu-id="a1673-131">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a1673-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1673-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a1673-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1673-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1673-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1673-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1673-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1673-135">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="a1673-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a1673-136">**Player. Buffering (événement)**</span><span class="sxs-lookup"><span data-stu-id="a1673-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





