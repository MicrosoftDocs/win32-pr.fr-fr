---
description: Crée un objet IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'IInkAnalyzer :: CreateContextNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515670"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="223e8-103">IInkAnalyzer :: CreateContextNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="223e8-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="223e8-104">Crée un objet [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="223e8-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="223e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="223e8-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="223e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="223e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223e8-107">*ppContextNodes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="223e8-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="223e8-108">Pointeur vers l’objet [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="223e8-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223e8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="223e8-109">Return value</span></span>

<span data-ttu-id="223e8-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="223e8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="223e8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="223e8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="223e8-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodes* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="223e8-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="223e8-113">Utilisez cette méthode pour créer une collection [**IContextNodes**](icontextnodes.md) vide associée au [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="223e8-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="223e8-114">La nouvelle collection **IContextNodes** ne fait pas partie de l’arborescence de contexte de l’objet **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="223e8-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="223e8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="223e8-115">Requirements</span></span>



| <span data-ttu-id="223e8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="223e8-116">Requirement</span></span> | <span data-ttu-id="223e8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="223e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="223e8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="223e8-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="223e8-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="223e8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="223e8-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="223e8-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="223e8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="223e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="223e8-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="223e8-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="223e8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="223e8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="223e8-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="223e8-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="223e8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="223e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223e8-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="223e8-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="223e8-128">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="223e8-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="223e8-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="223e8-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

