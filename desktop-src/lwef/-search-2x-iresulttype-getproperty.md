---
title: IResultType GetProperty, propriété (WdsSharedIDL. h)
description: Cette propriété contient les informations de propriété spécifiées.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Fonctions de l’environnement Windows hérité de la propriété GetProperty
- GetProperty, propriété fonctionnalités d’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités de l’environnement Windows héritées, propriété GetProperty
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843374"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="232b5-106">IResultType :: GetProperty, propriété</span><span class="sxs-lookup"><span data-stu-id="232b5-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="232b5-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="232b5-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="232b5-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="232b5-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="232b5-109">Cette propriété contient les informations de propriété spécifiées.</span><span class="sxs-lookup"><span data-stu-id="232b5-109">This property contains specified property information.</span></span>

<span data-ttu-id="232b5-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="232b5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="232b5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="232b5-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="232b5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="232b5-112">Property value</span></span>

<span data-ttu-id="232b5-113">Définit l’adresse des informations de propriété spécifiées.</span><span class="sxs-lookup"><span data-stu-id="232b5-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="232b5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="232b5-114">Requirements</span></span>



| <span data-ttu-id="232b5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="232b5-115">Requirement</span></span> | <span data-ttu-id="232b5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="232b5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="232b5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="232b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="232b5-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="232b5-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="232b5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="232b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="232b5-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="232b5-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="232b5-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="232b5-121">Redistributable</span></span><br/>          | <span data-ttu-id="232b5-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="232b5-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="232b5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="232b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="232b5-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="232b5-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





