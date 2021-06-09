---
title: Création d’une signature racine
description: Les signatures racines sont une structure de données complexe contenant des structures imbriquées.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826435"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="0017b-103">Création d’une signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-103">Creating a Root Signature</span></span>

<span data-ttu-id="0017b-104">Les signatures racines sont une structure de données complexe contenant des structures imbriquées.</span><span class="sxs-lookup"><span data-stu-id="0017b-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="0017b-105">Celles-ci peuvent être définies par programme à l’aide de la définition de la structure de données ci-dessous (qui comprend des méthodes pour aider à initialiser les membres).</span><span class="sxs-lookup"><span data-stu-id="0017b-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="0017b-106">Elles peuvent également être créées dans le langage HLSL (High Level Shading Language), ce qui donne l’avantage que le compilateur validera tôt que la disposition soit compatible avec le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0017b-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="0017b-107">L’API pour la création d’une signature racine utilise une version sérialisée (autonome, à pointeur libre) de la description de la disposition décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0017b-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="0017b-108">Une méthode est fournie pour générer cette version sérialisée à partir de la structure de données C++, mais une autre façon d’obtenir une définition de signature racine sérialisée est de la récupérer à partir d’un nuanceur qui a été compilé avec une signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="0017b-109">Si vous souhaitez tirer parti des optimisations de pilotes pour les descripteurs de signature racine et les données, reportez-vous à la [signature racine Version 1,1](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="0017b-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="0017b-110">Types de liaison de table de descripteur</span><span class="sxs-lookup"><span data-stu-id="0017b-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="0017b-111">Plage du descripteur</span><span class="sxs-lookup"><span data-stu-id="0017b-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="0017b-112">Disposition du tableau de descripteurs</span><span class="sxs-lookup"><span data-stu-id="0017b-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="0017b-113">Constantes racine</span><span class="sxs-lookup"><span data-stu-id="0017b-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="0017b-114">Descripteur racine</span><span class="sxs-lookup"><span data-stu-id="0017b-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="0017b-115">Visibilité du nuanceur</span><span class="sxs-lookup"><span data-stu-id="0017b-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="0017b-116">Définition de signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="0017b-117">Sérialisation/désérialisation de la structure de données de la signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="0017b-118">API de création de signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="0017b-119">Signature racine dans les objets d’état de pipeline</span><span class="sxs-lookup"><span data-stu-id="0017b-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="0017b-120">Code pour définir une signature racine de la version 1,1</span><span class="sxs-lookup"><span data-stu-id="0017b-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="0017b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0017b-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="0017b-122">Types de liaison de table de descripteur</span><span class="sxs-lookup"><span data-stu-id="0017b-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="0017b-123">Le [**\_ \_ \_ type de plage**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) du descripteur D3D12 enum définit les types de descripteurs qui peuvent être référencés dans le cadre d’une définition de présentation de tableau de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="0017b-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="0017b-124">C’est une plage dans laquelle, par exemple, si une partie d’une table de descripteur a 100 SRVs, cette plage peut être déclarée dans une entrée au lieu de 100.</span><span class="sxs-lookup"><span data-stu-id="0017b-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="0017b-125">Par conséquent, une définition de table de descripteur est une collection de plages.</span><span class="sxs-lookup"><span data-stu-id="0017b-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="0017b-126">Plage du descripteur</span><span class="sxs-lookup"><span data-stu-id="0017b-126">Descriptor Range</span></span>

<span data-ttu-id="0017b-127">La structure de la [**\_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) définit une plage de descripteurs d’un type donné (par exemple, SRVs) dans une table de descripteur.</span><span class="sxs-lookup"><span data-stu-id="0017b-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="0017b-128">La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro peut généralement être utilisée pour le `OffsetInDescriptorsFromTableStart` paramètre de [**la \_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="0017b-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="0017b-129">Cela signifie que vous ajoutez la plage de descripteurs qui est définie après le précédent dans la table du descripteur.</span><span class="sxs-lookup"><span data-stu-id="0017b-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="0017b-130">Si l’application souhaite des descripteurs d’alias ou, pour une raison quelconque, souhaite ignorer des emplacements, elle peut `OffsetInDescriptorsFromTableStart` être définie sur le décalage souhaité.</span><span class="sxs-lookup"><span data-stu-id="0017b-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="0017b-131">La définition de plages qui se chevauchent de types différents n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0017b-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="0017b-132">L’ensemble de registres de nuanceur spécifié par la combinaison de, `RangeType` `NumDescriptors` , `BaseShaderRegister` et `RegisterSpace` ne peut pas entrer en conflit ou se chevaucher dans toutes les déclarations d’une signature racine qui ont une [**\_ \_ visibilité de nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) commune (consultez la section de visibilité du nuanceur ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="0017b-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="0017b-133">Disposition du tableau de descripteurs</span><span class="sxs-lookup"><span data-stu-id="0017b-133">Descriptor Table Layout</span></span>

<span data-ttu-id="0017b-134">La structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) déclare la disposition d’une table de descripteurs sous la forme d’une collection de plages de descripteur qui apparaissent une après l’autre dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="0017b-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="0017b-135">Les échantillonneurs ne sont pas autorisés dans la même table de descripteurs que CBV/UAV/SRVs.</span><span class="sxs-lookup"><span data-stu-id="0017b-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="0017b-136">Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="0017b-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="0017b-137">Pour définir un tableau de descripteurs Graphics (CBV, SRV, UAV, Sampler), utilisez [**ID3D12GraphicsCommandList :: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="0017b-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="0017b-138">Pour définir une table de descripteurs de calcul, utilisez [**ID3D12GraphicsCommandList :: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="0017b-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="0017b-139">Constantes racine</span><span class="sxs-lookup"><span data-stu-id="0017b-139">Root Constants</span></span>

<span data-ttu-id="0017b-140">La structure de [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) déclare des constantes inline dans la signature racine qui s’affichent dans les nuanceurs comme une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="0017b-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="0017b-141">Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="0017b-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="0017b-142">Descripteur racine</span><span class="sxs-lookup"><span data-stu-id="0017b-142">Root Descriptor</span></span>

<span data-ttu-id="0017b-143">La structure du descripteur [**\_ \_ racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) déclare les descripteurs (qui apparaissent dans les nuanceurs) Inline dans la signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="0017b-144">Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` ou `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="0017b-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="0017b-145">Visibilité du nuanceur</span><span class="sxs-lookup"><span data-stu-id="0017b-145">Shader Visibility</span></span>

<span data-ttu-id="0017b-146">Le membre de l’énumération de [**\_ \_ visibilité du nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) défini dans le paramètre de visibilité du nuanceur du [**\_ \_ paramètre racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) détermine les nuanceurs qui voient le contenu d’un emplacement de signature racine donné.</span><span class="sxs-lookup"><span data-stu-id="0017b-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="0017b-147">Compute utilise toujours \_ All (puisqu’il n’y a qu’une seule étape active).</span><span class="sxs-lookup"><span data-stu-id="0017b-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="0017b-148">Les graphiques peuvent choisir, mais s’ils utilisent \_ tous, toutes les étapes de nuanceur voient tout ce qui est lié à l’emplacement de signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="0017b-149">L’une des utilisations de la visibilité du nuanceur est l’aide pour les nuanceurs qui sont créés en attendant des liaisons différentes par étape de nuanceur à l’aide d’un espace de noms qui se chevauche.</span><span class="sxs-lookup"><span data-stu-id="0017b-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="0017b-150">Par exemple, un nuanceur vertex peut déclarer :</span><span class="sxs-lookup"><span data-stu-id="0017b-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="0017b-151">et le nuanceur de pixels peut également déclarer :</span><span class="sxs-lookup"><span data-stu-id="0017b-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="0017b-152">Si l’application établit une liaison de signature racine avec T0 VISIBILity \_ All, les deux nuanciers voient la même texture.</span><span class="sxs-lookup"><span data-stu-id="0017b-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="0017b-153">Si le nuanceur définit réellement que chaque nuanceur souhaite voir différentes textures, il peut définir 2 emplacements de signature racine avec un vertex de visibilité \_ et un \_ Pixel.</span><span class="sxs-lookup"><span data-stu-id="0017b-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="0017b-154">Quelle que soit la visibilité sur un emplacement de signature racine, il a toujours le même coût (coût uniquement en fonction de l’SlotType) vers une taille de signature maximale fixe.</span><span class="sxs-lookup"><span data-stu-id="0017b-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="0017b-155">Sur un matériel D3D11 de bas niveau, la visibilité du NUANCEur \_ est également prise en compte lors de la validation des tailles de tables de descripteurs dans une disposition racine, car certains matériels d3d11 ne peuvent prendre en charge qu’une quantité maximale de liaisons par étape.</span><span class="sxs-lookup"><span data-stu-id="0017b-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="0017b-156">Ces restrictions sont imposées uniquement lors de l’exécution sur du matériel de bas niveau et ne limitent pas du tout le matériel moderne.</span><span class="sxs-lookup"><span data-stu-id="0017b-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="0017b-157">Si une signature racine a plusieurs tables de descripteur définies qui se chevauchent dans l’espace de noms (les liaisons de Registre au nuanceur) et que l’une d’entre elles indique \_ tout pour la visibilité, la disposition n’est pas valide (la création échoue).</span><span class="sxs-lookup"><span data-stu-id="0017b-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="0017b-158">Définition de signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-158">Root Signature Definition</span></span>

<span data-ttu-id="0017b-159">La structure de la [**\_ signature racine D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) peut contenir des tables de descripteurs et des constantes incluses, chaque type d’emplacement défini par la structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) et le [**\_ \_ \_ type de paramètre racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)Enum.</span><span class="sxs-lookup"><span data-stu-id="0017b-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="0017b-160">Pour initier un emplacement de signature racine, reportez-vous aux méthodes **\* \* \* SetComputeRoot** et **SetGraphicsRoot \* \* \*** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="0017b-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="0017b-161">Les échantillonneurs statiques sont décrits dans la signature racine à l’aide de la structure d' [**\_ \_ échantillonneur statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="0017b-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="0017b-162">Un certain nombre d’indicateurs limitent l’accès de certains nuanceurs à la signature racine, reportez-vous aux [**\_ \_ \_ indicateurs de signature racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="0017b-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="0017b-163">Sérialisation/désérialisation de la structure de données de la signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="0017b-164">Les méthodes décrites dans cette section sont exportées par D3D12Core.dll et fournissent des méthodes pour sérialiser et désérialiser une structure de données de signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="0017b-165">La forme sérialisée est celle qui est transmise dans l’API lors de la création d’une signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="0017b-166">Si un nuanceur a été créé avec une signature racine dans celui-ci (lorsque cette fonctionnalité est ajoutée), le nuanceur compilé contient déjà une signature racine sérialisée dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0017b-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="0017b-167">Si une application génère de façon procédurale une structure de données [**\_ \_ \_ desc signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , elle doit établir la forme sérialisée à l’aide de [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="0017b-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="0017b-168">Sortie de qui peut être passée dans [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="0017b-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="0017b-169">Si une application a déjà une signature racine sérialisée, ou a un nuanceur compilé qui contient une signature racine et souhaite découvrir par programmation la définition de la disposition (appelée « réflexion »), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) peut être appelé.</span><span class="sxs-lookup"><span data-stu-id="0017b-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="0017b-170">Cela génère une interface [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , qui contient une méthode pour retourner la structure de données [**\_ \_ \_ desc de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) désérialisée.</span><span class="sxs-lookup"><span data-stu-id="0017b-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="0017b-171">L’interface possède la durée de vie de la structure de données désérialisée.</span><span class="sxs-lookup"><span data-stu-id="0017b-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="0017b-172">API de création de signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-172">Root Signature Creation API</span></span>

<span data-ttu-id="0017b-173">L’API [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) prend une version sérialisée d’une signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="0017b-174">Signature racine dans les objets d’état de pipeline</span><span class="sxs-lookup"><span data-stu-id="0017b-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="0017b-175">Les méthodes permettant de créer l’état du pipeline ([**ID3D12Device :: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) et [**ID3D12Device :: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) prennent une interface [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facultative comme paramètre d’entrée (stocké dans une structure [**\_ desc d' \_ \_ état \_ de pipeline Graphics D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ).</span><span class="sxs-lookup"><span data-stu-id="0017b-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="0017b-176">Cette opération remplace toute signature racine déjà présente dans les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="0017b-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="0017b-177">Si une signature racine est passée dans l’une des méthodes Create Pipeline State, cette signature racine est validée par rapport à tous les nuanceurs de l’PSO pour la compatibilité et donnée au pilote à utiliser avec tous les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="0017b-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="0017b-178">Si l’un des nuanceurs a une signature racine différente, il est remplacé par la signature racine passée dans l’API.</span><span class="sxs-lookup"><span data-stu-id="0017b-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="0017b-179">Si aucune signature racine n’est transmise, tous les nuanceurs transmis doivent avoir une signature racine et doivent correspondre, ce qui sera attribué au pilote.</span><span class="sxs-lookup"><span data-stu-id="0017b-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="0017b-180">La définition d’un PSO sur une liste de commandes ou une offre groupée ne modifie pas la signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="0017b-181">Cela est accompli par les méthodes [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) et [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="0017b-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="0017b-182">À l’heure où Draw (Graphics)/Dispatch (Compute) est appelé, l’application doit s’assurer que le PSO actuel correspond à la signature racine actuelle ; dans le cas contraire, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0017b-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="0017b-183">Code pour définir une signature racine de la version 1,1</span><span class="sxs-lookup"><span data-stu-id="0017b-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="0017b-184">L’exemple ci-dessous montre comment créer une signature racine au format suivant :</span><span class="sxs-lookup"><span data-stu-id="0017b-184">The example below shows how to create a root signature with the following format:</span></span>



| <span data-ttu-id="0017b-185">RootParameterIndex</span><span class="sxs-lookup"><span data-stu-id="0017b-185">RootParameterIndex</span></span>                       | <span data-ttu-id="0017b-186">Contenu</span><span class="sxs-lookup"><span data-stu-id="0017b-186">Contents</span></span>                                               | <span data-ttu-id="0017b-187">Valeurs</span><span class="sxs-lookup"><span data-stu-id="0017b-187">Values</span></span>                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| <span data-ttu-id="0017b-188">\[0\]</span><span class="sxs-lookup"><span data-stu-id="0017b-188">\[0\]</span></span>                  | <span data-ttu-id="0017b-189">Constantes racine : {B2}</span><span class="sxs-lookup"><span data-stu-id="0017b-189">Root constants: { b2 }</span></span>                         | <span data-ttu-id="0017b-190">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="0017b-190">(1 CBV)</span></span>                                      |
| <span data-ttu-id="0017b-191">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0017b-191">\[1\]</span></span>                  | <span data-ttu-id="0017b-192">Table du descripteur : {T2-T7, U0-U3}</span><span class="sxs-lookup"><span data-stu-id="0017b-192">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="0017b-193">(6 SRVs + 4 UAVs)</span><span class="sxs-lookup"><span data-stu-id="0017b-193">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="0017b-194">\[2\]</span><span class="sxs-lookup"><span data-stu-id="0017b-194">\[2\]</span></span>                  | <span data-ttu-id="0017b-195">CBV racine : {B0}</span><span class="sxs-lookup"><span data-stu-id="0017b-195">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="0017b-196">(1 CBV, données statiques)</span><span class="sxs-lookup"><span data-stu-id="0017b-196">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="0017b-197">\[3\]</span><span class="sxs-lookup"><span data-stu-id="0017b-197">\[3\]</span></span>                  | <span data-ttu-id="0017b-198">Tableau du descripteur : {S0-S1}</span><span class="sxs-lookup"><span data-stu-id="0017b-198">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="0017b-199">(2 échantillonneurs)</span><span class="sxs-lookup"><span data-stu-id="0017b-199">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="0017b-200">\[4\]</span><span class="sxs-lookup"><span data-stu-id="0017b-200">\[4\]</span></span>                  | <span data-ttu-id="0017b-201">Table du descripteur : {T8-Unlimited}</span><span class="sxs-lookup"><span data-stu-id="0017b-201">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="0017b-202">(non lié à \# SRVs, descripteurs volatils)</span><span class="sxs-lookup"><span data-stu-id="0017b-202">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="0017b-203">\[5\]</span><span class="sxs-lookup"><span data-stu-id="0017b-203">\[5\]</span></span>                  | <span data-ttu-id="0017b-204">Table du descripteur : {(T0, space1)-Unlimited}</span><span class="sxs-lookup"><span data-stu-id="0017b-204">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="0017b-205">(non lié à \# SRVs, descripteurs volatils)</span><span class="sxs-lookup"><span data-stu-id="0017b-205">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="0017b-206">\[6\]</span><span class="sxs-lookup"><span data-stu-id="0017b-206">\[6\]</span></span>                  | <span data-ttu-id="0017b-207">Tableau du descripteur : {B1}</span><span class="sxs-lookup"><span data-stu-id="0017b-207">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="0017b-208">(1 CBV, données statiques)</span><span class="sxs-lookup"><span data-stu-id="0017b-208">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="0017b-209">Si la plupart des parties de la signature racine sont utilisées la plupart du temps, il peut être préférable d’avoir un changement trop fréquent de la signature racine.</span><span class="sxs-lookup"><span data-stu-id="0017b-209">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="0017b-210">Les applications doivent trier les entrées de la signature racine le plus souvent au moins.</span><span class="sxs-lookup"><span data-stu-id="0017b-210">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="0017b-211">Quand une application modifie les liaisons à n’importe quelle partie de la signature racine, il peut être nécessaire d’effectuer une copie de tout ou partie de l’état de la signature racine, ce qui peut devenir un coût non négligeable lorsqu’elle est multipliée par de nombreuses modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="0017b-211">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="0017b-212">En outre, la signature racine définit un échantillonneur statique qui effectue un filtrage de texture anisotrope au registre du nuanceur S3.</span><span class="sxs-lookup"><span data-stu-id="0017b-212">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="0017b-213">Une fois cette signature racine liée, les tables de descripteurs, les CBV racines et les constantes peuvent être affectés à l' \[ espace de paramètre 0.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="0017b-213">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="0017b-214">par exemple, les tables de descripteurs (plages dans un tas de descripteur) peuvent être liées à chacun des paramètres racine \[ 1 \] et \[ 3.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="0017b-214">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="0017b-215">Le code suivant illustre la façon dont la signature racine ci-dessus peut être utilisée dans une liste de commandes Graphics.</span><span class="sxs-lookup"><span data-stu-id="0017b-215">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="0017b-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0017b-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0017b-217">Signatures racine</span><span class="sxs-lookup"><span data-stu-id="0017b-217">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="0017b-218">Spécification de signatures racine en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="0017b-218">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="0017b-219">Utilisation d’une signature racine</span><span class="sxs-lookup"><span data-stu-id="0017b-219">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
