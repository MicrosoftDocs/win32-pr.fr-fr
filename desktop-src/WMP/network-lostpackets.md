---
title: Network. lostPackets
description: La propriété lostPackets récupère le nombre de paquets perdus.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Lecteur Windows Media Network. lostPackets
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525261"
---
# <a name="networklostpackets"></a><span data-ttu-id="9b86b-104">Network. lostPackets</span><span class="sxs-lookup"><span data-stu-id="9b86b-104">Network.lostPackets</span></span>

<span data-ttu-id="9b86b-105">La propriété **lostPackets** récupère le nombre de paquets perdus.</span><span class="sxs-lookup"><span data-stu-id="9b86b-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b86b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b86b-106">Syntax</span></span>

<span data-ttu-id="9b86b-107">*lecteur*. *réseau*. **lostPackets**</span><span class="sxs-lookup"><span data-stu-id="9b86b-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9b86b-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9b86b-108">Possible Values</span></span>

<span data-ttu-id="9b86b-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="9b86b-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b86b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9b86b-110">Remarks</span></span>

<span data-ttu-id="9b86b-111">Cette propriété n’est valide que pour la diffusion multimédia en continu et sera égale à zéro lors de l’utilisation du protocole HTTP, qui est sans perte.</span><span class="sxs-lookup"><span data-stu-id="9b86b-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="9b86b-112">Les paquets peuvent être perdus pour plusieurs raisons, telles que le type et la qualité de la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="9b86b-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="9b86b-113">Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9b86b-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="9b86b-114">Elle n’est pas réinitialisée si la lecture est suspendue et redémarrée.</span><span class="sxs-lookup"><span data-stu-id="9b86b-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="9b86b-115">Cette propriété retourne des informations valides uniquement au moment de l’exécution, et uniquement si le *joueur*. La propriété **URL** est définie.</span><span class="sxs-lookup"><span data-stu-id="9b86b-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="9b86b-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b86b-116">Examples</span></span>

<span data-ttu-id="9b86b-117">L’exemple JScript suivant utilise le *réseau*. **lostPackets** pour afficher le nombre total de paquets perdus lors de la lecture lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="9b86b-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="9b86b-118">Les informations s’affichent dans une balise DIV HTML créée avec ID = « LP ».</span><span class="sxs-lookup"><span data-stu-id="9b86b-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="9b86b-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9b86b-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="9b86b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b86b-120">Requirements</span></span>



| <span data-ttu-id="9b86b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b86b-121">Requirement</span></span> | <span data-ttu-id="9b86b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b86b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b86b-123">Version</span><span class="sxs-lookup"><span data-stu-id="9b86b-123">Version</span></span><br/> | <span data-ttu-id="9b86b-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9b86b-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9b86b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9b86b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b86b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b86b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b86b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b86b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b86b-128">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="9b86b-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="9b86b-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="9b86b-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





