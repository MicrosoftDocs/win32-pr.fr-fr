---
description: Récupère le IContextLink à l’index spécifié.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'IContextLinks :: GetContextLink, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113394"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="f005d-103">IContextLinks :: GetContextLink, méthode</span><span class="sxs-lookup"><span data-stu-id="f005d-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="f005d-104">Récupère le [**IContextLink**](icontextlink.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f005d-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f005d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f005d-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="f005d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f005d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f005d-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f005d-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f005d-108">Index de base zéro de l’objet [**IContextLink**](icontextlink.md) à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f005d-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="f005d-109">*ppContextLink* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f005d-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f005d-110">Pointeur vers l’objet [**IContextLink**](icontextlink.md) à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f005d-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f005d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f005d-111">Return value</span></span>

<span data-ttu-id="f005d-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f005d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f005d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f005d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f005d-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLink* lorsque vous n’avez plus besoin d’utiliser le lien de contexte.</span><span class="sxs-lookup"><span data-stu-id="f005d-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f005d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f005d-115">Requirements</span></span>



| <span data-ttu-id="f005d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f005d-116">Requirement</span></span> | <span data-ttu-id="f005d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f005d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f005d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f005d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f005d-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f005d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f005d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f005d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f005d-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f005d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f005d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f005d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f005d-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f005d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f005d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f005d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f005d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f005d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f005d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f005d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f005d-127">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="f005d-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="f005d-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f005d-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f005d-129">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="f005d-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

