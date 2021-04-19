---
title: Réseau. cadence
description: La propriété cadencer récupère la fréquence d’images vidéo actuelle en images par centaines de secondes. Par exemple, une valeur de 2998 indique 29,98 images par seconde.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network. cadencer le lecteur Windows Media
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536048"
---
# <a name="networkframerate"></a><span data-ttu-id="4397e-105">Réseau. cadence</span><span class="sxs-lookup"><span data-stu-id="4397e-105">Network.frameRate</span></span>

<span data-ttu-id="4397e-106">La propriété **cadencer** récupère la fréquence d’images vidéo actuelle en images par centaines de secondes.</span><span class="sxs-lookup"><span data-stu-id="4397e-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="4397e-107">Par exemple, une valeur de 2998 indique 29,98 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4397e-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="4397e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4397e-108">Syntax</span></span>

<span data-ttu-id="4397e-109">*lecteur*. *réseau*. **fréquence** d’images</span><span class="sxs-lookup"><span data-stu-id="4397e-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4397e-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4397e-110">Possible Values</span></span>

<span data-ttu-id="4397e-111">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="4397e-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="4397e-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="4397e-112">Examples</span></span>

<span data-ttu-id="4397e-113">L’exemple JScript suivant utilise le *réseau*. **cadence** d’images pour afficher la fréquence d’images actuelle.</span><span class="sxs-lookup"><span data-stu-id="4397e-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="4397e-114">Les informations sont affichées dans une balise DIV HTML créée avec ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="4397e-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="4397e-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4397e-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="4397e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4397e-116">Requirements</span></span>



| <span data-ttu-id="4397e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4397e-117">Requirement</span></span> | <span data-ttu-id="4397e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4397e-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4397e-119">Version</span><span class="sxs-lookup"><span data-stu-id="4397e-119">Version</span></span><br/> | <span data-ttu-id="4397e-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4397e-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4397e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4397e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="4397e-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4397e-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4397e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4397e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4397e-124">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="4397e-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4397e-125">**Network. encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="4397e-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





