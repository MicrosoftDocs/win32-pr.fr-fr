---
title: Constantes de nuanceur (HLSL)
description: Dans le nuancier modèle 4, les constantes de nuanceur sont stockées dans une ou plusieurs ressources de mémoire tampon en mémoire.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- mémoire tampon constante
- mémoire tampon de texture
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129958"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="1c8ae-107">Constantes de nuanceur (HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c8ae-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="1c8ae-108">Dans le nuancier modèle 4, les constantes de nuanceur sont stockées dans une ou plusieurs ressources de mémoire tampon en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="1c8ae-109">Ils peuvent être organisés en deux types de mémoires tampons : des mémoires tampons constantes (cbuffers) et des mémoires tampons de texture (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="1c8ae-110">Les mémoires tampons constantes sont optimisées pour l’utilisation de variables constantes, ce qui est caractérisé par un accès à latence faible et des mises à jour plus fréquentes de l’UC.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="1c8ae-111">Pour cette raison, des restrictions supplémentaires sur la taille, la disposition et l’accès s’appliquent à ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="1c8ae-112">Les mémoires tampons de texture sont accessibles comme les textures et s’exécutent mieux pour les données indexées arbitrairement.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="1c8ae-113">Quel que soit le type de ressource que vous utilisez, il n’existe aucune limite quant au nombre de mémoires tampons constantes ou de mémoires tampons de texture qu’une application peut créer.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="1c8ae-114">La déclaration d’une mémoire tampon constante ou d’une mémoire tampon de texture ressemble beaucoup à celle d’une déclaration de structure en C, avec l’ajout des mots clés **Register** et **packoffset** pour l’affectation manuelle des registres ou l’empaquetage des données.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8ae-115">*BufferType* \[ *Nom* \] \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . XYZW) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="1c8ae-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1c8ae-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c8ae-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c8ae-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="1c8ae-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="1c8ae-118">\[dans \] le type de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="1c8ae-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="1c8ae-119">BufferType</span></span> | <span data-ttu-id="1c8ae-120">Description</span><span class="sxs-lookup"><span data-stu-id="1c8ae-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="1c8ae-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="1c8ae-121">cbuffer</span></span>    | <span data-ttu-id="1c8ae-122">mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="1c8ae-122">constant buffer</span></span> |
| <span data-ttu-id="1c8ae-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="1c8ae-123">tbuffer</span></span>    | <span data-ttu-id="1c8ae-124">mémoire tampon de texture</span><span class="sxs-lookup"><span data-stu-id="1c8ae-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1c8ae-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="1c8ae-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="1c8ae-126">\[dans \] une chaîne ASCII facultative, contenant un nom de mémoire tampon unique.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="1c8ae-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**inscrire**(b \# )</span><span class="sxs-lookup"><span data-stu-id="1c8ae-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="1c8ae-128">\[dans le \] mot clé facultatif, utilisé pour empaqueter manuellement des données constantes.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="1c8ae-129">Les constantes peuvent être empaquetées dans un registre uniquement dans une mémoire tampon constante, où le registre de départ est donné par le numéro de Registre ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="1c8ae-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="1c8ae-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="1c8ae-131">\[dans \] une déclaration de variable, semblable à une déclaration de membre de structure.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="1c8ae-132">Il peut s’agir d’un objet de type ou d’effet HLSL (à l’exception d’une texture ou d’un objet échantillonneur).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="1c8ae-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . XYZW)</span><span class="sxs-lookup"><span data-stu-id="1c8ae-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="1c8ae-134">\[dans le \] mot clé facultatif, utilisé pour empaqueter manuellement des données constantes.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="1c8ae-135">Les constantes peuvent être compressées dans n’importe quelle mémoire tampon constante, où le numéro de Registre est donné par ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="1c8ae-136">La compression de sous-composant (à l’aide de XYZW swizzling) est disponible pour les constantes dont la taille s’ajuste à un seul registre (ne pas traverser une limite de registre).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="1c8ae-137">Par exemple, un float4 ne peut pas être empaqueté dans un seul registre à partir du composant y car il ne tient pas dans un registre à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c8ae-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c8ae-138">Remarks</span></span>

<span data-ttu-id="1c8ae-139">Les mémoires tampons constantes réduisent la bande passante requise pour mettre à jour les constantes de nuanceur en permettant aux constantes de nuanceur d’être regroupées et validées en même temps plutôt que d’effectuer des appels individuels pour valider chaque constante séparément.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="1c8ae-140">Une mémoire tampon constante est une ressource tampon spécialisée accessible comme une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="1c8ae-141">Chaque mémoire tampon constante peut contenir jusqu’à 4096 [vecteurs](dx-graphics-hlsl-vector.md); chaque vecteur contient jusqu’à 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="1c8ae-142">Vous pouvez lier jusqu’à 14 mémoires tampons constantes par étape de pipeline (2 emplacements supplémentaires sont réservés à un usage interne).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="1c8ae-143">Une mémoire tampon de texture est une ressource tampon spécialisée accessible comme une texture.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="1c8ae-144">L’accès aux textures (par rapport à l’accès aux tampons) peut avoir de meilleures performances pour les données indexées arbitrairement.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="1c8ae-145">Vous pouvez lier jusqu’à 128 tampons de texture par étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="1c8ae-146">Une ressource de mémoire tampon est conçue pour réduire la surcharge liée à la définition de constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="1c8ae-147">L’infrastructure Effect (voir [**interface ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gère la mise à jour des mémoires tampons de constante et de texture, ou vous pouvez utiliser l’API Direct3D pour mettre à jour les mémoires tampons (pour plus d’informations, consultez [copie et accès aux données des ressources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) ).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="1c8ae-148">Une application peut également copier des données à partir d’une autre mémoire tampon (telle qu’une cible de rendu ou une cible de sortie de flux) dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="1c8ae-149">Pour plus d’informations sur l’utilisation de mémoires tampons constantes dans une application D3D10, consultez [types de ressources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) et [création de ressources de mémoire tampon (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="1c8ae-150">Pour Morel d’informations sur l’utilisation de mémoires tampons constantes dans une application D3D11, consultez [Introduction aux mémoires tampons dans Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) et [Comment : créer une mémoire tampon constante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="1c8ae-151">Une mémoire tampon constante ne nécessite pas la liaison d’une [vue](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) au pipeline.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="1c8ae-152">Toutefois, une mémoire tampon de texture requiert une vue et doit être liée à un emplacement de texture (ou doit être liée à [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) lors de l’utilisation d’un effet).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="1c8ae-153">Il existe deux façons de compresser des données de constantes : à l’aide des mots clés [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) et [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8ae-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>

<span data-ttu-id="1c8ae-154">Différences entre Direct3D 9 et Direct3D 10 et 11 :</span><span class="sxs-lookup"><span data-stu-id="1c8ae-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span>

- <span data-ttu-id="1c8ae-155">Contrairement à l’allocation automatique de constantes dans Direct3D 9, qui n’effectuait pas de compression et attribuaient à la place chaque variable à un ensemble de registres float4, les variables de constantes HLSL suivent les règles de compression dans Direct3D 10 et 11.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span>



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="1c8ae-156">Organisation de mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="1c8ae-156">Organizing constant buffers</span></span>

<span data-ttu-id="1c8ae-157">Les mémoires tampons constantes réduisent la bande passante requise pour mettre à jour les constantes de nuanceur en permettant aux constantes de nuanceur d’être regroupées et validées en même temps plutôt que d’effectuer des appels individuels pour valider chaque constante séparément.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="1c8ae-158">Pour optimiser l’utilisation des mémoires tampons constantes, classez les variables de nuanceur dans ces mémoires en fonction de la fréquence de leur mise à jour.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="1c8ae-159">Cela permet à une application de réduire la bande passante requise pour la mise à jour des constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="1c8ae-160">Par exemple, un nuanceur peut déclarer deux mémoires tampons constantes et organiser les données en fonction de leur fréquence de mise à jour : les données qui doivent être mises à jour au niveau de chaque objet (par exemple, une matrice universelle) sont regroupées dans une mémoire tampon constante qui peut être mise à jour pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="1c8ae-161">Cela est indépendant des données qui caractérisent une scène et est donc susceptible d’être mis à jour bien moins souvent (lorsque la scène change).</span><span class="sxs-lookup"><span data-stu-id="1c8ae-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="1c8ae-162">Mémoires tampons constantes par défaut</span><span class="sxs-lookup"><span data-stu-id="1c8ae-162">Default constant buffers</span></span>

<span data-ttu-id="1c8ae-163">Deux mémoires tampons constantes par défaut sont disponibles, $Global et $Param.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="1c8ae-164">Les variables placées dans la portée globale sont ajoutées implicitement au $Global CBuffer, à l’aide de la même méthode de compression que celle utilisée pour cbuffers.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="1c8ae-165">Les paramètres uniformes de la liste de paramètres d’une fonction s’affichent dans le $Param mémoire tampon constante lorsqu’un nuanceur est compilé en dehors de l’infrastructure d’effets.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="1c8ae-166">En cas de compilation dans l’infrastructure Effects, toutes les uniformes doivent être résolues en variables définies dans la portée globale.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="1c8ae-167">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c8ae-167">Examples</span></span>

<span data-ttu-id="1c8ae-168">Voici un exemple de l' [exemple Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) qui est une mémoire tampon de texture constituée d’un tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="1c8ae-169">Cet exemple de déclaration assigne manuellement une mémoire tampon constante pour commencer à un registre particulier et compresse également des éléments particuliers par sous-composants.</span><span class="sxs-lookup"><span data-stu-id="1c8ae-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="1c8ae-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c8ae-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8ae-171">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1c8ae-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

