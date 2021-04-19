---
description: Réorganise un objet IContextNode enfant spécifié à l’index spécifié.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'IContextNode :: MoveSubNodeToPosition, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514195"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="b4178-103">IContextNode :: MoveSubNodeToPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="b4178-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="b4178-104">Réorganise un objet [**IContextNode**](icontextnode.md) enfant spécifié à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4178-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4178-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4178-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b4178-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4178-107">*pSubnodeToMove* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4178-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4178-108">Objet [**IContextNode**](icontextnode.md) à déplacer.</span><span class="sxs-lookup"><span data-stu-id="b4178-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="b4178-109">*ulNewIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4178-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4178-110">Index de la nouvelle position du sous-nœud.</span><span class="sxs-lookup"><span data-stu-id="b4178-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4178-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4178-111">Return value</span></span>

<span data-ttu-id="b4178-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b4178-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4178-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b4178-113">Remarks</span></span>

<span data-ttu-id="b4178-114">Retourne **E \_ INVALIDARG** si *pSubnodeToMove* n’est pas un nœud enfant de ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="b4178-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4178-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4178-115">Requirements</span></span>



| <span data-ttu-id="b4178-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4178-116">Requirement</span></span> | <span data-ttu-id="b4178-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4178-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4178-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4178-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4178-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4178-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4178-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4178-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4178-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4178-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4178-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4178-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4178-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4178-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4178-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b4178-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4178-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4178-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4178-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4178-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4178-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b4178-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b4178-128">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="b4178-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="b4178-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b4178-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




