---
title: Syntaxe des variables
description: Utilisez les règles de syntaxe suivantes pour déclarer des variables HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, syntaxe de variable (DirectX HLSL)
- nointerpolation, syntaxe de variable (DirectX HLSL)
- Syntaxe Shared, variable (DirectX HLSL)
- groupshared, syntaxe de variable (DirectX HLSL)
- Syntaxe des variables statiques (DirectX HLSL)
- Syntaxe uniforme et variable (DirectX HLSL)
- volatile, syntaxe de variable (DirectX HLSL)
- Syntaxe précise et variable (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/11/2020
ms.locfileid: "104991045"
---
# <a name="variable-syntax"></a><span data-ttu-id="1efcb-111">Syntaxe des variables</span><span class="sxs-lookup"><span data-stu-id="1efcb-111">Variable Syntax</span></span>

<span data-ttu-id="1efcb-112">Utilisez les règles de syntaxe suivantes pour déclarer des variables HLSL.</span><span class="sxs-lookup"><span data-stu-id="1efcb-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efcb-113">\[*Stockage \_* Nom du type de \] \[ *\_ modificateur* de type de classe \]  \[ *index* \] \[ *: sémantique* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[ *Annotations* \] \[ *= Initial \_ Valeur*                    \]</span><span class="sxs-lookup"><span data-stu-id="1efcb-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1efcb-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1efcb-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efcb-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe de stockage \_*</span><span class="sxs-lookup"><span data-stu-id="1efcb-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="1efcb-116">Modificateurs de classe de stockage facultatifs qui fournissent les indications du compilateur sur la portée de la variable et la durée de vie ; les modificateurs peuvent être spécifiés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="1efcb-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1efcb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1efcb-117">Value</span></span></th>
<th><span data-ttu-id="1efcb-118">Description</span><span class="sxs-lookup"><span data-stu-id="1efcb-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1efcb-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="1efcb-120">Marquez une variable globale comme entrée externe pour le nuanceur. Il s’agit du marquage par défaut pour toutes les variables globales.</span><span class="sxs-lookup"><span data-stu-id="1efcb-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="1efcb-121">Ne peut pas être combiné avec <strong>static</strong>.</span><span class="sxs-lookup"><span data-stu-id="1efcb-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1efcb-122"><strong>nointerpolation</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="1efcb-123">N’interpolez pas les sorties d’un nuanceur de sommets avant de les passer à un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1efcb-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1efcb-124"><strong>établir</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="1efcb-125">Le mot clé <strong>precise</strong> lorsqu’il est appliqué à une variable limite les calculs utilisés pour produire la valeur assignée à cette variable selon les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1efcb-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="1efcb-126">Les opérations distinctes sont conservées séparément.</span><span class="sxs-lookup"><span data-stu-id="1efcb-126">Separate operations are kept separate.</span></span> <span data-ttu-id="1efcb-127">Par exemple, lorsqu’une opération mul et Add peut avoir été fusionnée dans une opération Mad, <strong>precise</strong> force les opérations à rester séparées.</span><span class="sxs-lookup"><span data-stu-id="1efcb-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="1efcb-128">Au lieu de cela, vous devez utiliser explicitement la fonction intrinsèque Mad.</span><span class="sxs-lookup"><span data-stu-id="1efcb-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="1efcb-129">L’ordre des opérations est conservé.</span><span class="sxs-lookup"><span data-stu-id="1efcb-129">Order of operations are maintained.</span></span> <span data-ttu-id="1efcb-130">Lorsque l’ordre des instructions peut être aléatoire pour améliorer les performances, la <strong>précision</strong> garantit que le compilateur conserve l’ordre écrit.</span><span class="sxs-lookup"><span data-stu-id="1efcb-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="1efcb-131">Les opérations non sécurisées IEEE sont restreintes.</span><span class="sxs-lookup"><span data-stu-id="1efcb-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="1efcb-132">Là où le compilateur peut avoir utilisé des opérations mathématiques rapides qui ne concernent pas les valeurs NaN (not a Number) et INF (infini), force <strong>précisément</strong> les exigences IEEE relatives aux valeurs NaN et INF à respecter.</span><span class="sxs-lookup"><span data-stu-id="1efcb-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="1efcb-133">Sans <strong>précision</strong>, ces optimisations et opérations mathématiques ne sont pas compatibles IEEE.</span><span class="sxs-lookup"><span data-stu-id="1efcb-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="1efcb-134">La qualification d’une variable <strong>précise</strong> ne rend pas les opérations qui utilisent la variable avec <strong>précision</strong>.</span><span class="sxs-lookup"><span data-stu-id="1efcb-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="1efcb-135">Étant donné que <strong>precise</strong> se propage uniquement aux opérations qui contribuent aux valeurs affectées à la variable qualifiée <strong>précise</strong>, <strong>il peut être</strong> difficile de déterminer correctement les calculs souhaités. nous vous recommandons donc de marquer les sorties du nuanceur avec <strong>précision</strong> directement là où vous les déclarez, si celles-ci se trouvent sur un champ de structure, ou sur un paramètre de sortie ou le type de retour de</span><span class="sxs-lookup"><span data-stu-id="1efcb-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="1efcb-136">La possibilité de contrôler les optimisations de cette façon maintient l’invariance de résultat pour la variable de sortie modifiée en désactivant les optimisations qui peuvent affecter les résultats finaux en raison de différences de différences de précision accumulée.</span><span class="sxs-lookup"><span data-stu-id="1efcb-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="1efcb-137">Il est utile lorsque vous souhaitez que les nuanceurs de facettes maintiennent des jointures de patch hermétiques ou des valeurs de profondeur de correspondance sur plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="1efcb-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="1efcb-138">[Exemple de code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="1efcb-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1efcb-139"><strong>partagé</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="1efcb-140">Marquer une variable pour le partage entre les effets ; Il s’agit d’un indicateur pour le compilateur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1efcb-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="1efcb-142">Marquez une variable pour la mémoire partagée de groupe de threads pour les nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="1efcb-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="1efcb-143">Dans D3D10, la taille totale maximale de toutes les variables avec la classe de stockage groupshared est de 16 Ko, dans D3D11 la taille maximale est de 32 Ko.</span><span class="sxs-lookup"><span data-stu-id="1efcb-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="1efcb-144">Consultez les exemples.</span><span class="sxs-lookup"><span data-stu-id="1efcb-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1efcb-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="1efcb-146">Marquez une variable locale pour qu’elle soit initialisée une fois et persiste entre les appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="1efcb-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="1efcb-147">Si la déclaration n’inclut pas d’initialiseur, la valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1efcb-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="1efcb-148">Une variable globale marquée comme <strong>static</strong> n’est pas visible pour une application.</span><span class="sxs-lookup"><span data-stu-id="1efcb-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1efcb-149"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="1efcb-150">Marquer une variable dont les données sont constantes tout au long de l’exécution d’un nuanceur (par exemple, une couleur de matériau dans un nuanceur de sommets); les variables globales sont considérées comme <strong>uniformes</strong> par défaut.</span><span class="sxs-lookup"><span data-stu-id="1efcb-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1efcb-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="1efcb-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="1efcb-152">Marquer une variable qui change fréquemment ; Il s’agit d’un indicateur pour le compilateur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="1efcb-153">Ce modificateur de classe de stockage s’applique uniquement à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="1efcb-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1efcb-154">Le compilateur HLSL ignore actuellement ce modificateur de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="1efcb-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="1efcb-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificateur de type*</span><span class="sxs-lookup"><span data-stu-id="1efcb-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-156">Modificateur de type variable facultatif.</span><span class="sxs-lookup"><span data-stu-id="1efcb-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="1efcb-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="1efcb-157">Value</span></span>             | <span data-ttu-id="1efcb-158">Description</span><span class="sxs-lookup"><span data-stu-id="1efcb-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efcb-159">**const**</span><span class="sxs-lookup"><span data-stu-id="1efcb-159">**const**</span></span>         | <span data-ttu-id="1efcb-160">Marquer une variable qui ne peut pas être modifiée par un nuanceur, par conséquent, elle doit être initialisée dans la déclaration de la variable.</span><span class="sxs-lookup"><span data-stu-id="1efcb-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="1efcb-161">Les variables globales sont considérées comme **const** par défaut (supprimez ce comportement en fournissant l’indicateur/GEC au compilateur).</span><span class="sxs-lookup"><span data-stu-id="1efcb-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="1efcb-162">**ligne \_ principale**</span><span class="sxs-lookup"><span data-stu-id="1efcb-162">**row\_major**</span></span>    | <span data-ttu-id="1efcb-163">Marquer une variable qui stocke quatre composants sur une seule ligne afin qu’ils puissent être stockés dans un seul registre de constantes.</span><span class="sxs-lookup"><span data-stu-id="1efcb-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="1efcb-164">**colonne \_ principale**</span><span class="sxs-lookup"><span data-stu-id="1efcb-164">**column\_major**</span></span> | <span data-ttu-id="1efcb-165">Marquez une variable qui stocke 4 composants dans une seule colonne pour optimiser les mathématiques de matrice.</span><span class="sxs-lookup"><span data-stu-id="1efcb-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="1efcb-166">Si vous ne spécifiez pas de valeur de modificateur de type, le compilateur utilise la **colonne \_ principale** comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1efcb-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="1efcb-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Entrer*</span><span class="sxs-lookup"><span data-stu-id="1efcb-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-168">Tout type HLSL listé dans [types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="1efcb-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nom* \[ *Index*\]</span><span class="sxs-lookup"><span data-stu-id="1efcb-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-170">Chaîne ASCII qui identifie de façon unique une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="1efcb-171">Pour définir un tableau facultatif, utilisez **index** pour la taille du tableau, qui est un entier positif = 1.</span><span class="sxs-lookup"><span data-stu-id="1efcb-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Équivalent*</span><span class="sxs-lookup"><span data-stu-id="1efcb-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-173">Informations d’utilisation de paramètre facultatives, utilisées par le compilateur pour lier les entrées et sorties du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="1efcb-174">Il existe plusieurs [sémantiques](dx-graphics-hlsl-semantics.md) prédéfinies pour les nuanceurs de sommets et de pixels.</span><span class="sxs-lookup"><span data-stu-id="1efcb-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="1efcb-175">Le compilateur ignore la sémantique, sauf si elles sont déclarées sur une variable globale, ou un paramètre passé dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="1efcb-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-177">Mot clé facultatif pour la compression manuelle des constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="1efcb-178">Consultez [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="1efcb-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Annuler*</span><span class="sxs-lookup"><span data-stu-id="1efcb-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-180">Mot clé facultatif permettant d’assigner manuellement une variable de nuanceur à un registre particulier.</span><span class="sxs-lookup"><span data-stu-id="1efcb-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="1efcb-181">Consultez [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="1efcb-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation (s)*</span><span class="sxs-lookup"><span data-stu-id="1efcb-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-183">Métadonnées facultatives, sous la forme d’une chaîne, attachées à une variable globale.</span><span class="sxs-lookup"><span data-stu-id="1efcb-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="1efcb-184">Une annotation est utilisée par l’infrastructure Effect et est ignorée par le langage HLSL. Pour plus d’informations sur la syntaxe, consultez [syntaxe d’annotation](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="1efcb-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="1efcb-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valeur initiale*</span><span class="sxs-lookup"><span data-stu-id="1efcb-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="1efcb-186">Valeur (s) initiale facultative (s); le nombre de valeurs doit correspondre au nombre de composants dans le *type*.</span><span class="sxs-lookup"><span data-stu-id="1efcb-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="1efcb-187">Chaque variable globale marquée **extern** doit être initialisée avec une valeur littérale ; chaque variable marquée comme **static** doit être initialisée avec une constante.</span><span class="sxs-lookup"><span data-stu-id="1efcb-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="1efcb-188">Les variables globales qui ne sont pas marquées comme **static** ou **extern** ne sont pas compilées dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="1efcb-189">Le compilateur ne définit pas automatiquement les valeurs par défaut pour les variables globales et ne peut pas les utiliser dans les optimisations.</span><span class="sxs-lookup"><span data-stu-id="1efcb-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="1efcb-190">Pour initialiser ce type de variable globale, utilisez la réflexion pour obtenir sa valeur, puis copiez la valeur dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="1efcb-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="1efcb-191">Par exemple, vous pouvez utiliser la méthode [**ID3D11ShaderReflection :: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) pour obtenir la variable, utiliser la méthode [**ID3D11ShaderReflectionVariable :: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) pour obtenir la description de la variable de nuanceur et obtenir la valeur initiale du membre **DefaultValue** de la structure DESC de la [**\_ \_ variable \_ de nuanceur d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) .</span><span class="sxs-lookup"><span data-stu-id="1efcb-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="1efcb-192">Pour copier la valeur dans la mémoire tampon constante, vous devez vous assurer que la mémoire tampon a été créée avec l’accès en écriture de l’UC ([**d3d11 \_ \_ l’accès \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)en écriture de l’UC).</span><span class="sxs-lookup"><span data-stu-id="1efcb-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="1efcb-193">Pour plus d’informations sur la création d’une mémoire tampon constante, consultez [How to : Create a constant buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="1efcb-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="1efcb-194">Vous pouvez également utiliser l' [infrastructure Effects](../direct3d11/d3d11-graphics-programming-guide-effects.md) pour traiter automatiquement la réflexion et définir la valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="1efcb-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="1efcb-195">Par exemple, vous pouvez utiliser la méthode [**ID3DX11EffectPass :: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .</span><span class="sxs-lookup"><span data-stu-id="1efcb-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1efcb-196">Exemples</span><span class="sxs-lookup"><span data-stu-id="1efcb-196">Examples</span></span>

<span data-ttu-id="1efcb-197">Voici plusieurs exemples de déclarations de variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1efcb-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="1efcb-198">Groupe partagé</span><span class="sxs-lookup"><span data-stu-id="1efcb-198">Group Shared</span></span>

<span data-ttu-id="1efcb-199">Le langage HLSL permet aux threads d’un nuanceur de calcul d’échanger des valeurs via la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1efcb-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="1efcb-200">Le langage HLSL fournit des primitives de cloisonnement telles que [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), et ainsi de suite pour garantir l’ordre correct des lectures et des écritures dans la mémoire partagée dans le nuanceur et pour éviter les concurrences de données.</span><span class="sxs-lookup"><span data-stu-id="1efcb-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="1efcb-201">Le matériel exécute des threads dans des groupes (distorsions ou frontaux Wave), et la synchronisation de cloisonnement peut parfois être omise pour améliorer les performances lorsque seuls les threads qui appartiennent au même groupe sont corrects.</span><span class="sxs-lookup"><span data-stu-id="1efcb-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="1efcb-202">Toutefois, nous déconseillons vivement cette omission pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="1efcb-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="1efcb-203">Cette omission entraîne un code non portable, qui peut ne pas fonctionner sur du matériel et ne fonctionne pas sur les rastériseurs logiciels qui exécutent généralement des threads dans des groupes plus petits.</span><span class="sxs-lookup"><span data-stu-id="1efcb-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="1efcb-204">Les améliorations de performances que vous pourriez atteindre avec cette omission seront mineures par rapport à l’utilisation de la barrière All-threads.</span><span class="sxs-lookup"><span data-stu-id="1efcb-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="1efcb-205">Dans Direct3D 10, il n’existe pas de synchronisation des threads lors de l’écriture dans **groupshared**, ce qui signifie que chaque thread est limité à un emplacement unique dans un tableau pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="1efcb-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="1efcb-206">Utilisez la valeur système [SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) pour indexer dans ce tableau lors de l’écriture afin de garantir que deux threads ne peuvent pas entrer en conflit.</span><span class="sxs-lookup"><span data-stu-id="1efcb-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="1efcb-207">En termes de lecture, tous les threads ont accès à l’ensemble du tableau pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="1efcb-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="1efcb-208">Colis</span><span class="sxs-lookup"><span data-stu-id="1efcb-208">Packing</span></span>

<span data-ttu-id="1efcb-209">Compresser les sous-composants des vecteurs et des scalaires dont la taille est suffisamment grande pour empêcher le franchissement des limites du Registre.</span><span class="sxs-lookup"><span data-stu-id="1efcb-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="1efcb-210">Par exemple, ils sont tous valides :</span><span class="sxs-lookup"><span data-stu-id="1efcb-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="1efcb-211">Impossible de mélanger les types de compression.</span><span class="sxs-lookup"><span data-stu-id="1efcb-211">Cannot mix packing types.</span></span>

<span data-ttu-id="1efcb-212">À l’instar du mot clé Register, un packoffset peut être spécifique à Target.</span><span class="sxs-lookup"><span data-stu-id="1efcb-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="1efcb-213">La compression des sous-composants est uniquement disponible avec le mot clé packoffset, pas le mot clé Register.</span><span class="sxs-lookup"><span data-stu-id="1efcb-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="1efcb-214">Dans une déclaration CBuffer, le mot clé Register est ignoré pour les cibles Direct3D 10, car il est supposé être pour la compatibilité multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="1efcb-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="1efcb-215">Les éléments empaquetés peuvent se chevaucher et le compilateur n’émet aucune erreur ni aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="1efcb-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="1efcb-216">Dans cet exemple, élément2 et Element3 se chevauchent avec Element1. x et Element1. y.</span><span class="sxs-lookup"><span data-stu-id="1efcb-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="1efcb-217">Un exemple qui utilise packoffset est : [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="1efcb-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1efcb-218">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1efcb-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1efcb-219">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1efcb-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

