---
description: Récupère l’identificateur de trait pour le trait référencé par une valeur d’index dans l’objet IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'IContextNode :: GetStrokeId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751844"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="acabe-103">IContextNode :: GetStrokeId, méthode</span><span class="sxs-lookup"><span data-stu-id="acabe-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="acabe-104">Récupère l’identificateur de trait pour le trait référencé par une valeur d’index dans l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="acabe-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="acabe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acabe-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="acabe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acabe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acabe-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acabe-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acabe-108">Index du trait à retourner.</span><span class="sxs-lookup"><span data-stu-id="acabe-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="acabe-109">*plStrokeId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="acabe-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acabe-110">Identificateur de trait pour le trait référencé par le paramètre *ulIndex* dans l’objet [**IContextNode**](icontextnode.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="acabe-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acabe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acabe-111">Return value</span></span>

<span data-ttu-id="acabe-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="acabe-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acabe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acabe-113">Requirements</span></span>



| <span data-ttu-id="acabe-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acabe-114">Requirement</span></span> | <span data-ttu-id="acabe-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="acabe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acabe-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acabe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="acabe-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acabe-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="acabe-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acabe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="acabe-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="acabe-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="acabe-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="acabe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="acabe-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="acabe-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="acabe-122">DLL</span><span class="sxs-lookup"><span data-stu-id="acabe-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acabe-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acabe-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="acabe-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acabe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acabe-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="acabe-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="acabe-126">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="acabe-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="acabe-127">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="acabe-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="acabe-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="acabe-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




