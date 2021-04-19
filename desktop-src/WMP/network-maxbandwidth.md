---
title: Network. maxBandwidth
description: La propriété maxBandwidth spécifie ou récupère la bande passante maximale autorisée.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Lecteur Windows Media Network. maxBandwidth
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539502"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="4709e-104">Network. maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="4709e-104">Network.maxBandwidth</span></span>

<span data-ttu-id="4709e-105">La propriété **maxBandwidth** spécifie ou récupère la bande passante maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="4709e-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="4709e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4709e-106">Syntax</span></span>

<span data-ttu-id="4709e-107">*lecteur*. *réseau*. **maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="4709e-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4709e-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4709e-108">Possible Values</span></span>

<span data-ttu-id="4709e-109">Cette propriété est un **nombre** en lecture/écriture (**long**).</span><span class="sxs-lookup"><span data-stu-id="4709e-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4709e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4709e-110">Remarks</span></span>

<span data-ttu-id="4709e-111">Cette propriété n’a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4709e-111">This property has no default value.</span></span> <span data-ttu-id="4709e-112">Sa valeur peut être spécifiée pendant la lecture du lecteur Windows Media, mais la modification ne prendra effet qu’après la libération de l’élément multimédia en cours en ouvrant un autre élément ou en appelant le *lecteur*. **Fermez**.</span><span class="sxs-lookup"><span data-stu-id="4709e-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="4709e-113">Le lecteur Windows Media tente d’obtenir la bande passante la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="4709e-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="4709e-114">Une réduction de la bande passante se produit uniquement dans le cas de la valeur définie.</span><span class="sxs-lookup"><span data-stu-id="4709e-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="4709e-115">Ce paramètre est utile pour réduire la quantité de bande passante utilisée, en particulier dans le cas d’un flux de la vitesse de transmission multiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="4709e-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="4709e-116">Un flux MBR contient plusieurs flux avec différentes vitesses de transmission.</span><span class="sxs-lookup"><span data-stu-id="4709e-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="4709e-117">Dans certains cas, il peut être souhaitable d’utiliser un flux avec une vitesse de transmission inférieure à celle requise par le client.</span><span class="sxs-lookup"><span data-stu-id="4709e-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="4709e-118">Dans ce cas, la définition de la propriété **maxBandwidth** sélectionnera un flux de vitesse de transmission inférieur.</span><span class="sxs-lookup"><span data-stu-id="4709e-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="4709e-119">Par exemple, un flux de données MBR peut inclure des flux encodés à 20 kilobits par seconde (Kbits/s), 37 Kbits/s et 200 kbit/s.</span><span class="sxs-lookup"><span data-stu-id="4709e-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="4709e-120">Si vous affectez à la propriété **maxBandwidth** la valeur 50 000 (50 Kbits/s), vous sélectionnez le flux de 37 kbps au lieu du flux de 200 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="4709e-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="4709e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4709e-121">Requirements</span></span>



| <span data-ttu-id="4709e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4709e-122">Requirement</span></span> | <span data-ttu-id="4709e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4709e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4709e-124">Version</span><span class="sxs-lookup"><span data-stu-id="4709e-124">Version</span></span><br/> | <span data-ttu-id="4709e-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4709e-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4709e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4709e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="4709e-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4709e-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4709e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4709e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4709e-129">**Objet réseau**</span><span class="sxs-lookup"><span data-stu-id="4709e-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4709e-130">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="4709e-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





