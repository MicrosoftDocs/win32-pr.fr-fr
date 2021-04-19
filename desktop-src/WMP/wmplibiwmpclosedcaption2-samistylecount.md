---
title: IWMPClosedCaption2 propriété SAMIStyleCount
description: La propriété SAMIStyleCount obtient le nombre de styles pris en charge par le fichier SAMI actuel.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propriété SAMIStyleCount lecteur Windows Media
- Propriété SAMIStyleCount lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, propriété SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521729"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="fc576-106">IWMPClosedCaption2 :: SAMIStyleCount, propriété</span><span class="sxs-lookup"><span data-stu-id="fc576-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="fc576-107">La propriété **SAMIStyleCount** obtient le nombre de styles pris en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="fc576-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc576-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc576-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="fc576-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fc576-109">Property value</span></span>

<span data-ttu-id="fc576-110">**System. Int32** qui correspond au nombre de styles.</span><span class="sxs-lookup"><span data-stu-id="fc576-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc576-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fc576-111">Remarks</span></span>

<span data-ttu-id="fc576-112">Cette propriété retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="fc576-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc576-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc576-113">Requirements</span></span>



| <span data-ttu-id="fc576-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc576-114">Requirement</span></span> | <span data-ttu-id="fc576-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc576-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc576-116">Version</span><span class="sxs-lookup"><span data-stu-id="fc576-116">Version</span></span><br/>   | <span data-ttu-id="fc576-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fc576-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fc576-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fc576-118">Namespace</span></span><br/> | <span data-ttu-id="fc576-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fc576-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fc576-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="fc576-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fc576-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fc576-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc576-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc576-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc576-123">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="fc576-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="fc576-124">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fc576-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fc576-125">**IWMPClosedCaption. SAMIStyle (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fc576-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fc576-126">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fc576-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fc576-127">**IWMPClosedCaption2. getSAMIStyleName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fc576-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





