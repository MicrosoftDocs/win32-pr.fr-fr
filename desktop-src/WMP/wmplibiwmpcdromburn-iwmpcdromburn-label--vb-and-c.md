---
title: Propriété d’étiquette IWMPCdromBurn
description: La propriété étiquette obtient la chaîne de nom du volume du CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propriété d’étiquette lecteur Windows Media
- propriété étiquette lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, propriété label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542633"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="66146-106">IWMPCdromBurn :: label, propriété</span><span class="sxs-lookup"><span data-stu-id="66146-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="66146-107">La propriété *étiquette* obtient la chaîne de nom du volume du CD.</span><span class="sxs-lookup"><span data-stu-id="66146-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="66146-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="66146-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66146-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66146-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="66146-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="66146-110">Property value</span></span>

<span data-ttu-id="66146-111">**System. String** qui est la chaîne de nom de volume.</span><span class="sxs-lookup"><span data-stu-id="66146-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="66146-112">Notes</span><span class="sxs-lookup"><span data-stu-id="66146-112">Remarks</span></span>

<span data-ttu-id="66146-113">En raison de la façon dont les étiquettes de CD sont stockées, l’étiquette du CD peut être plus petite que la longueur de la chaîne de nom de volume spécifiée.</span><span class="sxs-lookup"><span data-stu-id="66146-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="66146-114">Si la chaîne dépasse la longueur maximale d’une étiquette de CD, le texte est tronqué.</span><span class="sxs-lookup"><span data-stu-id="66146-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="66146-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66146-115">Requirements</span></span>



| <span data-ttu-id="66146-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66146-116">Requirement</span></span> | <span data-ttu-id="66146-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="66146-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66146-118">Version</span><span class="sxs-lookup"><span data-stu-id="66146-118">Version</span></span><br/>   | <span data-ttu-id="66146-119">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="66146-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="66146-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66146-120">Namespace</span></span><br/> | <span data-ttu-id="66146-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="66146-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="66146-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="66146-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="66146-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="66146-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66146-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66146-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66146-125">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="66146-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





