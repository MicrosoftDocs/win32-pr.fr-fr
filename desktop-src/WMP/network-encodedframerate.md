---
title: Network. encodedFrameRate
description: La propriété encodedFrameRate récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu en images par seconde.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Lecteur Windows Media Network. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521626"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="ccda3-104">Network. encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="ccda3-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="ccda3-105">La propriété **encodedFrameRate** récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="ccda3-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccda3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccda3-106">Syntax</span></span>

<span data-ttu-id="ccda3-107">*lecteur*. *réseau*. **encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="ccda3-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ccda3-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ccda3-108">Possible Values</span></span>

<span data-ttu-id="ccda3-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="ccda3-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="ccda3-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="ccda3-110">Examples</span></span>

<span data-ttu-id="ccda3-111">L’exemple JScript suivant utilise le *réseau*. **encodedFrameRate** pour afficher la fréquence d’images spécifiée lors de l’encodage du fichier.</span><span class="sxs-lookup"><span data-stu-id="ccda3-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="ccda3-112">Les informations sont affichées dans une balise DIV HTML créée avec ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="ccda3-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="ccda3-113">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ccda3-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="ccda3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccda3-114">Requirements</span></span>



| <span data-ttu-id="ccda3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccda3-115">Requirement</span></span> | <span data-ttu-id="ccda3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccda3-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccda3-117">Version</span><span class="sxs-lookup"><span data-stu-id="ccda3-117">Version</span></span><br/> | <span data-ttu-id="ccda3-118">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ccda3-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ccda3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ccda3-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ccda3-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccda3-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccda3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccda3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccda3-122">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="ccda3-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="ccda3-123">**Réseau. cadence**</span><span class="sxs-lookup"><span data-stu-id="ccda3-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





