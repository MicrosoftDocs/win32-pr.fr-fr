---
description: Supprime un objet IContextNode de cette collection.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'IContextNodes :: RemoveContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514632"
---
# <a name="icontextnodesremovecontextnode-method"></a><span data-ttu-id="186b6-103">IContextNodes :: RemoveContextNode, méthode</span><span class="sxs-lookup"><span data-stu-id="186b6-103">IContextNodes::RemoveContextNode method</span></span>

<span data-ttu-id="186b6-104">Supprime un objet [**IContextNode**](icontextnode.md) de cette collection.</span><span class="sxs-lookup"><span data-stu-id="186b6-104">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="186b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="186b6-105">Syntax</span></span>


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="186b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="186b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186b6-107">*pContextNode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="186b6-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186b6-108">Objet [**IContextNode**](icontextnode.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="186b6-108">The [**IContextNode**](icontextnode.md) object to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186b6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="186b6-109">Return value</span></span>

<span data-ttu-id="186b6-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="186b6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="186b6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="186b6-111">Requirements</span></span>



| <span data-ttu-id="186b6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="186b6-112">Requirement</span></span> | <span data-ttu-id="186b6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="186b6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186b6-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="186b6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="186b6-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="186b6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="186b6-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="186b6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="186b6-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="186b6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="186b6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="186b6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="186b6-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="186b6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="186b6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="186b6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="186b6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="186b6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="186b6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="186b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186b6-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="186b6-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="186b6-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="186b6-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




