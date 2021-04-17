---
title: IPropertyFilter LogicOperator, propriété (WdsSharedIDL. h)
description: Opérateur logique à utiliser lors de l’application d’un filtre.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Propriétés LogicOperator héritées fonctionnalités de l’environnement Windows
- Propriété LogicOperator fonctionnalités de l’environnement Windows héritées, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités d’environnement Windows héritées, propriété LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466946"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="39479-106">IPropertyFilter :: LogicOperator, propriété</span><span class="sxs-lookup"><span data-stu-id="39479-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="39479-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39479-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="39479-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="39479-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="39479-109">Opérateur logique à utiliser lors de l’application d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="39479-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="39479-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="39479-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39479-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39479-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="39479-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="39479-112">Property value</span></span>

<span data-ttu-id="39479-113">Définit le type d’opérateur logique.</span><span class="sxs-lookup"><span data-stu-id="39479-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="39479-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39479-114">Requirements</span></span>



| <span data-ttu-id="39479-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39479-115">Requirement</span></span> | <span data-ttu-id="39479-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="39479-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="39479-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39479-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39479-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39479-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39479-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39479-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39479-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39479-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39479-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="39479-121">Redistributable</span></span><br/>          | <span data-ttu-id="39479-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="39479-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="39479-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="39479-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39479-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39479-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





