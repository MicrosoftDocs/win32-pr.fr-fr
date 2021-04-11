---
description: Contient des informations sur un formulaire d’impression localisable.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Structure FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202691"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="a5033-103">Structure des informations de formulaire \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="a5033-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="a5033-104">Contient des informations sur un formulaire d’impression localisable.</span><span class="sxs-lookup"><span data-stu-id="a5033-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5033-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5033-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="a5033-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a5033-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5033-107">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="a5033-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-108">Propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5033-108">The form properties.</span></span> <span data-ttu-id="a5033-109">Les valeurs suivantes sont définies, mais une seule peut être définie.</span><span class="sxs-lookup"><span data-stu-id="a5033-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="a5033-110">Lorsque les **informations de formulaire \_ \_ 2** sont retournées par [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md), **Flags** est défini sur la valeur actuelle dans la base de données de formulaires.</span><span class="sxs-lookup"><span data-stu-id="a5033-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="a5033-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5033-111">Value</span></span>         | <span data-ttu-id="a5033-112">Signification</span><span class="sxs-lookup"><span data-stu-id="a5033-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5033-113">utilisateur de formulaire \_</span><span class="sxs-lookup"><span data-stu-id="a5033-113">FORM\_USER</span></span>    | <span data-ttu-id="a5033-114">Si cet indicateur de bit est défini, le formulaire a été défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5033-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="a5033-115">Les formulaires avec cet indicateur défini sont définis dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a5033-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="a5033-116">FORMULAIRE \_ BuiltIn</span><span class="sxs-lookup"><span data-stu-id="a5033-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="a5033-117">Si cet indicateur de bit est défini, le formulaire fait partie du spouleur.</span><span class="sxs-lookup"><span data-stu-id="a5033-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="a5033-118">Les définitions de formulaire pour lesquelles cet indicateur est défini n’apparaissent pas dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a5033-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="a5033-119">Les formulaires intégrés ne peuvent pas être modifiés. cet indicateur ne doit donc pas être défini lorsque la structure est transmise à [**AddForm**](addform.md) ou [**SetForm**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="a5033-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="a5033-120">imprimante de formulaire \_</span><span class="sxs-lookup"><span data-stu-id="a5033-120">FORM\_PRINTER</span></span> | <span data-ttu-id="a5033-121">Si cet indicateur de bit est défini, le formulaire est associé à une certaine imprimante et sa définition apparaît dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a5033-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="a5033-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="a5033-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-123">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a5033-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="a5033-124">Le nom du formulaire ne peut pas dépasser 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="a5033-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-125">**Taille**</span><span class="sxs-lookup"><span data-stu-id="a5033-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-126">Largeur et hauteur du formulaire en millièmes de millimètres.</span><span class="sxs-lookup"><span data-stu-id="a5033-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="a5033-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-128">Largeur et hauteur, en millièmes de millimètres, de la zone de la page sur laquelle l’imprimante peut imprimer.</span><span class="sxs-lookup"><span data-stu-id="a5033-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-129">**pKeyword**</span><span class="sxs-lookup"><span data-stu-id="a5033-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-130">Pointeur vers un identificateur de chaîne non localisable sous la forme.</span><span class="sxs-lookup"><span data-stu-id="a5033-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="a5033-131">Lorsqu’elle est transmise à [**AddForm**](addform.md) ou [**SetForm**](setform.md), l’appelant est un moyen d’identifier le formulaire dans tous les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a5033-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="a5033-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-133">Spécifie comment un nom complet localisé pour le formulaire est obtenu au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a5033-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="a5033-134">Les valeurs suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="a5033-134">The following values are defined.</span></span> <span data-ttu-id="a5033-135">Une seule peut être définie dans un appel donné à [**AddForm**](addform.md) ou [**SetForm**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="a5033-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="a5033-136">Les chaînes \_ MUIDLL et String \_ LANGPAIR peuvent être définies dans les **informations de formulaire \_ \_ 2** retournées par [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md).</span><span class="sxs-lookup"><span data-stu-id="a5033-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="a5033-137">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a5033-137">See Remarks.</span></span>



| <span data-ttu-id="a5033-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5033-138">Value</span></span>            | <span data-ttu-id="a5033-139">Signification</span><span class="sxs-lookup"><span data-stu-id="a5033-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5033-140">CHAÎNE \_ aucun</span><span class="sxs-lookup"><span data-stu-id="a5033-140">STRING\_NONE</span></span>     | <span data-ttu-id="a5033-141">Il n’existe aucun nom complet localisé.</span><span class="sxs-lookup"><span data-stu-id="a5033-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="a5033-142">CHAÎNE \_ MUIDLL</span><span class="sxs-lookup"><span data-stu-id="a5033-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="a5033-143">Le nom d’affichage est extrait de la DLL de ressources localisées de l' [interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) spécifiée dans **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="a5033-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="a5033-144">L’ID se trouve dans le membre **dwResourceId** .</span><span class="sxs-lookup"><span data-stu-id="a5033-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="a5033-145">CHAÎNE \_ LANGPAIR</span><span class="sxs-lookup"><span data-stu-id="a5033-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="a5033-146">Le nom d’affichage et l’ID de langue sont fournis directement par **pDisplayName** et la langue est spécifiée par **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="a5033-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="a5033-147">**pMuiDll**</span><span class="sxs-lookup"><span data-stu-id="a5033-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-148">DLL de ressource localisée de l' [interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) qui contient le nom complet localisé.</span><span class="sxs-lookup"><span data-stu-id="a5033-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-149">**dwResourceId**</span><span class="sxs-lookup"><span data-stu-id="a5033-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-150">ID de ressource du nom d’affichage du formulaire dans **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="a5033-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-151">**pDisplayName**</span><span class="sxs-lookup"><span data-stu-id="a5033-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-152">Nom complet du formulaire dans la langue spécifiée par **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="a5033-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="a5033-153">**wLangId**</span><span class="sxs-lookup"><span data-stu-id="a5033-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="a5033-154">Langage du **pDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="a5033-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5033-155">Notes</span><span class="sxs-lookup"><span data-stu-id="a5033-155">Remarks</span></span>

<span data-ttu-id="a5033-156">Sur un appel à [**AddForm**](addform.md) ou [**SetForm**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="a5033-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="a5033-157">Si **StringType** a la \_ valeur String None, **pMuiDll** et **PDisplayName** doivent tous deux avoir la **valeur null** et **dwResourceId** et **wLangId** doivent avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="a5033-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="a5033-158">Si **StringType** est de type String \_ MUIDLL, **PDisplayName** doit avoir la **valeur null** et **wLangId** doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="a5033-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="a5033-159">Si **StringType** est de type String \_ LANGPAIR, **PMuiDll** doit avoir la **valeur null** et **dwResourceId** doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="a5033-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="a5033-160">Pour les **informations de formulaire \_ \_ 2** retournées par un appel à [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md):</span><span class="sxs-lookup"><span data-stu-id="a5033-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="a5033-161">Si **StringType** est à la fois String \_ MUIDLL et String \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** et **wLangId** auront des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="a5033-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="a5033-162">Si **StringType** a la valeur String \_ MUIDLL only, **pMuiDll** et **dwResourceId** auront des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="a5033-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="a5033-163">**pDisplayName** sera **null** et **wLangId** sera 0.</span><span class="sxs-lookup"><span data-stu-id="a5033-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="a5033-164">Si **StringType** a la valeur String \_ LANGPAIR only, **pDisplayName** et **wLangId** auront des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="a5033-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="a5033-165">**pMuiDll** sera **null** et **dwResourceId** sera 0.</span><span class="sxs-lookup"><span data-stu-id="a5033-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5033-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5033-166">Requirements</span></span>



| <span data-ttu-id="a5033-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5033-167">Requirement</span></span> | <span data-ttu-id="a5033-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5033-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5033-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5033-169">Minimum supported client</span></span><br/> | <span data-ttu-id="a5033-170">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5033-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a5033-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5033-171">Minimum supported server</span></span><br/> | <span data-ttu-id="a5033-172">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5033-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5033-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5033-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5033-174"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a5033-175">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a5033-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a5033-176">**\_ Informations de formulaire \_ \_ 2S** (Unicode) et **\_ informations de formulaire \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a5033-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="a5033-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5033-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5033-178">Impression</span><span class="sxs-lookup"><span data-stu-id="a5033-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a5033-179">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a5033-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a5033-180">Interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="a5033-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="a5033-181">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="a5033-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="a5033-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="a5033-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="a5033-183">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="a5033-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="a5033-184">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="a5033-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

