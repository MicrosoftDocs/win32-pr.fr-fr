---
description: Dans Direct3D 10, l’état de l’appareil est regroupé en objets d’État, ce qui réduit de manière considérable le coût des changements d’État.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objets d’État (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512883"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="8c2d7-103">Objets d’État (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8c2d7-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="8c2d7-104">Dans Direct3D 10, l’état de l’appareil est regroupé en objets d’État, ce qui réduit de manière considérable le coût des changements d’État.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="8c2d7-105">Il existe plusieurs objets d’État et chacun d’eux est conçu pour initialiser un ensemble d’États pour une étape de pipeline particulière.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="8c2d7-106">Vous pouvez créer jusqu’à 4096 pour chaque type d’objet d’État.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="8c2d7-107">État de la disposition d’entrée</span><span class="sxs-lookup"><span data-stu-id="8c2d7-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="8c2d7-108">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="8c2d7-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="8c2d7-109">État du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="8c2d7-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="8c2d7-110">État de fusion</span><span class="sxs-lookup"><span data-stu-id="8c2d7-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="8c2d7-111">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="8c2d7-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="8c2d7-112">Considérations relatives aux performances</span><span class="sxs-lookup"><span data-stu-id="8c2d7-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="8c2d7-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c2d7-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="8c2d7-114">État de l' Input-Layout</span><span class="sxs-lookup"><span data-stu-id="8c2d7-114">Input-Layout State</span></span>

<span data-ttu-id="8c2d7-115">Ce groupe d’État (voir la description de l' [**\_ \_ \_ élément d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dicte comment l' [étape assembleur d’entrée](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) lit les données en dehors des mémoires tampons d’entrée et les assemble pour une utilisation par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="8c2d7-116">Cela comprend l’État, tel que le nombre d’éléments dans la mémoire tampon d’entrée et la signature des données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="8c2d7-117">L’étape assembleur d’entrée est une nouvelle étape dans le pipeline dont la tâche consiste à diffuser en continu des primitives de la mémoire dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="8c2d7-118">Pour créer un objet d’état de disposition d’entrée, consultez [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="8c2d7-119">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="8c2d7-119">Rasterizer State</span></span>

<span data-ttu-id="8c2d7-120">Ce groupe d’États (voir [**D3D10 \_ rastériseur \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) Initialise l’étape de [rastérisation](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="8c2d7-121">Cet objet comprend un état tel que les modes de remplissage ou d’élimination, l’activation d’un rectangle de ciseaux pour le découpage et la définition des paramètres d’échantillonnages.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="8c2d7-122">Cette étape pixellise les primitives en pixels, en effectuant des opérations telles que le découpage et le mappage des primitives à la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="8c2d7-123">Pour créer un objet d’État rastériseur, consultez [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="8c2d7-124">État de l' Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="8c2d7-124">Depth-Stencil State</span></span>

<span data-ttu-id="8c2d7-125">Ce groupe d’États (voir [**D3D10 de \_ profondeur du \_ stencil \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) Initialise la partie profondeur du gabarit de l' [étape de fusion de sortie](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="8c2d7-126">Plus spécifiquement, cet objet Initialise le test de profondeur et de stencil.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="8c2d7-127">Pour créer un objet d’état de stencil-profondeur, consultez [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="8c2d7-128">État de fusion</span><span class="sxs-lookup"><span data-stu-id="8c2d7-128">Blend State</span></span>

<span data-ttu-id="8c2d7-129">Ce groupe d’États (voir [**D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) Initialise la partie de fusion de l' [étape de fusion de sortie](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="8c2d7-130">Pour créer un objet d’état de fusion, consultez [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="8c2d7-131">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="8c2d7-131">Sampler State</span></span>

<span data-ttu-id="8c2d7-132">Ce groupe d’État (voir [**l' \_ exemple D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Initialise un objet échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="8c2d7-133">Un objet échantillonneur est utilisé par les étapes du nuanceur pour filtrer les textures en mémoire.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2d7-134">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="8c2d7-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="8c2d7-135">Dans Direct3D 10, l’objet échantillonneur n’est plus lié à une texture spécifique. il décrit simplement comment effectuer un filtrage en fonction d’une ressource attachée.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="8c2d7-136">Pour créer un objet d’état d’échantillonnage, consultez [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="8c2d7-137">Considérations relatives aux performances</span><span class="sxs-lookup"><span data-stu-id="8c2d7-137">Performance Considerations</span></span>

<span data-ttu-id="8c2d7-138">La conception de l’API pour utiliser les objets d’État crée plusieurs avantages en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="8c2d7-139">Cela inclut la validation de l’État au moment de la création de l’objet, l’activation de la mise en cache des objets d’État dans le matériel et la réduction considérable de la quantité d’État qui est passée pendant un appel d’API de paramétrage d’État (en passant un handle à l’objet d’État au lieu de l’État).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="8c2d7-140">Pour améliorer ces performances, vous devez créer vos objets d’État au démarrage de votre application, bien avant votre boucle de rendu.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="8c2d7-141">Les objets d’État sont immuables, autrement dit, une fois qu’ils sont créés, vous ne pouvez pas les modifier.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="8c2d7-142">Au lieu de cela, vous devez les détruire et les recréer.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="8c2d7-143">Pour faire face à cette restriction, vous pouvez créer jusqu’à 4096 pour chaque type d’objets d’État.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="8c2d7-144">Par exemple, vous pouvez créer plusieurs objets échantillonner avec différentes combinaisons d’États d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="8c2d7-145">La modification de l’état de l’échantillonneur est ensuite effectuée en appelant l’API Set appropriée qui passe un handle à l’objet (par opposition à l’état de l’échantillonneur).</span><span class="sxs-lookup"><span data-stu-id="8c2d7-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="8c2d7-146">Cela réduit considérablement la quantité de surcharge au cours de chaque trame de rendu pour la modification de l’État, car le nombre d’appels et la quantité de données sont considérablement réduits.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="8c2d7-147">Vous pouvez également choisir d’utiliser le système d’effet qui gère automatiquement la création et la destruction efficaces des objets d’État pour votre application.</span><span class="sxs-lookup"><span data-stu-id="8c2d7-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c2d7-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c2d7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c2d7-149">Fonctionnalités de l’API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8c2d7-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
