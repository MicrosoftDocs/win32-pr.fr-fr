---
title: IWMPCdromBurn propriété burnProgress
description: La propriété burnProgress obtient la progression de la gravure de CD comme pourcentage d’achèvement.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- propriété burnProgress lecteur Windows Media
- propriété burnProgress lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, propriété burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541584"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="886c7-106">IWMPCdromBurn :: burnProgress, propriété</span><span class="sxs-lookup"><span data-stu-id="886c7-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="886c7-107">La propriété **burnProgress** obtient la progression de la gravure de CD comme pourcentage d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="886c7-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="886c7-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="886c7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="886c7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="886c7-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="886c7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="886c7-110">Property value</span></span>

<span data-ttu-id="886c7-111">**System. Int32** qui est la valeur de progression.</span><span class="sxs-lookup"><span data-stu-id="886c7-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="886c7-112">Les valeurs de progression sont comprises entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="886c7-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="886c7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="886c7-113">Remarks</span></span>

<span data-ttu-id="886c7-114">La valeur de progression représente le pourcentage terminé de l’ensemble du processus de gravure, y compris les opérations intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="886c7-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="886c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="886c7-115">Requirements</span></span>



| <span data-ttu-id="886c7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="886c7-116">Requirement</span></span> | <span data-ttu-id="886c7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="886c7-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="886c7-118">Version</span><span class="sxs-lookup"><span data-stu-id="886c7-118">Version</span></span><br/>   | <span data-ttu-id="886c7-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="886c7-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="886c7-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="886c7-120">Namespace</span></span><br/> | <span data-ttu-id="886c7-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="886c7-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="886c7-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="886c7-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="886c7-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="886c7-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="886c7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="886c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886c7-125">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="886c7-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





