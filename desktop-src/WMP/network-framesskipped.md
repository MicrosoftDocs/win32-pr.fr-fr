---
title: Network. framesSkipped
description: La propriété framesSkipped récupère le nombre total de trames ignorées lors de la lecture.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Lecteur Windows Media Network. framesSkipped
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536047"
---
# <a name="networkframesskipped"></a><span data-ttu-id="68a67-104">Network. framesSkipped</span><span class="sxs-lookup"><span data-stu-id="68a67-104">Network.framesSkipped</span></span>

<span data-ttu-id="68a67-105">La propriété **framesSkipped** récupère le nombre total de trames ignorées lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="68a67-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a67-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68a67-106">Syntax</span></span>

<span data-ttu-id="68a67-107">*lecteur*. *réseau*. **framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="68a67-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="68a67-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="68a67-108">Possible Values</span></span>

<span data-ttu-id="68a67-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="68a67-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="68a67-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="68a67-110">Examples</span></span>

<span data-ttu-id="68a67-111">L’exemple JScript suivant utilise le *réseau*. **framesSkipped** pour afficher le nombre total de trames ignorées lors de la lecture lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="68a67-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="68a67-112">Les informations s’affichent dans une balise DIV HTML créée avec ID = « FS ».</span><span class="sxs-lookup"><span data-stu-id="68a67-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="68a67-113">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="68a67-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="68a67-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68a67-114">Requirements</span></span>



| <span data-ttu-id="68a67-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68a67-115">Requirement</span></span> | <span data-ttu-id="68a67-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="68a67-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68a67-117">Version</span><span class="sxs-lookup"><span data-stu-id="68a67-117">Version</span></span><br/> | <span data-ttu-id="68a67-118">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68a67-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="68a67-119">DLL</span><span class="sxs-lookup"><span data-stu-id="68a67-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="68a67-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a67-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a67-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68a67-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a67-122">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="68a67-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





