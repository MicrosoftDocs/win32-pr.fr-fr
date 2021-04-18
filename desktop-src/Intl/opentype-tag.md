---
description: Définit un tableau de 4 octets qui contient les valeurs ASCII 4 8 bits de l’espace, A-Z ou a-z pour identifier les balises de fonctionnalité de script, de langue et de police OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519804"
---
# <a name="opentype_tag"></a><span data-ttu-id="5d8b6-103">\_balise OpenType</span><span class="sxs-lookup"><span data-stu-id="5d8b6-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="5d8b6-104">Définit un tableau de 4 octets qui contient les valeurs ASCII 4 8 bits de l’espace, A-Z ou a-z pour identifier les balises de fonctionnalité de script, de langue et de police OpenType.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="5d8b6-105">Notes</span><span class="sxs-lookup"><span data-stu-id="5d8b6-105">Remarks</span></span>

<span data-ttu-id="5d8b6-106">Les exemples suivants définissent des représentations de balises de fonctionnalités OpenType.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="5d8b6-107">La balise de fonctionnalité pour la fonctionnalité de ligature est « Liga ».</span><span class="sxs-lookup"><span data-stu-id="5d8b6-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="5d8b6-108">Les balises de langue pour roumain, ourdou et persan sont respectivement « ROM », « URD » et « FAR ».</span><span class="sxs-lookup"><span data-stu-id="5d8b6-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="5d8b6-109">Notez que chacune de ces balises se termine par un espace.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="5d8b6-110">Les balises de script pour les scripts latins et arabes sont respectivement « LATN » et « arabe ».</span><span class="sxs-lookup"><span data-stu-id="5d8b6-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="5d8b6-111">Pour plus d’informations sur les balises de fonctionnalités OpenType et la spécification OpenType, consultez <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="5d8b6-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d8b6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d8b6-112">Requirements</span></span>



| <span data-ttu-id="5d8b6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d8b6-113">Requirement</span></span> | <span data-ttu-id="5d8b6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d8b6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8b6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d8b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8b6-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d8b6-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5d8b6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d8b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8b6-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d8b6-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d8b6-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5d8b6-119">Redistributable</span></span><br/>          | <span data-ttu-id="5d8b6-120">Usp10.dll version 1,600 ou supérieure onWindows velopper plus tard</span><span class="sxs-lookup"><span data-stu-id="5d8b6-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="5d8b6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d8b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d8b6-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d8b6-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d8b6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d8b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8b6-124">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5d8b6-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="5d8b6-125">Structures Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5d8b6-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="5d8b6-126">**ScriptGetFontAlternateGlyphs**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="5d8b6-127">**ScriptGetFontFeatureTags**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="5d8b6-128">**ScriptGetFontLanguageTags**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="5d8b6-129">**ScriptGetFontScriptTags**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="5d8b6-130">**ScriptItemizeOpenType**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="5d8b6-131">**ScriptPlaceOpenType**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="5d8b6-132">**ScriptPositionSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="5d8b6-133">**ScriptShapeOpenType**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="5d8b6-134">**ScriptSubstituteSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="5d8b6-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




