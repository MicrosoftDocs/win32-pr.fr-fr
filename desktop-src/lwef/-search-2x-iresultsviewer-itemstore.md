---
title: IResultsViewer ItemStore, propriété (WdsView. h)
description: Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Propriétés ItemStore héritées fonctionnalités de l’environnement Windows
- Propriété ItemStore fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété ItemStore
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465167"
---
# <a name="iresultsvieweritemstore-property"></a><span data-ttu-id="b186c-106">IResultsViewer :: ItemStore, propriété</span><span class="sxs-lookup"><span data-stu-id="b186c-106">IResultsViewer::ItemStore property</span></span>

> [!NOTE]
> <span data-ttu-id="b186c-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b186c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b186c-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="b186c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b186c-109">Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="b186c-109">This property will set or return the name of the store to filter results by.</span></span>

<span data-ttu-id="b186c-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b186c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b186c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b186c-111">Syntax</span></span>


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="b186c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b186c-112">Property value</span></span>

<span data-ttu-id="b186c-113">Définit les noms du magasin.</span><span class="sxs-lookup"><span data-stu-id="b186c-113">Sets the names of the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="b186c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b186c-114">Requirements</span></span>



| <span data-ttu-id="b186c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b186c-115">Requirement</span></span> | <span data-ttu-id="b186c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b186c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b186c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b186c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b186c-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b186c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b186c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b186c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b186c-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b186c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b186c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b186c-121">Redistributable</span></span><br/>          | <span data-ttu-id="b186c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="b186c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="b186c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b186c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b186c-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="b186c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





