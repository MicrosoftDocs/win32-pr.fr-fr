---
title: IWMPNetwork propriété maxBandwidth
description: La propriété maxBandwidth obtient ou définit la bande passante maximale autorisée.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- propriété maxBandwidth lecteur Windows Media
- propriété maxBandwidth lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530991"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="f224c-106">IWMPNetwork :: maxBandwidth, propriété</span><span class="sxs-lookup"><span data-stu-id="f224c-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="f224c-107">La propriété **maxBandwidth** obtient ou définit la bande passante maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="f224c-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="f224c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f224c-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f224c-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f224c-109">Property value</span></span>

<span data-ttu-id="f224c-110">**System. Int32** qui correspond à la bande passante maximale.</span><span class="sxs-lookup"><span data-stu-id="f224c-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="f224c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f224c-111">Remarks</span></span>

<span data-ttu-id="f224c-112">Cette propriété n’a pas de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f224c-112">This property does not have a default value.</span></span> <span data-ttu-id="f224c-113">La valeur peut être spécifiée pendant la lecture du lecteur Windows Media, mais la modification ne prendra effet qu’après la libération de l’élément multimédia en cours en ouvrant une autre ou en appelant **AxWindowsMediaPlayer. Close**.</span><span class="sxs-lookup"><span data-stu-id="f224c-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="f224c-114">Le lecteur Windows Media tente d’obtenir la bande passante la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="f224c-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="f224c-115">Aucune réduction intentionnelle de la bande passante ne se produit, sauf si cette valeur est définie.</span><span class="sxs-lookup"><span data-stu-id="f224c-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="f224c-116">Ce paramètre est utile pour réduire la quantité de bande passante utilisée, en particulier dans le cas d’un flux de la vitesse de transmission multiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="f224c-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="f224c-117">Un flux MBR contient plusieurs flux avec différentes vitesses de transmission.</span><span class="sxs-lookup"><span data-stu-id="f224c-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="f224c-118">Dans certains cas, il peut être souhaitable d’utiliser un flux avec une vitesse de transmission inférieure à celle requise par le client.</span><span class="sxs-lookup"><span data-stu-id="f224c-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="f224c-119">Dans ce cas, la spécification d’une vitesse de transmission inférieure avec la propriété **IWMPNetwork. maxBandwidth** sélectionnera un flux de vitesse de transmission inférieur.</span><span class="sxs-lookup"><span data-stu-id="f224c-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="f224c-120">Par exemple, un flux de données MBR peut inclure des flux encodés à 20 kilobits par seconde (Kbits/s), 37 Kbits/s et 200 kbit/s.</span><span class="sxs-lookup"><span data-stu-id="f224c-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="f224c-121">L’utilisation de **IWMPNetwork. maxBandwidth** pour spécifier une vitesse de transmission de 50 000 (50 kbps) sélectionnera le flux de 37 Kbits/s au lieu du flux de 200 Kbits/s.</span><span class="sxs-lookup"><span data-stu-id="f224c-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="f224c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f224c-122">Requirements</span></span>



| <span data-ttu-id="f224c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f224c-123">Requirement</span></span> | <span data-ttu-id="f224c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f224c-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f224c-125">Version</span><span class="sxs-lookup"><span data-stu-id="f224c-125">Version</span></span><br/>   | <span data-ttu-id="f224c-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f224c-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f224c-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f224c-127">Namespace</span></span><br/> | <span data-ttu-id="f224c-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f224c-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f224c-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="f224c-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f224c-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f224c-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f224c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f224c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f224c-132">**AxWindowsMediaPlayer. Close (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f224c-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="f224c-133">**Interface IWMPNetwork (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="f224c-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





