---
title: IResultsViewer SortProperty, propriété (WdsView. h)
description: Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Propriétés SortProperty héritées fonctionnalités de l’environnement Windows
- Propriété SortProperty fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843505"
---
# <a name="iresultsviewersortproperty-property"></a><span data-ttu-id="4011d-106">IResultsViewer :: SortProperty, propriété</span><span class="sxs-lookup"><span data-stu-id="4011d-106">IResultsViewer::SortProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="4011d-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4011d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4011d-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4011d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4011d-109">Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.</span><span class="sxs-lookup"><span data-stu-id="4011d-109">This property will set or return the IndexColumn of the property to sort results by.</span></span>

<span data-ttu-id="4011d-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4011d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4011d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4011d-111">Syntax</span></span>


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="4011d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4011d-112">Property value</span></span>

<span data-ttu-id="4011d-113">Définit la propriété IndexColumn.</span><span class="sxs-lookup"><span data-stu-id="4011d-113">Sets the IndexColumn property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4011d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4011d-114">Requirements</span></span>



| <span data-ttu-id="4011d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4011d-115">Requirement</span></span> | <span data-ttu-id="4011d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4011d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4011d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4011d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4011d-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4011d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4011d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4011d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4011d-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4011d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="4011d-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4011d-121">Redistributable</span></span><br/>          | <span data-ttu-id="4011d-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="4011d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="4011d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4011d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4011d-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="4011d-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





