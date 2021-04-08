---
title: IResultsViewer HeaderStyle, propriété (WdsView. h)
description: Style de l’en-tête affiché dans la vue.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Propriété HeaderStyle héritée des fonctionnalités de l’environnement Windows
- HeaderStyle, propriété fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités de l’environnement Windows héritées, propriété HeaderStyle
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741596"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="a0cf3-106">IResultsViewer :: HeaderStyle, propriété</span><span class="sxs-lookup"><span data-stu-id="a0cf3-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="a0cf3-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a0cf3-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a0cf3-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a0cf3-109">Style de l’en-tête affiché dans la vue.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="a0cf3-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cf3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0cf3-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="a0cf3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a0cf3-112">Property value</span></span>

<span data-ttu-id="a0cf3-113">Définit le style de l’en-tête affiché.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cf3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0cf3-114">Requirements</span></span>



| <span data-ttu-id="a0cf3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0cf3-115">Requirement</span></span> | <span data-ttu-id="a0cf3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0cf3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cf3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cf3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cf3-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0cf3-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a0cf3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cf3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cf3-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0cf3-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="a0cf3-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a0cf3-121">Redistributable</span></span><br/>          | <span data-ttu-id="a0cf3-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="a0cf3-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="a0cf3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0cf3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0cf3-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0cf3-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





