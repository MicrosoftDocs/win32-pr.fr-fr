---
title: attribut nocode
description: L’attribut \ nocode \ est utilisé dans les en-têtes ACF ou avec des fonctions individuelles pour empêcher la génération de code stub client.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- attribut nocode MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312211"
---
# <a name="nocode-attribute"></a><span data-ttu-id="42667-104">attribut nocode</span><span class="sxs-lookup"><span data-stu-id="42667-104">nocode attribute</span></span>

<span data-ttu-id="42667-105">L’attribut **\[ nocode \]** est utilisé dans les en-têtes ACF ou avec des fonctions individuelles pour empêcher la génération de code stub client.</span><span class="sxs-lookup"><span data-stu-id="42667-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="42667-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42667-107">*ACF-interface-attributs*</span><span class="sxs-lookup"><span data-stu-id="42667-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-108">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="42667-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="42667-109">Les attributs valides incluent **\[** [**\_ handle automatique**](auto-handle.md) **\]** ou **\[** [**\_ handle implicite**](implicit-handle.md) **\]** et **\[** [**code**](code.md) **\]** ou **\[ \] nocode**.</span><span class="sxs-lookup"><span data-stu-id="42667-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="42667-110">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="42667-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="42667-111">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="42667-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-112">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="42667-112">Specifies the name of the interface.</span></span> <span data-ttu-id="42667-113">Dans le mode de compatibilité DCE, le nom de l’interface doit correspondre au nom de l’interface spécifiée dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="42667-114">Quand vous utilisez le commutateur de compilateur MIDL [**/ACF**](-acf.md), le nom d’interface dans le CCP et le nom d’interface dans le fichier IDL peuvent être différents.</span><span class="sxs-lookup"><span data-stu-id="42667-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="42667-115">*nom de fichier-liste*</span><span class="sxs-lookup"><span data-stu-id="42667-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-116">Spécifie une liste d’un ou plusieurs noms de fichiers d’en-tête en langage C, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="42667-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="42667-117">Le nom de fichier complet, y compris l’extension, doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="42667-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="42667-118">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="42667-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-119">Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="42667-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="42667-120">Les attributs de type valides incluent **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="42667-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="42667-121">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="42667-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-122">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="42667-123">Les attributs de type dans le ACF peuvent uniquement être appliqués aux types précédemment définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="42667-124">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="42667-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-125">Spécifie les attributs qui s’appliquent à la fonction dans son ensemble, par exemple l' **\[** [**\_ État comm**](comm-status.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="42667-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="42667-126">Les attributs de fonction sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="42667-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="42667-127">Séparez plusieurs attributs de fonction par des virgules.</span><span class="sxs-lookup"><span data-stu-id="42667-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="42667-128">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="42667-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-129">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="42667-130">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="42667-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-131">Spécifie les attributs ACF qui s’appliquent à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="42667-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="42667-132">Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="42667-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="42667-133">Séparez les attributs de plusieurs paramètres par des virgules.</span><span class="sxs-lookup"><span data-stu-id="42667-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="42667-134">Les attributs de paramètres ACF sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="42667-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="42667-135">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="42667-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="42667-136">Spécifie un paramètre de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="42667-137">Chaque paramètre de la fonction doit être spécifié dans la même séquence et utiliser le même nom que celui défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42667-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42667-138">Notes</span><span class="sxs-lookup"><span data-stu-id="42667-138">Remarks</span></span>

<span data-ttu-id="42667-139">L’attribut **\[ nocode \]** peut apparaître dans l’en-tête ACF, ou il peut être appliqué à une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="42667-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="42667-140">Lorsque l’attribut **\[ \] nocode** apparaît dans l’en-tête ACF, le code stub du client n’est pas généré pour une fonction distante, sauf s’il a l’attribut de fonction de **\[** [**code**](code.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="42667-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="42667-141">Vous pouvez remplacer l’attribut **\[ nocode \]** dans l’en-tête d’une fonction individuelle en spécifiant l’attribut de **\[ code \]** en tant qu’attribut de fonction.</span><span class="sxs-lookup"><span data-stu-id="42667-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="42667-142">Lorsque l’attribut **\[ nocode \]** apparaît dans la liste d’attributs de la fonction, aucun code stub client n’est généré pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="42667-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="42667-143">Le code stub du client n’est pas généré dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="42667-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="42667-144">L’en-tête ACF comprend l’attribut **\[ nocode \]** .</span><span class="sxs-lookup"><span data-stu-id="42667-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="42667-145">L’attribut **\[ nocode \]** est appliqué à la fonction.</span><span class="sxs-lookup"><span data-stu-id="42667-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="42667-146">L' **\[** attribut [**local**](local.md) **\]** s’applique à la fonction dans le fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="42667-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="42667-147">**\[** [**Code**](code.md) **\]** ou **\[ nocode \]** peut apparaître dans la liste des attributs d’une fonction, et celui que vous choisissez peut apparaître une seule fois.</span><span class="sxs-lookup"><span data-stu-id="42667-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="42667-148">L’attribut **\[ nocode \]** est ignoré lors de la génération de stubs de serveur.</span><span class="sxs-lookup"><span data-stu-id="42667-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="42667-149">Vous ne pouvez pas l’appliquer lors de la génération de stubs de serveur dans le mode de compatibilité DCE.</span><span class="sxs-lookup"><span data-stu-id="42667-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="42667-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42667-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42667-151">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="42667-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="42667-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="42667-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="42667-153">**lui**</span><span class="sxs-lookup"><span data-stu-id="42667-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="42667-154">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="42667-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="42667-155">**code**</span><span class="sxs-lookup"><span data-stu-id="42667-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="42667-156">**État comm. \_**</span><span class="sxs-lookup"><span data-stu-id="42667-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="42667-157">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="42667-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




