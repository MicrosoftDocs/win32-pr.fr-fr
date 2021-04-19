---
title: Propriété de type de données IResultProperty (WdsSharedIDL. h)
description: Type de données des propriétés.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Propriété DataType, fonctionnalités de l’environnement Windows héritées
- Propriété DataType héritée fonctionnalités de l’environnement Windows, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510548"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="f8619-106">IResultProperty ::D propriété ataType</span><span class="sxs-lookup"><span data-stu-id="f8619-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="f8619-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f8619-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f8619-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f8619-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f8619-109">Type de données des propriétés.</span><span class="sxs-lookup"><span data-stu-id="f8619-109">A properties data type.</span></span>

<span data-ttu-id="f8619-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f8619-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8619-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8619-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="f8619-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f8619-112">Property value</span></span>

<span data-ttu-id="f8619-113">retourne un pointeur vers le type de données des propriétés.</span><span class="sxs-lookup"><span data-stu-id="f8619-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8619-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8619-114">Requirements</span></span>



| <span data-ttu-id="f8619-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8619-115">Requirement</span></span> | <span data-ttu-id="f8619-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8619-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8619-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8619-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8619-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8619-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f8619-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8619-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8619-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8619-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f8619-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f8619-121">Redistributable</span></span><br/>          | <span data-ttu-id="f8619-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="f8619-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="f8619-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8619-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8619-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8619-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





