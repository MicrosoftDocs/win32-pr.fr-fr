---
description: Ajoute un objet IContextNode à cette collection.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'IContextNodes :: AddContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113370"
---
# <a name="icontextnodesaddcontextnode-method"></a><span data-ttu-id="e830e-103">IContextNodes :: AddContextNode, méthode</span><span class="sxs-lookup"><span data-stu-id="e830e-103">IContextNodes::AddContextNode method</span></span>

<span data-ttu-id="e830e-104">Ajoute un objet [**IContextNode**](icontextnode.md) à cette collection.</span><span class="sxs-lookup"><span data-stu-id="e830e-104">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e830e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e830e-105">Syntax</span></span>


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="e830e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e830e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e830e-107">*pContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e830e-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e830e-108">Objet [**IContextNode**](icontextnode.md) à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e830e-108">The [**IContextNode**](icontextnode.md) object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e830e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e830e-109">Return value</span></span>

<span data-ttu-id="e830e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e830e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e830e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e830e-111">Requirements</span></span>



| <span data-ttu-id="e830e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e830e-112">Requirement</span></span> | <span data-ttu-id="e830e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e830e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e830e-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e830e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e830e-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e830e-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e830e-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e830e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e830e-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e830e-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e830e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e830e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e830e-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e830e-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e830e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e830e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e830e-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e830e-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e830e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e830e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e830e-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="e830e-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e830e-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e830e-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




