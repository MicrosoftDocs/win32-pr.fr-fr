---
description: Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518865"
---
# <a name="script_string_analysis"></a><span data-ttu-id="64322-103">\_analyse de chaîne de script \_</span><span class="sxs-lookup"><span data-stu-id="64322-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="64322-104">Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.</span><span class="sxs-lookup"><span data-stu-id="64322-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="64322-105">Notes</span><span class="sxs-lookup"><span data-stu-id="64322-105">Remarks</span></span>

<span data-ttu-id="64322-106">Il s’agit d’une structure opaque qui est allouée dynamiquement et récupérée par [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span><span class="sxs-lookup"><span data-stu-id="64322-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="64322-107">Elle est requise pour toutes les autres fonctions \**ScriptString \** _.</span><span class="sxs-lookup"><span data-stu-id="64322-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="64322-108">Étant donné que l’analyse peut être volumineuse, il est important que votre application appelle [_ *ScriptStringFree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) dès qu’elle a terminé la chaîne.</span><span class="sxs-lookup"><span data-stu-id="64322-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="64322-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64322-109">Requirements</span></span>



| <span data-ttu-id="64322-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64322-110">Requirement</span></span> | <span data-ttu-id="64322-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="64322-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64322-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64322-112">Minimum supported client</span></span><br/> | <span data-ttu-id="64322-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64322-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="64322-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64322-114">Minimum supported server</span></span><br/> | <span data-ttu-id="64322-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64322-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64322-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="64322-116">Redistributable</span></span><br/>          | <span data-ttu-id="64322-117">Internet Explorer 5 ou version ultérieure onWindows me/98/95</span><span class="sxs-lookup"><span data-stu-id="64322-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="64322-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="64322-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="64322-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="64322-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64322-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64322-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64322-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="64322-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="64322-122">Structures Uniscribe</span><span class="sxs-lookup"><span data-stu-id="64322-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="64322-123">**ScriptStringAnalyse**</span><span class="sxs-lookup"><span data-stu-id="64322-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="64322-124">**ScriptStringFree**</span><span class="sxs-lookup"><span data-stu-id="64322-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




