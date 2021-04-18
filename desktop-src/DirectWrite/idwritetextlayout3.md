---
title: Interface IDWriteTextLayout3
description: Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. | Interface IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Écriture directe de l’interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, décrite
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522544"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="09a3f-106">Interface IDWriteTextLayout3</span><span class="sxs-lookup"><span data-stu-id="09a3f-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="09a3f-107">Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme.</span><span class="sxs-lookup"><span data-stu-id="09a3f-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="09a3f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="09a3f-108">Members</span></span>

<span data-ttu-id="09a3f-109">L’interface **IDWriteTextLayout3** hérite de [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="09a3f-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="09a3f-110">**IDWriteTextLayout3** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="09a3f-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="09a3f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09a3f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="09a3f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09a3f-112">Methods</span></span>

<span data-ttu-id="09a3f-113">L’interface **IDWriteTextLayout3** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="09a3f-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="09a3f-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="09a3f-114">Method</span></span>                                                          | <span data-ttu-id="09a3f-115">Description</span><span class="sxs-lookup"><span data-stu-id="09a3f-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09a3f-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="09a3f-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="09a3f-117">Récupère les propriétés de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="09a3f-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="09a3f-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="09a3f-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="09a3f-119">Obtient les informations d’interligne.</span><span class="sxs-lookup"><span data-stu-id="09a3f-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="09a3f-120">**InvalidateLayout**</span><span class="sxs-lookup"><span data-stu-id="09a3f-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="09a3f-121">Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin.</span><span class="sxs-lookup"><span data-stu-id="09a3f-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="09a3f-122">Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée.</span><span class="sxs-lookup"><span data-stu-id="09a3f-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="09a3f-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="09a3f-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="09a3f-124">Définissez l’interligne.</span><span class="sxs-lookup"><span data-stu-id="09a3f-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="09a3f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09a3f-125">Requirements</span></span>



| <span data-ttu-id="09a3f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09a3f-126">Requirement</span></span> | <span data-ttu-id="09a3f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="09a3f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09a3f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09a3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="09a3f-129">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="09a3f-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="09a3f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09a3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="09a3f-131">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="09a3f-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="09a3f-132">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09a3f-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="09a3f-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="09a3f-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="09a3f-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09a3f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="09a3f-135"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09a3f-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="09a3f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="09a3f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09a3f-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09a3f-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09a3f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09a3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a3f-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="09a3f-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





