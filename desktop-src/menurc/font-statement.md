---
title: FONT (instruction)
description: Définit la police avec laquelle le système dessinera du texte dans la boîte de dialogue. La police doit avoir été précédemment chargée ; par exemple, en appelant la fonction LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menus d’instructions de police et autres ressources
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463111"
---
# <a name="font-statement"></a><span data-ttu-id="065e4-105">FONT (instruction)</span><span class="sxs-lookup"><span data-stu-id="065e4-105">FONT statement</span></span>

<span data-ttu-id="065e4-106">Définit la police avec laquelle le système dessinera du texte dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="065e4-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="065e4-107">La police doit avoir été précédemment chargée ; par exemple, en appelant la fonction [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="065e4-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="065e4-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span><span class="sxs-lookup"><span data-stu-id="065e4-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="065e4-109">Taille de la police, en points.</span><span class="sxs-lookup"><span data-stu-id="065e4-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="065e4-110"><span id="typeface"></span><span id="TYPEFACE"></span>*certain*</span><span class="sxs-lookup"><span data-stu-id="065e4-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="065e4-111">Nom de la police.</span><span class="sxs-lookup"><span data-stu-id="065e4-111">The name of the typeface.</span></span> <span data-ttu-id="065e4-112">Ce paramètre doit être placé entre guillemets (").</span><span class="sxs-lookup"><span data-stu-id="065e4-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="065e4-113"><span id="weight"></span><span id="WEIGHT"></span>*poids*</span><span class="sxs-lookup"><span data-stu-id="065e4-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="065e4-114">Poids de la police dans la plage comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="065e4-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="065e4-115">Par exemple, 400 est normal et 700 est en gras.</span><span class="sxs-lookup"><span data-stu-id="065e4-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="065e4-116">Si cette valeur est égale à 0, le poids par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="065e4-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="065e4-117">Pour obtenir la liste des valeurs prédéfinies, consultez les valeurs **FW \_ \*** définies dans WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="065e4-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="065e4-118"><span id="italic"></span><span id="ITALIC"></span>*italique*</span><span class="sxs-lookup"><span data-stu-id="065e4-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="065e4-119">Indique une police en italique si la valeur est TRUE.</span><span class="sxs-lookup"><span data-stu-id="065e4-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="065e4-120"><span id="charset"></span><span id="CHARSET"></span>*caractères*</span><span class="sxs-lookup"><span data-stu-id="065e4-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="065e4-121">Jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="065e4-121">The character set.</span></span> <span data-ttu-id="065e4-122">Pour obtenir la liste des valeurs, consultez le membre **lfCharSet** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="065e4-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="065e4-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="065e4-123">Examples</span></span>

<span data-ttu-id="065e4-124">L’exemple suivant illustre l’utilisation de l’instruction **font** :</span><span class="sxs-lookup"><span data-stu-id="065e4-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="065e4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="065e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065e4-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="065e4-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 