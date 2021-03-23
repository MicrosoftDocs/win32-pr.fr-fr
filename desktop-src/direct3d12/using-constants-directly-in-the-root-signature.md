---
title: Utilisation des constantes directement dans la signature racine
description: Les applications peuvent définir des constantes racine dans la signature racine, chacune sous la forme d’un ensemble de valeurs 32 bits. Elles s’affichent en langage HLSL (High Level Shading Language) en tant que mémoire tampon constante. Notez que les mémoires tampons constantes pour des raisons historiques sont affichées sous forme d’ensembles de valeurs 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103390"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="95b16-105">Utilisation des constantes directement dans la signature racine</span><span class="sxs-lookup"><span data-stu-id="95b16-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="95b16-106">Les applications peuvent définir des constantes racine dans la signature racine, chacune sous la forme d’un ensemble de valeurs 32 bits.</span><span class="sxs-lookup"><span data-stu-id="95b16-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="95b16-107">Elles s’affichent en langage HLSL (High Level Shading Language) en tant que mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="95b16-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="95b16-108">Notez que les mémoires tampons constantes pour des raisons historiques sont affichées sous forme d’ensembles de valeurs 4x32 bits.</span><span class="sxs-lookup"><span data-stu-id="95b16-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="95b16-109">Chaque ensemble de constantes utilisateur est traité comme un tableau scalaire de valeurs 32 bits, indexable dynamiquement et en lecture seule à partir du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="95b16-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="95b16-110">En dehors des limites, l’indexation d’un ensemble donné de constantes racine génère des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="95b16-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="95b16-111">En langage HLSL, les définitions de structure de données peuvent être fournies pour que les constantes utilisateur leur fournissent des types.</span><span class="sxs-lookup"><span data-stu-id="95b16-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="95b16-112">Par exemple, si la signature racine définit un ensemble de 4 constantes racine, le langage HLSL peut superposer la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="95b16-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="95b16-113">Les tableaux ne sont pas autorisés dans les mémoires tampons constantes qui sont mappées sur les constantes racine puisque l’indexation dynamique dans l’espace de signature racine n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95b16-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="95b16-114">Par exemple, il n’est pas valide d’avoir une entrée dans la mémoire tampon constante telle que `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="95b16-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="95b16-115">Une mémoire tampon constante mappée aux constantes racine ne peut pas être un tableau ; par conséquent, il n’est pas valide de mapper à des `cbuffer myCBArray[2]` constantes racine.</span><span class="sxs-lookup"><span data-stu-id="95b16-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="95b16-116">Les constantes peuvent être partiellement définies.</span><span class="sxs-lookup"><span data-stu-id="95b16-116">Constants can be partially set.</span></span> <span data-ttu-id="95b16-117">Par exemple, si la signature racine définit des valeurs 4 32 bits à *RootTableBindSlot* 2, tout sous-ensemble des quatre constantes peut être défini à la fois (les autres restent inchangées).</span><span class="sxs-lookup"><span data-stu-id="95b16-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="95b16-118">Cela peut être utile dans les regroupements qui héritent de l’état de signature racine et peuvent être modifiés partiellement.</span><span class="sxs-lookup"><span data-stu-id="95b16-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="95b16-119">Lors de la définition de constantes, faites attention à la disposition de mémoire tampon constante attendue par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="95b16-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="95b16-120">Il est possible que les constantes soient remplies dans `vec4` les limites, par exemple.</span><span class="sxs-lookup"><span data-stu-id="95b16-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="95b16-121">Pour vérifier la disposition attendue, vérifiez les informations de réflexion du nuanceur HLSL.</span><span class="sxs-lookup"><span data-stu-id="95b16-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="95b16-122">Les API suivantes (à partir de l’interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) concernent la définition de constantes directement sur la signature racine :</span><span class="sxs-lookup"><span data-stu-id="95b16-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="95b16-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="95b16-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="95b16-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="95b16-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="95b16-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="95b16-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="95b16-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="95b16-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="95b16-127">Reportez-vous également à la structure des [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="95b16-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95b16-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95b16-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b16-129">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="95b16-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




