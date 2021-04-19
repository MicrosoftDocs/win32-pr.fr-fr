---
title: Spécification de signatures racine en langage HLSL
description: La spécification de signatures racines dans le modèle de nuanceur HLSL 5,1 est une alternative à leur spécification dans du code C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492281"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="3ebce-103">Spécification de signatures racine en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="3ebce-104">La spécification de signatures racines dans le modèle de nuanceur HLSL 5,1 est une alternative à leur spécification dans du code C++.</span><span class="sxs-lookup"><span data-stu-id="3ebce-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="3ebce-105">Exemple de signature racine HLSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="3ebce-106">Signature racine version 1,0</span><span class="sxs-lookup"><span data-stu-id="3ebce-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="3ebce-107">Signature racine version 1.1</span><span class="sxs-lookup"><span data-stu-id="3ebce-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="3ebce-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="3ebce-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="3ebce-109">Constantes racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="3ebce-110">Visibilité</span><span class="sxs-lookup"><span data-stu-id="3ebce-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="3ebce-111">CBV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="3ebce-112">SRV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="3ebce-113">UAV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="3ebce-114">Tableau du descripteur</span><span class="sxs-lookup"><span data-stu-id="3ebce-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="3ebce-115">Échantillonneur statique</span><span class="sxs-lookup"><span data-stu-id="3ebce-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="3ebce-116">Compilation d’une signature racine HLSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="3ebce-117">Manipulation des signatures racines avec le compilateur FXC</span><span class="sxs-lookup"><span data-stu-id="3ebce-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="3ebce-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ebce-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="3ebce-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ebce-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="3ebce-120">Exemple de signature racine HLSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="3ebce-121">Une signature racine peut être spécifiée en langage HLSL en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ebce-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="3ebce-122">La chaîne contient une collection de clauses séparées par des virgules qui décrivent les composants constitutifs de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="3ebce-123">La signature racine doit être identique sur les nuanceurs pour un objet d’état de pipeline (PSO).</span><span class="sxs-lookup"><span data-stu-id="3ebce-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="3ebce-124">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="3ebce-125">Signature racine version 1,0</span><span class="sxs-lookup"><span data-stu-id="3ebce-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="3ebce-126">Cette définition donne la signature racine suivante, en notant :</span><span class="sxs-lookup"><span data-stu-id="3ebce-126">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="3ebce-127">Utilisation des paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="3ebce-127">The use of default parameters.</span></span>
-   <span data-ttu-id="3ebce-128">B0 et (B0, Space = 1) ne sont pas en conflit</span><span class="sxs-lookup"><span data-stu-id="3ebce-128">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="3ebce-129">U0 est visible uniquement pour le nuanceur Geometry</span><span class="sxs-lookup"><span data-stu-id="3ebce-129">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="3ebce-130">U4 et U5 ont pour alias le même descripteur dans un segment de mémoire</span><span class="sxs-lookup"><span data-stu-id="3ebce-130">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![signature racine spécifiée à l’aide du langage de nuanceur de haut niveau](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a><span data-ttu-id="3ebce-132">Signature racine version 1.1</span><span class="sxs-lookup"><span data-stu-id="3ebce-132">Root Signature Version 1.1</span></span>

<span data-ttu-id="3ebce-133">La [signature racine Version 1,1](root-signature-version-1-1.md) permet d’optimiser les pilotes sur les descripteurs de signature racine et les données.</span><span class="sxs-lookup"><span data-stu-id="3ebce-133">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="3ebce-134">Le langage de signature racine HLSL correspond étroitement aux API de signature racine C++ et a une puissance expressif équivalente.</span><span class="sxs-lookup"><span data-stu-id="3ebce-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="3ebce-135">La signature racine est spécifiée en tant que séquence de clauses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3ebce-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="3ebce-136">L’ordre des clauses est important, car l’ordre d’analyse détermine la position de l’emplacement dans la signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="3ebce-137">Chaque clause accepte un ou plusieurs paramètres nommés.</span><span class="sxs-lookup"><span data-stu-id="3ebce-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="3ebce-138">Toutefois, l’ordre des paramètres n’est pas important.</span><span class="sxs-lookup"><span data-stu-id="3ebce-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="3ebce-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="3ebce-139">RootFlags</span></span>

<span data-ttu-id="3ebce-140">La clause facultative *RootFlags* prend la valeur 0 (valeur par défaut pour indiquer qu’il n’y a pas d’indicateur), ou une ou plusieurs valeurs d’indicateurs racines prédéfinies, connectées via l’opérateur ou' \| '.</span><span class="sxs-lookup"><span data-stu-id="3ebce-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="3ebce-141">Les valeurs d’indicateur racine autorisées sont définies par les [**\_ \_ \_ indicateurs de signature racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="3ebce-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="3ebce-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="3ebce-143">Constantes racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-143">Root Constants</span></span>

<span data-ttu-id="3ebce-144">La clause *RootConstants* spécifie des constantes racine dans la signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="3ebce-145">Deux paramètres obligatoires sont : *num32BitConstants* et *bReg* (le registre correspondant à *BaseShaderRegister* dans les API C++) du *CBuffer*.</span><span class="sxs-lookup"><span data-stu-id="3ebce-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="3ebce-146">Les paramètres espace (*RegisterSpace* dans les API c++) et visibilité (*ShaderVisibility* en c++) sont facultatifs, et les valeurs par défaut sont :</span><span class="sxs-lookup"><span data-stu-id="3ebce-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="3ebce-147">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="3ebce-148">Visibilité</span><span class="sxs-lookup"><span data-stu-id="3ebce-148">Visibility</span></span>

<span data-ttu-id="3ebce-149">Visibility est un paramètre facultatif qui peut avoir l’une des valeurs de la [**\_ \_ visibilité du nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="3ebce-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="3ebce-150">\_La visibilité \_ du nuanceur diffuse tous les arguments racine à tous les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="3ebce-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="3ebce-151">Sur un matériel, cela n’a aucun coût, mais sur un autre matériel, il y a un coût pour la duplication des données à toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ebce-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="3ebce-152">La définition de l’une des options, comme \_ le vertex de visibilité du nuanceur \_ , limite l’argument racine à une seule étape de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ebce-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="3ebce-153">La définition des arguments racine sur des étapes de nuanceur uniques permet d’utiliser le même nom de liaison à différentes étapes.</span><span class="sxs-lookup"><span data-stu-id="3ebce-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="3ebce-154">Par exemple, une liaison SRV de `t0,SHADER_VISIBILITY_VERTEX` et une liaison SRV de sont `t0,SHADER_VISIBILITY_PIXEL` valides.</span><span class="sxs-lookup"><span data-stu-id="3ebce-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="3ebce-155">Toutefois, si le paramètre de visibilité était `t0,SHADER_VISIBILITY_ALL` pour l’une des liaisons, la signature racine n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3ebce-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="3ebce-156">CBV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-156">Root-level CBV</span></span>

<span data-ttu-id="3ebce-157">La `CBV` clause (vue de la mémoire tampon constante) spécifie une entrée de registre de la mémoire tampon de l’enregistrement b-Register au niveau de la racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="3ebce-158">Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="3ebce-159">SRV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-159">Root-level SRV</span></span>

<span data-ttu-id="3ebce-160">La `SRV` clause (vue de ressource Shader) spécifie une entrée de Registre SRV t-Register de niveau racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="3ebce-161">Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="3ebce-162">UAV au niveau de la racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-162">Root-level UAV</span></span>

<span data-ttu-id="3ebce-163">La `UAV` clause (vue d’accès non ordonnée) spécifie une entrée de Registre UAV u-Register au niveau de la racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="3ebce-164">Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="3ebce-165">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="3ebce-166">Tableau du descripteur</span><span class="sxs-lookup"><span data-stu-id="3ebce-166">Descriptor Table</span></span>

<span data-ttu-id="3ebce-167">La `DescriptorTable` clause est elle-même une liste de clauses de table de descripteur séparées par des virgules, ainsi qu’un paramètre de visibilité facultatif.</span><span class="sxs-lookup"><span data-stu-id="3ebce-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="3ebce-168">Les clauses *DescriptorTable* incluent CBV, SRV, UAV et échantillonner.</span><span class="sxs-lookup"><span data-stu-id="3ebce-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="3ebce-169">Notez que leurs paramètres diffèrent de ceux des clauses de niveau racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="3ebce-170">La table du descripteur `CBV` a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3ebce-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="3ebce-171">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="3ebce-172">Le paramètre obligatoire *bReg* spécifie le début de l’reg de la plage CBuffer.</span><span class="sxs-lookup"><span data-stu-id="3ebce-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="3ebce-173">Le paramètre *numDescriptors* spécifie le nombre de descripteurs dans la plage de CBuffer contiguës ; la valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="3ebce-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="3ebce-174">L’entrée déclare une plage CBuffer ` [Reg, Reg + numDescriptors - 1]` , lorsque *numDescriptors* est un nombre.</span><span class="sxs-lookup"><span data-stu-id="3ebce-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="3ebce-175">Si *numDescriptors* est égal à « Unlimited », la plage est `[Reg, UINT_MAX]` , ce qui signifie que l’application doit s’assurer qu’elle ne référence pas de zone hors limites.</span><span class="sxs-lookup"><span data-stu-id="3ebce-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="3ebce-176">Le champ *offset* représente le paramètre *OffsetInDescriptorsFromTableStart* dans les API C++, autrement dit, l’offset (dans descripteurs) à partir du début de la table.</span><span class="sxs-lookup"><span data-stu-id="3ebce-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="3ebce-177">Si le décalage est défini sur le descripteur de décalage de la plage de descripteurs \_ \_ \_ (valeur par défaut), cela signifie que la plage se trouve directement après la plage précédente.</span><span class="sxs-lookup"><span data-stu-id="3ebce-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="3ebce-178">Toutefois, l’entrée de décalages spécifiques permet aux plages de se chevaucher l’une de l’autre, ce qui permet d’enregistrer les alias.</span><span class="sxs-lookup"><span data-stu-id="3ebce-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="3ebce-179">La table du descripteur `SRV` a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3ebce-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="3ebce-180">Cela est similaire à l’entrée du tableau du descripteur `CBV` , à la différence que la plage spécifiée concerne les vues des ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ebce-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="3ebce-181">La table du descripteur `UAV` a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3ebce-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="3ebce-182">Cela est similaire à l’entrée de table du descripteur `CBV` , à la différence que la plage spécifiée concerne les vues d’accès non ordonnées.</span><span class="sxs-lookup"><span data-stu-id="3ebce-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="3ebce-183">La table du descripteur `Sampler` a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3ebce-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="3ebce-184">Cela est similaire à l’entrée de table du descripteur `CBV` , sauf que la plage spécifiée est pour les échantillonneurs de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ebce-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="3ebce-185">Notez que les échantillonneurs ne peuvent pas être mélangés avec d’autres types de descripteurs dans la même table de descripteurs (puisqu’ils se trouvent dans un tas de descripteur distinct).</span><span class="sxs-lookup"><span data-stu-id="3ebce-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="3ebce-186">Échantillonneur statique</span><span class="sxs-lookup"><span data-stu-id="3ebce-186">Static Sampler</span></span>

<span data-ttu-id="3ebce-187">L’échantillonneur statique représente la structure de l' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="3ebce-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="3ebce-188">Le paramètre obligatoire pour *StaticSampler* est un fichier de Registre scalaire, d’échantillonneur. Les autres paramètres sont facultatifs avec les valeurs par défaut indiquées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3ebce-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="3ebce-189">La plupart des champs acceptent un ensemble d’énumérations prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="3ebce-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="3ebce-190">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="3ebce-191">Les options des paramètres sont très similaires aux appels de l’API C++, à l’exception de *BorderColor*, qui est limité à une énumération en HLSL.</span><span class="sxs-lookup"><span data-stu-id="3ebce-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="3ebce-192">Le champ de filtre peut être l’un des [**\_ filtres D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span><span class="sxs-lookup"><span data-stu-id="3ebce-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="3ebce-193">Les champs d’adresse peuvent tous être un [**\_ mode d' \_ adresse \_ de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="3ebce-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="3ebce-194">La fonction de comparaison peut être l’une des fonctions de [**\_ comparaison \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="3ebce-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="3ebce-195">Le champ de couleur de la bordure peut être une [**\_ \_ \_ couleur de bordure statique D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="3ebce-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="3ebce-196">La visibilité peut être l’une des D3D12 de la [**\_ \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="3ebce-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="3ebce-197">Compilation d’une signature racine HLSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="3ebce-198">Il existe deux mécanismes pour compiler une signature racine HLSL.</span><span class="sxs-lookup"><span data-stu-id="3ebce-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="3ebce-199">Tout d’abord, il est possible d’attacher une chaîne de signature racine à un nuanceur particulier par le biais de l’attribut *RootSignature* (dans l’exemple suivant, à l’aide du point d’entrée **MyRS1** ) :</span><span class="sxs-lookup"><span data-stu-id="3ebce-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="3ebce-200">Le compilateur crée et vérifie l’objet blob de signature racine pour le nuanceur et l’incorpore en même temps que le code d’octet du nuanceur dans l’objet blob de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ebce-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="3ebce-201">Le compilateur prend en charge la syntaxe de signature racine pour le Shader Model 5,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3ebce-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="3ebce-202">Si une signature racine est incorporée dans un nuanceur de modèle de nuanceur 5,0 et que le nuanceur est envoyé au runtime D3D11, contrairement à D3D12, la partie de la signature racine est ignorée en mode silencieux par D3D11.</span><span class="sxs-lookup"><span data-stu-id="3ebce-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="3ebce-203">L’autre mécanisme consiste à créer un objet blob de signature racine autonome, peut-être à le réutiliser avec un grand ensemble de nuanceurs, ce qui économise de l’espace.</span><span class="sxs-lookup"><span data-stu-id="3ebce-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="3ebce-204">L' [outil Effect-compiler Tool](/windows/desktop/direct3dtools/fxc) (fxc) prend en charge les modèles de nuanceur **rootsig \_ 1 \_ 0** et **rootsig \_ 1 \_ 1** .</span><span class="sxs-lookup"><span data-stu-id="3ebce-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="3ebce-205">Le nom de la chaîne définie est spécifié à l’aide de l’argument/E habituel.</span><span class="sxs-lookup"><span data-stu-id="3ebce-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="3ebce-206">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3ebce-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="3ebce-207">Notez que la définition de la chaîne de signature racine peut également être passée sur la ligne de commande, par exemple/D MyRS1 = "...".</span><span class="sxs-lookup"><span data-stu-id="3ebce-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="3ebce-208">Manipulation des signatures racines avec le compilateur FXC</span><span class="sxs-lookup"><span data-stu-id="3ebce-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="3ebce-209">Le compilateur FXC crée un code d’octet de nuanceur à partir de fichiers sources HLSL.</span><span class="sxs-lookup"><span data-stu-id="3ebce-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="3ebce-210">Il existe un grand nombre de paramètres facultatifs pour ce compilateur, reportez-vous à l' [outil Effect-compiler](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="3ebce-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="3ebce-211">Pour la gestion des signatures racines créées par HLSL, le tableau suivant fournit des exemples d’utilisation de FXC.</span><span class="sxs-lookup"><span data-stu-id="3ebce-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="3ebce-212">Courbes</span><span class="sxs-lookup"><span data-stu-id="3ebce-212">Line</span></span> | <span data-ttu-id="3ebce-213">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="3ebce-213">Command line</span></span>                                                                 | <span data-ttu-id="3ebce-214">Description</span><span class="sxs-lookup"><span data-stu-id="3ebce-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebce-215">1</span><span class="sxs-lookup"><span data-stu-id="3ebce-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="3ebce-216">Compile un nuanceur pour la cible de nuanceur de pixels 5,1, la source du nuanceur se trouve dans le fichier shaderWithRootSig. HLSL, qui comprend une signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="3ebce-217">Le nuanceur et la signature racine sont compilés en tant qu’objets BLOB distincts dans le fichier binaire RS1. FXO.</span><span class="sxs-lookup"><span data-stu-id="3ebce-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="3ebce-218">2</span><span class="sxs-lookup"><span data-stu-id="3ebce-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="3ebce-219">Extrait la signature racine du fichier créé par la ligne 1, de sorte que le fichier RS1. RS. FXO contient simplement une signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="3ebce-220">3</span><span class="sxs-lookup"><span data-stu-id="3ebce-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="3ebce-221">Supprime la signature racine du fichier créé par la ligne 1, de sorte que le fichier RS1. decapad. FXO contient un shader sans signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="3ebce-222">4</span><span class="sxs-lookup"><span data-stu-id="3ebce-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="3ebce-223">Combine un nuanceur et une signature racine qui se trouvent dans des fichiers distincts en un fichier binaire contenant les deux objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ebce-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="3ebce-224">Dans cet exemple, RS1. New. FX0 est identique à RS1. FX0 à la ligne 1.</span><span class="sxs-lookup"><span data-stu-id="3ebce-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="3ebce-225">5</span><span class="sxs-lookup"><span data-stu-id="3ebce-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="3ebce-226">Crée un fichier binaire de signature racine autonome à partir d’une source qui peut contenir plus qu’une seule signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="3ebce-227">Notez la \_ cible rootsig 1 \_ 0 et RS1 est le nom de la chaîne de macro de signature racine ( \# define) dans le fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="3ebce-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="3ebce-228">Les fonctionnalités disponibles via FXC sont également disponibles par programme à l’aide de la fonction [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="3ebce-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="3ebce-229">Cet appel compile un nuanceur avec une signature racine ou une signature racine autonome (en définissant la cible rootsig \_ 1 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="3ebce-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="3ebce-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) et [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) peuvent extraire et attacher des signatures racines à un objet BLOB existant.</span><span class="sxs-lookup"><span data-stu-id="3ebce-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span>  <span data-ttu-id="3ebce-231">\_ \_ La signature racine d’objet BLOB D3D \_ est utilisée pour spécifier le type de composant blob de signature racine.</span><span class="sxs-lookup"><span data-stu-id="3ebce-231">D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="3ebce-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) supprime la signature racine (à l’aide de l' \_ \_ \_ indicateur de signature racine D3DCOMPILER Strip) de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ebce-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="3ebce-233">Notes</span><span class="sxs-lookup"><span data-stu-id="3ebce-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="3ebce-234">Alors que la compilation hors connexion des nuanceurs est fortement recommandée, si les nuanceurs doivent être compilés au moment de l’exécution, reportez-vous aux remarques relatives à [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="3ebce-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="3ebce-235">Les ressources HLSL existantes n’ont pas besoin d’être modifiées pour gérer les signatures racines à utiliser avec elles.</span><span class="sxs-lookup"><span data-stu-id="3ebce-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3ebce-236">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ebce-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ebce-237">Indexation dynamique à l’aide de HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="3ebce-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="3ebce-238">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3ebce-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="3ebce-239">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="3ebce-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="3ebce-240">Liaison de ressource dans HSL</span><span class="sxs-lookup"><span data-stu-id="3ebce-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="3ebce-241">Signatures racine</span><span class="sxs-lookup"><span data-stu-id="3ebce-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="3ebce-242">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="3ebce-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="3ebce-243">Valeur de référence du stencil spécifié par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="3ebce-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="3ebce-244">Chargements de vues d’accès non ordonnées typées</span><span class="sxs-lookup"><span data-stu-id="3ebce-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
