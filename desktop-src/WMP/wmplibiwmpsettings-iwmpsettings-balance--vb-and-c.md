---
title: Propriété IWMPSettings balance
description: La propriété balance obtient ou définit le solde stéréo actuel.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- propriété balance Windows Media Player
- propriété solde lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété d’équilibrage
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529920"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="2cc0e-106">IWMPSettings :: balance, propriété</span><span class="sxs-lookup"><span data-stu-id="2cc0e-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="2cc0e-107">La propriété **balance** obtient ou définit le solde stéréo actuel.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cc0e-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2cc0e-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2cc0e-109">Property value</span></span>

<span data-ttu-id="2cc0e-110">**System. Int32** qui est la valeur de l’équilibre.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="2cc0e-111">Cette valeur peut être comprise entre 100 et 100.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="2cc0e-112">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc0e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2cc0e-113">Remarks</span></span>

<span data-ttu-id="2cc0e-114">La valeur zéro indique que le son est lu à un volume égal sur les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="2cc0e-115">Une valeur de 100 indique que l’audio est lu uniquement sur le canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="2cc0e-116">Une valeur de 100 indique que l’audio est lu uniquement sur le canal approprié.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc0e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cc0e-117">Requirements</span></span>



| <span data-ttu-id="2cc0e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cc0e-118">Requirement</span></span> | <span data-ttu-id="2cc0e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cc0e-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc0e-120">Version</span><span class="sxs-lookup"><span data-stu-id="2cc0e-120">Version</span></span><br/>   | <span data-ttu-id="2cc0e-121">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2cc0e-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="2cc0e-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2cc0e-122">Namespace</span></span><br/> | <span data-ttu-id="2cc0e-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2cc0e-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2cc0e-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="2cc0e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2cc0e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2cc0e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc0e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cc0e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc0e-127">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2cc0e-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





