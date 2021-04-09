---
title: IResultType PreceivedType, propriété (WdsSharedIDL. h)
description: Cette propriété contient la chaîne utilisée pour identifier le type dans l’index.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Propriétés PreceivedType héritées fonctionnalités de l’environnement Windows
- Propriété PreceivedType fonctionnalités de l’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843373"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="aec07-106">IResultType ::P propriété receivedType</span><span class="sxs-lookup"><span data-stu-id="aec07-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="aec07-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aec07-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="aec07-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="aec07-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="aec07-109">Cette propriété contient la chaîne utilisée pour identifier le type dans l’index.</span><span class="sxs-lookup"><span data-stu-id="aec07-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="aec07-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aec07-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec07-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aec07-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="aec07-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aec07-112">Property value</span></span>

<span data-ttu-id="aec07-113">retourne l’adresse de la chaîne identifyint le type dans l’index.</span><span class="sxs-lookup"><span data-stu-id="aec07-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec07-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aec07-114">Requirements</span></span>



| <span data-ttu-id="aec07-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aec07-115">Requirement</span></span> | <span data-ttu-id="aec07-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aec07-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec07-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aec07-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aec07-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aec07-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="aec07-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aec07-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aec07-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aec07-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aec07-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aec07-121">Redistributable</span></span><br/>          | <span data-ttu-id="aec07-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="aec07-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="aec07-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aec07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aec07-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec07-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





