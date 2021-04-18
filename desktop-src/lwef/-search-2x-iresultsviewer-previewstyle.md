---
title: IResultsViewer PreviewStyle, propriété (WdsView. h)
description: Contrôle le mode d’affichage du volet de visualisation.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Propriétés PreviewStyle héritées fonctionnalités de l’environnement Windows
- Propriété PreviewStyle fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété PreviewStyle
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512141"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="fd44c-106">IResultsViewer ::P propriété reviewStyle</span><span class="sxs-lookup"><span data-stu-id="fd44c-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="fd44c-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fd44c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="fd44c-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="fd44c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="fd44c-109">Contrôle le mode d’affichage du volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="fd44c-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="fd44c-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fd44c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd44c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd44c-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="fd44c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fd44c-112">Property value</span></span>

<span data-ttu-id="fd44c-113">Définit la propriété de style actuelle pour le volet de visualisation.</span><span class="sxs-lookup"><span data-stu-id="fd44c-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd44c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd44c-114">Requirements</span></span>



| <span data-ttu-id="fd44c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd44c-115">Requirement</span></span> | <span data-ttu-id="fd44c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd44c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd44c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd44c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd44c-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd44c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd44c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd44c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd44c-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd44c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="fd44c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fd44c-121">Redistributable</span></span><br/>          | <span data-ttu-id="fd44c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="fd44c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="fd44c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd44c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd44c-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd44c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





