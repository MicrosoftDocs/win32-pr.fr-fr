---
title: Propriété Text IPropertyFilter (WdsSharedIDL. h)
description: Texte du filtre.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Propriétés de texte héritées fonctionnalités de l’environnement Windows
- Propriétés de texte héritées fonctionnalités de l’environnement Windows, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités de l’environnement Windows héritées, propriété Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508933"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="74911-106">IPropertyFilter :: Text, propriété</span><span class="sxs-lookup"><span data-stu-id="74911-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="74911-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="74911-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="74911-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="74911-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="74911-109">Texte du filtre.</span><span class="sxs-lookup"><span data-stu-id="74911-109">Text of the filter.</span></span>

<span data-ttu-id="74911-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74911-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74911-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74911-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="74911-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="74911-112">Property value</span></span>

<span data-ttu-id="74911-113">Définit le texte du filtre.</span><span class="sxs-lookup"><span data-stu-id="74911-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="74911-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74911-114">Requirements</span></span>



| <span data-ttu-id="74911-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74911-115">Requirement</span></span> | <span data-ttu-id="74911-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="74911-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74911-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74911-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74911-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74911-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74911-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74911-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74911-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74911-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="74911-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="74911-121">Redistributable</span></span><br/>          | <span data-ttu-id="74911-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="74911-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="74911-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="74911-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74911-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="74911-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





