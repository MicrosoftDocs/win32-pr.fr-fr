---
title: Propriété DisplayName IResultsViewer (WdsView. h)
description: Nom complet localisé du type.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510959"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="e9f6b-106">IResultsViewer ::D propriété isplayName</span><span class="sxs-lookup"><span data-stu-id="e9f6b-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="e9f6b-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e9f6b-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f6b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e9f6b-109">Nom complet localisé du type.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-109">Localized display name of the type.</span></span>

<span data-ttu-id="e9f6b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f6b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9f6b-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="e9f6b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e9f6b-112">Property value</span></span>

<span data-ttu-id="e9f6b-113">Pointeur vers une valeur qui reçoit le nom complet localisé pour le type.</span><span class="sxs-lookup"><span data-stu-id="e9f6b-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f6b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f6b-114">Requirements</span></span>



| <span data-ttu-id="e9f6b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f6b-115">Requirement</span></span> | <span data-ttu-id="e9f6b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f6b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f6b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f6b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f6b-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f6b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e9f6b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f6b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f6b-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f6b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="e9f6b-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e9f6b-121">Redistributable</span></span><br/>          | <span data-ttu-id="e9f6b-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e9f6b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="e9f6b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f6b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f6b-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f6b-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





