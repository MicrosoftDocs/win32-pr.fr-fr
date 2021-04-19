---
title: Network. bufferingCount
description: La propriété bufferingCount récupère le nombre de fois que la mise en mémoire tampon s’est produite lors de la lecture du clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Lecteur Windows Media Network. bufferingCount
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542281"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="2efde-104">Network. bufferingCount</span><span class="sxs-lookup"><span data-stu-id="2efde-104">Network.bufferingCount</span></span>

<span data-ttu-id="2efde-105">La propriété **bufferingCount** récupère le nombre de fois que la mise en mémoire tampon s’est produite lors de la lecture du clip.</span><span class="sxs-lookup"><span data-stu-id="2efde-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="2efde-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2efde-106">Syntax</span></span>

<span data-ttu-id="2efde-107">*lecteur*. *réseau*. **bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="2efde-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2efde-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2efde-108">Possible Values</span></span>

<span data-ttu-id="2efde-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="2efde-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2efde-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2efde-110">Remarks</span></span>

<span data-ttu-id="2efde-111">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2efde-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="2efde-112">Elle n’est pas réinitialisée si la lecture est suspendue.</span><span class="sxs-lookup"><span data-stu-id="2efde-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="2efde-113">La mise en mémoire tampon s’applique uniquement au contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="2efde-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="2efde-114">Cette propriété retourne des informations valides uniquement au moment de l’exécution lorsque le *joueur*. La propriété **URL** est définie.</span><span class="sxs-lookup"><span data-stu-id="2efde-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="2efde-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="2efde-115">Examples</span></span>

<span data-ttu-id="2efde-116">L’exemple JScript suivant utilise le *réseau*. **bufferingCount** pour afficher le nombre de fois que la mise en mémoire tampon se produit pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="2efde-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="2efde-117">Les informations sont affichées dans une balise DIV HTML créée avec ID = "CB".</span><span class="sxs-lookup"><span data-stu-id="2efde-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="2efde-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2efde-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2efde-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2efde-119">Requirements</span></span>



| <span data-ttu-id="2efde-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2efde-120">Requirement</span></span> | <span data-ttu-id="2efde-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2efde-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2efde-122">Version</span><span class="sxs-lookup"><span data-stu-id="2efde-122">Version</span></span><br/> | <span data-ttu-id="2efde-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2efde-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2efde-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2efde-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2efde-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2efde-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2efde-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2efde-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efde-127">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="2efde-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="2efde-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="2efde-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





