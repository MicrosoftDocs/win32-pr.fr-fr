---
title: IResultsViewer FilterType, propriété (WdsView. h)
description: Cette propriété définit ou retourne le nom du type preceived pour filtrer les résultats par.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- Propriété FilterType, fonctionnalités d’environnement Windows héritées
- Propriété FilterType, fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518124"
---
# <a name="iresultsviewerfiltertype-property"></a><span data-ttu-id="8a0d4-106">IResultsViewer :: FilterType, propriété</span><span class="sxs-lookup"><span data-stu-id="8a0d4-106">IResultsViewer::FilterType property</span></span>

> [!NOTE]
> <span data-ttu-id="8a0d4-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8a0d4-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8a0d4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8a0d4-109">Cette propriété définit ou retourne le nom du type preceived pour filtrer les résultats par.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-109">This property will set or return the name of the preceived type to filter results by.</span></span>

<span data-ttu-id="8a0d4-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0d4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a0d4-111">Syntax</span></span>


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="8a0d4-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8a0d4-112">Property value</span></span>

<span data-ttu-id="8a0d4-113">Définit le type perçu utilisé pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="8a0d4-113">Sets the perceived type used to filter results.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0d4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a0d4-114">Requirements</span></span>



| <span data-ttu-id="8a0d4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a0d4-115">Requirement</span></span> | <span data-ttu-id="8a0d4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a0d4-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0d4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a0d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0d4-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a0d4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a0d4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a0d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0d4-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a0d4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8a0d4-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8a0d4-121">Redistributable</span></span><br/>          | <span data-ttu-id="8a0d4-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8a0d4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="8a0d4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a0d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a0d4-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0d4-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





