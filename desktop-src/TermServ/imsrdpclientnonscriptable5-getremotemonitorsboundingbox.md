---
title: IMsRdpClientNonScriptable5 propriété GetRemoteMonitorsBoundingBox
description: Spécifie le rectangle englobant du moniteur distant.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GetRemoteMonitorsBoundingBox
- Services Bureau à distance de la propriété GetRemoteMonitorsBoundingBox, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942417"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="7a2a5-106">IMsRdpClientNonScriptable5 :: GetRemoteMonitorsBoundingBox, propriété</span><span class="sxs-lookup"><span data-stu-id="7a2a5-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="7a2a5-107">Spécifie le rectangle englobant du moniteur distant.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="7a2a5-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2a5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a2a5-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="7a2a5-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7a2a5-110">Property value</span></span>

<span data-ttu-id="7a2a5-111">Reçoit le bord gauche du rectangle.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="7a2a5-112">Reçoit le bord supérieur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="7a2a5-113">Reçoit le bord droit du rectangle.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="7a2a5-114">Reçoit le bord inférieur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a2a5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a2a5-115">Remarks</span></span>

<span data-ttu-id="7a2a5-116">Toutes les coordonnées se trouvent dans des coordonnées d’écran virtuelles, qui sont relatives au coin supérieur gauche de l’écran principal.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="7a2a5-117">S’il ne s’agit pas du moniteur principal, une partie ou la totalité de ces valeurs peut être négative.</span><span class="sxs-lookup"><span data-stu-id="7a2a5-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2a5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a2a5-118">Requirements</span></span>



| <span data-ttu-id="7a2a5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a2a5-119">Requirement</span></span> | <span data-ttu-id="7a2a5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a2a5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2a5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2a5-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a2a5-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a2a5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2a5-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a2a5-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="7a2a5-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7a2a5-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a2a5-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a2a5-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7a2a5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a2a5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a2a5-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a2a5-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7a2a5-129">IID</span><span class="sxs-lookup"><span data-stu-id="7a2a5-129">IID</span></span><br/>                      | <span data-ttu-id="7a2a5-130">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="7a2a5-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a2a5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a2a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2a5-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7a2a5-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





