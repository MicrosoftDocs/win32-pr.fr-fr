---
title: IWMPControls2 Step, méthode
description: La méthode STEP fait passer l’élément multimédia vidéo actuel au frame suivant ou au frame précédent et fige la lecture.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- méthode STEP du lecteur Windows Media
- Step, méthode lecteur Windows Media, interface IWMPControls2
- Interface IWMPControls2 lecteur Windows Media, méthode STEP
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541363"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="bc3a5-106">IWMPControls2 :: Step, méthode</span><span class="sxs-lookup"><span data-stu-id="bc3a5-106">IWMPControls2::step method</span></span>

<span data-ttu-id="bc3a5-107">La méthode **Step** fait passer l’élément multimédia vidéo actuel au frame suivant ou au frame précédent et fige la lecture.</span><span class="sxs-lookup"><span data-stu-id="bc3a5-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3a5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc3a5-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="bc3a5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc3a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc3a5-110">*lStep* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc3a5-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc3a5-111">Valeur **System. Int32** indiquant le nombre de frames à exécuter avant le gel.</span><span class="sxs-lookup"><span data-stu-id="bc3a5-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="bc3a5-112">Doit avoir la valeur 1 ou-1.</span><span class="sxs-lookup"><span data-stu-id="bc3a5-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc3a5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc3a5-113">Return value</span></span>

<span data-ttu-id="bc3a5-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bc3a5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3a5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bc3a5-115">Remarks</span></span>

<span data-ttu-id="bc3a5-116">Cette méthode ne prend actuellement en charge que les paramètres 1 ou-1, de sorte que vous ne pouvez exécuter qu’un seul Frame à la fois.</span><span class="sxs-lookup"><span data-stu-id="bc3a5-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3a5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc3a5-117">Requirements</span></span>



| <span data-ttu-id="bc3a5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc3a5-118">Requirement</span></span> | <span data-ttu-id="bc3a5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc3a5-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3a5-120">Version</span><span class="sxs-lookup"><span data-stu-id="bc3a5-120">Version</span></span><br/>   | <span data-ttu-id="bc3a5-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bc3a5-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bc3a5-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bc3a5-122">Namespace</span></span><br/> | <span data-ttu-id="bc3a5-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc3a5-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bc3a5-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="bc3a5-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc3a5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bc3a5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3a5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc3a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3a5-127">**Interface IWMPControls2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bc3a5-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc3a5-128">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bc3a5-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





