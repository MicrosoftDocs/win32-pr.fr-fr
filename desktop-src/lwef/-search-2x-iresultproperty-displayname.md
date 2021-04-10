---
title: Propriété DisplayName IResultProperty (WdsSharedIDL. h)
description: Nom complet localisé de la propriété.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104554"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="c3f1a-106">IResultProperty ::D propriété isplayName</span><span class="sxs-lookup"><span data-stu-id="c3f1a-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="c3f1a-107">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3f1a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c3f1a-108">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f1a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c3f1a-109">Nom complet localisé de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c3f1a-109">Localized display name of the property.</span></span>

<span data-ttu-id="c3f1a-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c3f1a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f1a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3f1a-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="c3f1a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c3f1a-112">Property value</span></span>

<span data-ttu-id="c3f1a-113">retourne un pointeur vers le nom complet localisé.</span><span class="sxs-lookup"><span data-stu-id="c3f1a-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f1a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3f1a-114">Requirements</span></span>



| <span data-ttu-id="c3f1a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3f1a-115">Requirement</span></span> | <span data-ttu-id="c3f1a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3f1a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f1a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3f1a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f1a-118">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3f1a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c3f1a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3f1a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f1a-120">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3f1a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c3f1a-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c3f1a-121">Redistributable</span></span><br/>          | <span data-ttu-id="c3f1a-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c3f1a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c3f1a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3f1a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f1a-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3f1a-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





