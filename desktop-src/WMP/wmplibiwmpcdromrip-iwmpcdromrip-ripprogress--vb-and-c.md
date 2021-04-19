---
title: IWMPCdromRip propriété ripProgress
description: La propriété ripProgress obtient la progression de l’extraction de CD comme pourcentage d’achèvement.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- propriété ripProgress lecteur Windows Media
- propriété ripProgress lecteur Windows Media, interface IWMPCdromRip
- Interface IWMPCdromRip lecteur Windows Media, propriété ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542627"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="29676-106">IWMPCdromRip :: ripProgress, propriété</span><span class="sxs-lookup"><span data-stu-id="29676-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="29676-107">La propriété **ripProgress** obtient la progression de l’extraction de CD comme pourcentage d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="29676-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="29676-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29676-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="29676-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="29676-109">Property value</span></span>

<span data-ttu-id="29676-110">**System. Int32** qui est la valeur de progression.</span><span class="sxs-lookup"><span data-stu-id="29676-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="29676-111">Les valeurs de progression sont comprises entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="29676-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="29676-112">Notes</span><span class="sxs-lookup"><span data-stu-id="29676-112">Remarks</span></span>

<span data-ttu-id="29676-113">La valeur de progression représente le pourcentage terminé de l’ensemble du processus d’extraction.</span><span class="sxs-lookup"><span data-stu-id="29676-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="29676-114">Pour déterminer la progression d’une piste spécifique, utilisez [IWMPMedia. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) avec **RipProgress** comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="29676-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="29676-115">Pour récupérer l’index de la piste actuellement extraite, appelez IWMPPlaylist. getItemInfo avec « CurrentRipTrackIndex » comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="29676-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="29676-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29676-116">Requirements</span></span>



| <span data-ttu-id="29676-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29676-117">Requirement</span></span> | <span data-ttu-id="29676-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="29676-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29676-119">Version</span><span class="sxs-lookup"><span data-stu-id="29676-119">Version</span></span><br/>   | <span data-ttu-id="29676-120">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="29676-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="29676-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29676-121">Namespace</span></span><br/> | <span data-ttu-id="29676-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="29676-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="29676-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="29676-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="29676-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="29676-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29676-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29676-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29676-126">**Interface IWMPCdromRip (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="29676-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29676-127">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="29676-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





