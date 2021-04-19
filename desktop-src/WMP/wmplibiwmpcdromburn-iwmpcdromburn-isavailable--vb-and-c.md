---
title: IWMPCdromBurn isAvailable, méthode
description: La méthode isAvailable fournit des informations sur le lecteur de CD et le support.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- méthode isAvailable lecteur Windows Media
- méthode isAvailable lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, isAvailable, méthode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537761"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="47e9f-106">IWMPCdromBurn :: isAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="47e9f-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="47e9f-107">La méthode **isAvailable** fournit des informations sur le lecteur de CD et le support.</span><span class="sxs-lookup"><span data-stu-id="47e9f-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e9f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47e9f-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="47e9f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47e9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e9f-110">*bstrItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e9f-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e9f-111">**System. String** qui contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="47e9f-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="47e9f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="47e9f-112">Value</span></span> | <span data-ttu-id="47e9f-113">Description</span><span class="sxs-lookup"><span data-stu-id="47e9f-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="47e9f-114">Écrire</span><span class="sxs-lookup"><span data-stu-id="47e9f-114">Burn</span></span>  | <span data-ttu-id="47e9f-115">Le lecteur est un graveur de CD.</span><span class="sxs-lookup"><span data-stu-id="47e9f-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="47e9f-116">ROM</span><span class="sxs-lookup"><span data-stu-id="47e9f-116">Disc</span></span>  | <span data-ttu-id="47e9f-117">Un CD est présent dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="47e9f-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="47e9f-118">Effacer</span><span class="sxs-lookup"><span data-stu-id="47e9f-118">Erase</span></span> | <span data-ttu-id="47e9f-119">Le CD peut être effacé.</span><span class="sxs-lookup"><span data-stu-id="47e9f-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="47e9f-120">Write</span><span class="sxs-lookup"><span data-stu-id="47e9f-120">Write</span></span> | <span data-ttu-id="47e9f-121">Le CD peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="47e9f-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e9f-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47e9f-122">Return value</span></span>

<span data-ttu-id="47e9f-123">**System. Boolean** qui indique le résultat.</span><span class="sxs-lookup"><span data-stu-id="47e9f-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e9f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47e9f-124">Requirements</span></span>



| <span data-ttu-id="47e9f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47e9f-125">Requirement</span></span> | <span data-ttu-id="47e9f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="47e9f-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e9f-127">Version</span><span class="sxs-lookup"><span data-stu-id="47e9f-127">Version</span></span><br/>   | <span data-ttu-id="47e9f-128">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="47e9f-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="47e9f-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="47e9f-129">Namespace</span></span><br/> | <span data-ttu-id="47e9f-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="47e9f-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="47e9f-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="47e9f-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="47e9f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="47e9f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e9f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47e9f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e9f-134">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="47e9f-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





