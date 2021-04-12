---
title: attribut de code
description: L’attribut \ code \ ACF provoque la génération du code stub client pour les fonctions distantes.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- MIDL, attribut de code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313030"
---
# <a name="code-attribute"></a><span data-ttu-id="88dd8-104">attribut de code</span><span class="sxs-lookup"><span data-stu-id="88dd8-104">code attribute</span></span>

<span data-ttu-id="88dd8-105">L’attribut **\[ code \]** ACF provoque la génération du code stub client pour les fonctions distantes.</span><span class="sxs-lookup"><span data-stu-id="88dd8-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="88dd8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88dd8-107">*ACF-interface-attributs*</span><span class="sxs-lookup"><span data-stu-id="88dd8-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-108">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="88dd8-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="88dd8-109">Les attributs valides incluent le descripteur [**\[ \_ \] automatique**](auto-handle.md) ou [**\[ implicite \_ \]**](implicit-handle.md) et le **\[ code \]**, [**\[ \] le code ou**](nocode.md)l' [**\[ optimisation \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="88dd8-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="88dd8-110">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="88dd8-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-111">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="88dd8-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-112">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="88dd8-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-113">*nom de fichier-liste*</span><span class="sxs-lookup"><span data-stu-id="88dd8-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-114">Spécifie une liste d’un ou plusieurs noms de fichiers d’en-tête C, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="88dd8-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="88dd8-115">Vous devez fournir le nom de fichier complet, y compris l’extension.</span><span class="sxs-lookup"><span data-stu-id="88dd8-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-116">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="88dd8-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-117">Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="88dd8-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="88dd8-118">Les attributs de type valides incluent [**\[ allocate \]**](allocate.md) et [**\[ représentent \_ comme \]**](represent-as.md).</span><span class="sxs-lookup"><span data-stu-id="88dd8-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-119">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="88dd8-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-120">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88dd8-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="88dd8-121">Les attributs de type dans le ACF peuvent être appliqués uniquement aux types précédemment définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88dd8-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-122">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="88dd8-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-123">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction dans son ensemble, par exemple l' [**\[ \_ état \] comm**](comm-status.md).</span><span class="sxs-lookup"><span data-stu-id="88dd8-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="88dd8-124">Les attributs de fonction sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="88dd8-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="88dd8-125">Séparez plusieurs attributs de fonction par des virgules.</span><span class="sxs-lookup"><span data-stu-id="88dd8-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-126">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="88dd8-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-127">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88dd8-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-128">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="88dd8-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-129">Spécifie les attributs ACF qui s’appliquent à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="88dd8-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="88dd8-130">Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="88dd8-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="88dd8-131">Séparez les attributs de plusieurs paramètres par des virgules.</span><span class="sxs-lookup"><span data-stu-id="88dd8-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="88dd8-132">Les attributs de paramètres ACF sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="88dd8-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="88dd8-133">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="88dd8-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88dd8-134">Spécifie un paramètre de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88dd8-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="88dd8-135">Chaque paramètre de la fonction doit être spécifié dans la même séquence et avec le même nom que celui défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="88dd8-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88dd8-136">Notes</span><span class="sxs-lookup"><span data-stu-id="88dd8-136">Remarks</span></span>

<span data-ttu-id="88dd8-137">L’attribut **\[ code \]** peut apparaître dans l’en-tête ACF ou être appliqué à une fonction individuelle.</span><span class="sxs-lookup"><span data-stu-id="88dd8-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="88dd8-138">Lorsque l’attribut **\[ code \]** apparaît dans l’en-tête ACF, le code stub du client est généré pour toutes les fonctions distantes qui n’ont pas l’attribut de fonction [**\[ nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="88dd8-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="88dd8-139">Vous pouvez remplacer l’attribut **\[ code \]** dans l’en-tête d’une fonction individuelle en spécifiant l’attribut **\[ nocode \]** en tant qu’attribut de fonction.</span><span class="sxs-lookup"><span data-stu-id="88dd8-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="88dd8-140">Lorsque l’attribut **\[ code \]** apparaît dans la liste d’attributs de la fonction distante, le code stub du client est généré pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="88dd8-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="88dd8-141">Le code stub du client n’est pas généré dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="88dd8-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="88dd8-142">L’en-tête ACF comprend l’attribut [**\[ nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="88dd8-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="88dd8-143">L’attribut [**\[ nocode \]**](nocode.md) est appliqué à la fonction.</span><span class="sxs-lookup"><span data-stu-id="88dd8-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="88dd8-144">L’attribut [**\[ local \]**](local.md) s’applique à la fonction dans le fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="88dd8-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="88dd8-145">Le **\[ code \]** ou le [**\[ nocode \]**](nocode.md) peut apparaître dans la liste des attributs de l’interface ou de la fonction, mais celui que vous choisissez ne peut apparaître qu’une seule fois dans la liste.</span><span class="sxs-lookup"><span data-stu-id="88dd8-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="88dd8-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88dd8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dd8-147">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="88dd8-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="88dd8-148">**lui**</span><span class="sxs-lookup"><span data-stu-id="88dd8-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="88dd8-149">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="88dd8-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="88dd8-150">**État comm. \_**</span><span class="sxs-lookup"><span data-stu-id="88dd8-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="88dd8-151">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="88dd8-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="88dd8-152">**localisé**</span><span class="sxs-lookup"><span data-stu-id="88dd8-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="88dd8-153">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="88dd8-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="88dd8-154">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="88dd8-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="88dd8-155">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="88dd8-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




