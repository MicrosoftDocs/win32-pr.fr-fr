---
description: Récupère le nombre d’objets IContextNode contenus dans cette collection.
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'IContextNodes :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113367"
---
# <a name="icontextnodesgetcount-method"></a><span data-ttu-id="55cc0-103">IContextNodes :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="55cc0-103">IContextNodes::GetCount method</span></span>

<span data-ttu-id="55cc0-104">Récupère le nombre d’objets [**IContextNode**](icontextnode.md) contenus dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="55cc0-104">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="55cc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55cc0-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="55cc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55cc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55cc0-107">*pulCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="55cc0-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55cc0-108">Nombre d’objets [**IContextNode**](icontextnode.md) contenus dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="55cc0-108">The number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55cc0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55cc0-109">Return value</span></span>

<span data-ttu-id="55cc0-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="55cc0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55cc0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55cc0-111">Requirements</span></span>



| <span data-ttu-id="55cc0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55cc0-112">Requirement</span></span> | <span data-ttu-id="55cc0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="55cc0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cc0-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55cc0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="55cc0-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55cc0-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55cc0-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55cc0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="55cc0-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="55cc0-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55cc0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="55cc0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="55cc0-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55cc0-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55cc0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="55cc0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55cc0-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55cc0-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55cc0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55cc0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cc0-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="55cc0-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="55cc0-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="55cc0-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




