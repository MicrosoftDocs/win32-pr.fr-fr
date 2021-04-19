---
title: Réseau. bande passante
description: La propriété bandWidth récupère la bande passante actuelle du clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Réseau. bande passante Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520844"
---
# <a name="networkbandwidth"></a><span data-ttu-id="d089c-104">Réseau. bande passante</span><span class="sxs-lookup"><span data-stu-id="d089c-104">Network.bandWidth</span></span>

<span data-ttu-id="d089c-105">La propriété **Bandwidth** récupère la bande passante actuelle du clip.</span><span class="sxs-lookup"><span data-stu-id="d089c-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="d089c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d089c-106">Syntax</span></span>

<span data-ttu-id="d089c-107">*lecteur*. *réseau*. **bande passante**</span><span class="sxs-lookup"><span data-stu-id="d089c-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d089c-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d089c-108">Possible Values</span></span>

<span data-ttu-id="d089c-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="d089c-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="d089c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d089c-110">Remarks</span></span>

<span data-ttu-id="d089c-111">Cette propriété retourne zéro si le *joueur*. La propriété **URL** n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="d089c-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="d089c-112">Cette propriété n’est valide que pour la diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="d089c-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="d089c-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="d089c-113">Examples</span></span>

<span data-ttu-id="d089c-114">L’exemple Microsoft JScript suivant utilise le *réseau*. **bande passante** pour afficher la bande passante du support actuel.</span><span class="sxs-lookup"><span data-stu-id="d089c-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="d089c-115">Les informations s’affichent dans une balise DIV HTML créée avec ID = « BW ».</span><span class="sxs-lookup"><span data-stu-id="d089c-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="d089c-116">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d089c-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="d089c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d089c-117">Requirements</span></span>



| <span data-ttu-id="d089c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d089c-118">Requirement</span></span> | <span data-ttu-id="d089c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d089c-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d089c-120">Version</span><span class="sxs-lookup"><span data-stu-id="d089c-120">Version</span></span><br/> | <span data-ttu-id="d089c-121">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d089c-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d089c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d089c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d089c-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d089c-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d089c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d089c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d089c-125">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="d089c-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="d089c-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="d089c-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





