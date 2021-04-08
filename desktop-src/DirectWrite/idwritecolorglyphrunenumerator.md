---
title: Interface IDWriteColorGlyphRunEnumerator
description: Cette interface permet à l’application d’énumérer les exécutions de glyphes de couleurs.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator, décrite
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742237"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="df635-105">Interface IDWriteColorGlyphRunEnumerator</span><span class="sxs-lookup"><span data-stu-id="df635-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="df635-106">Cette interface permet à l’application d’énumérer les exécutions de glyphes de couleurs.</span><span class="sxs-lookup"><span data-stu-id="df635-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="df635-107">L’énumérateur énumère les couches dans une commande Back to front pour les couches appropriées.</span><span class="sxs-lookup"><span data-stu-id="df635-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="df635-108">Membres</span><span class="sxs-lookup"><span data-stu-id="df635-108">Members</span></span>

<span data-ttu-id="df635-109">L’interface **IDWriteColorGlyphRunEnumerator** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="df635-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="df635-110">**IDWriteColorGlyphRunEnumerator** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df635-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="df635-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df635-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="df635-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df635-112">Methods</span></span>

<span data-ttu-id="df635-113">L’interface **IDWriteColorGlyphRunEnumerator** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="df635-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="df635-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="df635-114">Method</span></span>                                                                | <span data-ttu-id="df635-115">Description</span><span class="sxs-lookup"><span data-stu-id="df635-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="df635-116">**GetCurrentRun**</span><span class="sxs-lookup"><span data-stu-id="df635-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="df635-117">Retourne l’exécution de glyphes actuelle de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="df635-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="df635-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="df635-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="df635-119">Passe au glyphe suivant exécuté dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="df635-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="df635-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df635-120">Requirements</span></span>



| <span data-ttu-id="df635-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df635-121">Requirement</span></span> | <span data-ttu-id="df635-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="df635-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df635-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df635-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df635-124">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="df635-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="df635-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df635-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df635-126">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="df635-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="df635-127">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df635-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="df635-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="df635-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="df635-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df635-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="df635-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df635-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df635-131">DLL</span><span class="sxs-lookup"><span data-stu-id="df635-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df635-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df635-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

