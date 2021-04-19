---
title: Interface IDWriteTextFormat2
description: Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. | Interface IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Écriture directe de l’interface IDWriteTextFormat2
- Écriture directe de l’interface IDWriteTextFormat2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523782"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="77457-106">Interface IDWriteTextFormat2</span><span class="sxs-lookup"><span data-stu-id="77457-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="77457-107">Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="77457-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="77457-108">Membres</span><span class="sxs-lookup"><span data-stu-id="77457-108">Members</span></span>

<span data-ttu-id="77457-109">L’interface **IDWriteTextFormat2** hérite de [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="77457-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="77457-110">**IDWriteTextFormat2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77457-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="77457-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77457-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77457-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77457-112">Methods</span></span>

<span data-ttu-id="77457-113">L’interface **IDWriteTextFormat2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="77457-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="77457-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="77457-114">Method</span></span>                                                      | <span data-ttu-id="77457-115">Description</span><span class="sxs-lookup"><span data-stu-id="77457-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="77457-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="77457-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="77457-117">Obtient l’ajustement de l’interligne défini pour un paragraphe de texte multiligne.</span><span class="sxs-lookup"><span data-stu-id="77457-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="77457-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="77457-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="77457-119">Définissez l’interligne.</span><span class="sxs-lookup"><span data-stu-id="77457-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="77457-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77457-120">Requirements</span></span>



| <span data-ttu-id="77457-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77457-121">Requirement</span></span> | <span data-ttu-id="77457-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="77457-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77457-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77457-123">Minimum supported client</span></span><br/> | <span data-ttu-id="77457-124">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="77457-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="77457-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77457-125">Minimum supported server</span></span><br/> | <span data-ttu-id="77457-126">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="77457-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="77457-127">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77457-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="77457-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="77457-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="77457-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77457-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="77457-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77457-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="77457-131">DLL</span><span class="sxs-lookup"><span data-stu-id="77457-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77457-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77457-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77457-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77457-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77457-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="77457-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

