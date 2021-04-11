---
title: IResultsViewer QueryText, propriété (WdsView. h)
description: Obtient ou définit le texte de la requête actuelle.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Propriétés QueryText héritées fonctionnalités de l’environnement Windows
- Propriété QueryText fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105781"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="8592c-106">IResultsViewer :: QueryText, propriété</span><span class="sxs-lookup"><span data-stu-id="8592c-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="8592c-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8592c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8592c-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8592c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8592c-109">Obtient ou définit le texte de la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="8592c-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="8592c-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8592c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8592c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8592c-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="8592c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8592c-112">Property value</span></span>

<span data-ttu-id="8592c-113">Définit le texte de la requête actuelle.</span><span class="sxs-lookup"><span data-stu-id="8592c-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="8592c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8592c-114">Requirements</span></span>



| <span data-ttu-id="8592c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8592c-115">Requirement</span></span> | <span data-ttu-id="8592c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8592c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8592c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8592c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8592c-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8592c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8592c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8592c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8592c-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8592c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8592c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8592c-121">Redistributable</span></span><br/>          | <span data-ttu-id="8592c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8592c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="8592c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8592c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8592c-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="8592c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





