---
title: Network. sourceProtocol
description: La propriété sourceProtocol récupère le protocole source utilisé pour recevoir des données.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Lecteur Windows Media Network. sourceProtocol
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535917"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="9bcd4-104">Network. sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="9bcd4-104">Network.sourceProtocol</span></span>

<span data-ttu-id="9bcd4-105">La propriété **sourceProtocol** récupère le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcd4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bcd4-106">Syntax</span></span>

<span data-ttu-id="9bcd4-107">*lecteur*. *réseau*. **sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="9bcd4-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9bcd4-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9bcd4-108">Possible Values</span></span>

<span data-ttu-id="9bcd4-109">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcd4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9bcd4-110">Remarks</span></span>

<span data-ttu-id="9bcd4-111">Cette propriété a la valeur "" (chaîne vide) lors de la diffusion de contenu multimédia à partir d’un CD ou d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="9bcd4-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="9bcd4-112">Examples</span></span>

<span data-ttu-id="9bcd4-113">L’exemple JScript suivant utilise le *réseau*. **sourceProtocol** pour afficher le protocole source utilisé pour recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="9bcd4-114">Les informations s’affichent dans une balise DIV HTML créée avec ID = « SP ».</span><span class="sxs-lookup"><span data-stu-id="9bcd4-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="9bcd4-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9bcd4-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="9bcd4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bcd4-116">Requirements</span></span>



| <span data-ttu-id="9bcd4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bcd4-117">Requirement</span></span> | <span data-ttu-id="9bcd4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bcd4-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcd4-119">Version</span><span class="sxs-lookup"><span data-stu-id="9bcd4-119">Version</span></span><br/> | <span data-ttu-id="9bcd4-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9bcd4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9bcd4-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bcd4-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bcd4-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcd4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bcd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcd4-124">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="9bcd4-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





