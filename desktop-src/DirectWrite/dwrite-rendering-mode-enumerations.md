---
title: Énumérations de DWRITE_RENDERING_MODE
description: À compter de Windows 8, l' \_ énumération du mode de rendu DWRITE a \_ ajouté de nouvelles valeurs d’énumération et déconseillé d’autres.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2019
ms.locfileid: "103939532"
---
# <a name="dwrite_rendering_mode-enumerations"></a><span data-ttu-id="1e8de-103">\_Énumérations du mode de rendu DWRITE \_</span><span class="sxs-lookup"><span data-stu-id="1e8de-103">DWRITE\_RENDERING\_MODE enumerations</span></span>

<span data-ttu-id="1e8de-104">À compter de Windows 8, l’énumération du **\_ \_ mode de rendu DWRITE** a ajouté de nouvelles valeurs d’énumération et déconseillé d’autres.</span><span class="sxs-lookup"><span data-stu-id="1e8de-104">Starting in Windows 8, the **DWRITE\_RENDERING\_MODE** enumeration added new enumeration values and deprecated others.</span></span>

<span data-ttu-id="1e8de-105">À compter de Windows 8, l’énumération du [**\_ mode DWRITE Text \_ antialias \_**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) détermine si le texte est rendu à l’aide de ClearType.</span><span class="sxs-lookup"><span data-stu-id="1e8de-105">Starting in Windows 8, the [**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) enumeration determines whether text is rendered using ClearType.</span></span> <span data-ttu-id="1e8de-106">Par conséquent, tous les modes de rendu ClearType dans l’énumération du **\_ \_ mode de rendu DWRITE** sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="1e8de-106">As a result, all the ClearType rendering modes in the **DWRITE\_RENDERING\_MODE** enumeration are deprecated.</span></span> <span data-ttu-id="1e8de-107">Ces valeurs d’énumération sont maintenant mappées à de nouveaux modes de rendu.</span><span class="sxs-lookup"><span data-stu-id="1e8de-107">These enumeration values now map to new rendering modes.</span></span>

<span data-ttu-id="1e8de-108">Le tableau ci-dessous montre les anciennes valeurs d’énumération et les nouvelles valeurs auxquelles elles sont mappées.</span><span class="sxs-lookup"><span data-stu-id="1e8de-108">The table here shows the old enumeration values and the new values they are mapped to.</span></span> <span data-ttu-id="1e8de-109">Pour obtenir une description des nouvelles valeurs, [**consultez \_ \_ mode de rendu DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span><span class="sxs-lookup"><span data-stu-id="1e8de-109">For descriptions of the new values, see [**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span></span>



| <span data-ttu-id="1e8de-110">Ancien mode</span><span class="sxs-lookup"><span data-stu-id="1e8de-110">Old mode</span></span>                                                                                | <span data-ttu-id="1e8de-111">Nouveau mode</span><span class="sxs-lookup"><span data-stu-id="1e8de-111">New mode</span></span>                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e8de-112">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ GDI \_ classique**</span><span class="sxs-lookup"><span data-stu-id="1e8de-112">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="1e8de-113">**\_mode de rendu DWRITE \_ \_ GDI \_ classique**</span><span class="sxs-lookup"><span data-stu-id="1e8de-113">**DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="1e8de-114">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ GDI \_ naturel**</span><span class="sxs-lookup"><span data-stu-id="1e8de-114">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="1e8de-115">**\_mode de rendu DWRITE \_ \_ GDI \_ naturel**</span><span class="sxs-lookup"><span data-stu-id="1e8de-115">**DWRITE\_RENDERING\_MODE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="1e8de-116">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ naturel**</span><span class="sxs-lookup"><span data-stu-id="1e8de-116">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [<span data-ttu-id="1e8de-117">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ naturel**</span><span class="sxs-lookup"><span data-stu-id="1e8de-117">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [<span data-ttu-id="1e8de-118">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ Natural \_ symétrique**</span><span class="sxs-lookup"><span data-stu-id="1e8de-118">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [<span data-ttu-id="1e8de-119">**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ Natural \_ symétrique**</span><span class="sxs-lookup"><span data-stu-id="1e8de-119">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a><span data-ttu-id="1e8de-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1e8de-120">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e8de-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1e8de-121">Topic</span></span></th>
<th><span data-ttu-id="1e8de-122">Description</span><span class="sxs-lookup"><span data-stu-id="1e8de-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e8de-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 et versions ultérieures)</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e8de-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 and later)</strong></a></span></span><br/></td>
<td><span data-ttu-id="1e8de-124">Représente une méthode de rendu des glyphes.</span><span class="sxs-lookup"><span data-stu-id="1e8de-124">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e8de-125">Cette rubrique concerne <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> dans Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1e8de-125">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 and later.</span></span> <span data-ttu-id="1e8de-126">Pour plus d’informations sur la version précédente, consultez <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>cette rubrique</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1e8de-126">For info on the previous version see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>this topic</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e8de-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e8de-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="1e8de-128">Représente une méthode de rendu des glyphes.</span><span class="sxs-lookup"><span data-stu-id="1e8de-128">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e8de-129">Cette rubrique concerne <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> antérieure à Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1e8de-129">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> previous to Windows 8 and later.</span></span> <span data-ttu-id="1e8de-130">Pour plus d’informations sur la version plus récente, consultez <strong>cette rubrique</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e8de-130">For info on the newer version see <strong>this topic</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





