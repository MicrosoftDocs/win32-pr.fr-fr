---
description: Récupère le type de relation représenté par ce IContextLink.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'IContextLink :: GetContextLinkDirection, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201511"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="11e90-103">IContextLink :: GetContextLinkDirection, méthode</span><span class="sxs-lookup"><span data-stu-id="11e90-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="11e90-104">Récupère le type de relation représenté par ce [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="11e90-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11e90-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="11e90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e90-107">*pContextLinkDirection* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11e90-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11e90-108">Direction que ce [**IContextLink**](icontextlink.md) représente.</span><span class="sxs-lookup"><span data-stu-id="11e90-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e90-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11e90-109">Return value</span></span>

<span data-ttu-id="11e90-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="11e90-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11e90-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11e90-111">Requirements</span></span>



| <span data-ttu-id="11e90-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11e90-112">Requirement</span></span> | <span data-ttu-id="11e90-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="11e90-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e90-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11e90-114">Minimum supported client</span></span><br/> | <span data-ttu-id="11e90-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11e90-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11e90-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11e90-116">Minimum supported server</span></span><br/> | <span data-ttu-id="11e90-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="11e90-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="11e90-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="11e90-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e90-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11e90-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11e90-120">DLL</span><span class="sxs-lookup"><span data-stu-id="11e90-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e90-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e90-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="11e90-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11e90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e90-123">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="11e90-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="11e90-124">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="11e90-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="11e90-125">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="11e90-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




