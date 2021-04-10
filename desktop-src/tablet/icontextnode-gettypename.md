---
description: Récupère un nom de type explicite de ce IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'IContextNode :: GetTypeName, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113375"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="2fefd-103">IContextNode :: GetTypeName, méthode</span><span class="sxs-lookup"><span data-stu-id="2fefd-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="2fefd-104">Récupère un nom de type explicite de ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2fefd-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fefd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fefd-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="2fefd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fefd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fefd-107">*pbstrContextNodeType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2fefd-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fefd-108">Nom de type explicite de ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2fefd-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fefd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fefd-109">Return value</span></span>

<span data-ttu-id="2fefd-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2fefd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fefd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2fefd-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2fefd-112">Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) sur \* *pbstrContextNodeType* lorsque vous n’avez plus besoin d’utiliser la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2fefd-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="2fefd-113">Par exemple, cette méthode définit *pbstrContextNodeType* sur « InkWordNode » pour un nœud de mot Ink (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="2fefd-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fefd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fefd-114">Requirements</span></span>



| <span data-ttu-id="2fefd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fefd-115">Requirement</span></span> | <span data-ttu-id="2fefd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fefd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fefd-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fefd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2fefd-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fefd-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2fefd-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fefd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2fefd-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fefd-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2fefd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fefd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fefd-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2fefd-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2fefd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2fefd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fefd-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fefd-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2fefd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fefd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fefd-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2fefd-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2fefd-127">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="2fefd-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="2fefd-128">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="2fefd-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="2fefd-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="2fefd-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

