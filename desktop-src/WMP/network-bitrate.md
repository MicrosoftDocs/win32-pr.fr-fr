---
title: Réseau. débit binaire
description: La propriété de débit binaire récupère la vitesse de transmission actuelle en cours de réception.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Lecteur Windows Media réseau. débit binaire
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523937"
---
# <a name="networkbitrate"></a><span data-ttu-id="be1b9-104">Réseau. débit binaire</span><span class="sxs-lookup"><span data-stu-id="be1b9-104">Network.bitRate</span></span>

<span data-ttu-id="be1b9-105">La propriété de **débit** binaire récupère la vitesse de transmission actuelle en cours de réception.</span><span class="sxs-lookup"><span data-stu-id="be1b9-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="be1b9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be1b9-106">Syntax</span></span>

<span data-ttu-id="be1b9-107">*lecteur*. *réseau*. **débit binaire**</span><span class="sxs-lookup"><span data-stu-id="be1b9-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="be1b9-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="be1b9-108">Possible Values</span></span>

<span data-ttu-id="be1b9-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="be1b9-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="be1b9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="be1b9-110">Remarks</span></span>

<span data-ttu-id="be1b9-111">Cette valeur est une combinaison des vitesses de transmission des flux vidéo et audio actuels.</span><span class="sxs-lookup"><span data-stu-id="be1b9-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="be1b9-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="be1b9-112">Examples</span></span>

<span data-ttu-id="be1b9-113">L’exemple JScript suivant utilise le *réseau*. **débit** binaire pour afficher la vitesse de transmission actuelle du média.</span><span class="sxs-lookup"><span data-stu-id="be1b9-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="be1b9-114">Les informations sont affichées dans une balise DIV HTML créée avec ID = "BR".</span><span class="sxs-lookup"><span data-stu-id="be1b9-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="be1b9-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="be1b9-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="be1b9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be1b9-116">Requirements</span></span>



| <span data-ttu-id="be1b9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be1b9-117">Requirement</span></span> | <span data-ttu-id="be1b9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="be1b9-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be1b9-119">Version</span><span class="sxs-lookup"><span data-stu-id="be1b9-119">Version</span></span><br/> | <span data-ttu-id="be1b9-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="be1b9-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="be1b9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="be1b9-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="be1b9-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be1b9-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be1b9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be1b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be1b9-124">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="be1b9-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





