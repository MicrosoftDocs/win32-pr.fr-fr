---
description: Supprime un IContextNode enfant.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: IContextNode ::D méthode eleteSubNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526530"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="9436e-103">IContextNode ::D méthode eleteSubNode</span><span class="sxs-lookup"><span data-stu-id="9436e-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="9436e-104">Supprime un [**IContextNode**](icontextnode.md)enfant.</span><span class="sxs-lookup"><span data-stu-id="9436e-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9436e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9436e-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="9436e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9436e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9436e-107">*pContextNodeToDelete* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9436e-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9436e-108">[**IContextNode**](icontextnode.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9436e-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9436e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9436e-109">Return value</span></span>

<span data-ttu-id="9436e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9436e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9436e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9436e-111">Remarks</span></span>

<span data-ttu-id="9436e-112">E \_ INVALIDARG est retourné si le paramètre *pContextNodeToDelete* n’est pas un enfant de cet objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9436e-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9436e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9436e-113">Requirements</span></span>



| <span data-ttu-id="9436e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9436e-114">Requirement</span></span> | <span data-ttu-id="9436e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9436e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9436e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9436e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9436e-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9436e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9436e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9436e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9436e-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9436e-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9436e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9436e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9436e-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9436e-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9436e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9436e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9436e-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9436e-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9436e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9436e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9436e-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9436e-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9436e-126">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="9436e-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="9436e-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="9436e-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




