---
title: Étape de Stream-Output
description: L’objectif de l’étape de flux de sortie est de générer continuellement des données de vertex (ou de diffuser) à partir de l’étape Geometry-Shader (ou de l’étape de nuanceur de vertex si l’étape Geometry-Shader est inactive) vers une ou plusieurs mémoires tampons en mémoire (voir Prise en main avec l’étape Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- étape de sortie de flux (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463951"
---
# <a name="stream-output-stage"></a><span data-ttu-id="b6e95-104">Étape de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="b6e95-104">Stream-Output Stage</span></span>

<span data-ttu-id="b6e95-105">L’objectif de l’étape de flux de sortie est de générer continuellement des données de vertex (ou de diffuser) à partir de l’étape Geometry-Shader (ou de l’étape de nuanceur de vertex si l’étape Geometry-Shader est inactive) vers une ou plusieurs mémoires tampons en mémoire (voir [prise en main avec l’étape Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="b6e95-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="b6e95-106">L’étape flux-sortie (SO) se trouve dans le pipeline juste après l’étape Geometry-Shader et juste avant l’étape de pixellisation, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="b6e95-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![diagramme de l’emplacement de l’étape de sortie de flux dans le pipeline](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="b6e95-108">Les données transmises en mémoire vers la mémoire peuvent être lues dans le pipeline dans une passe de rendu ultérieure, ou peuvent être copiées dans une ressource intermédiaire (afin qu’elles puissent être lues par l’UC).</span><span class="sxs-lookup"><span data-stu-id="b6e95-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="b6e95-109">La quantité de données transmises en continu peut varier. l’API [**ID3D11DeviceContext ::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) est conçue pour gérer les données sans qu’il soit nécessaire d’interroger (le GPU) sur la quantité de données écrites.</span><span class="sxs-lookup"><span data-stu-id="b6e95-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="b6e95-110">Lorsqu’un triangle ou une frange est lié à l’étape assembleur d’entrée, chaque bande est convertie en liste avant d’être diffusée en continu. Les vertex sont toujours écrits comme des primitives complètes (par exemple, 3 sommets à la fois pour les triangles); les primitives incomplètes ne sont jamais transmises en continu. Les types primitifs avec contiguïté ignorent les données d’adjacence avant la diffusion des données en continu.</span><span class="sxs-lookup"><span data-stu-id="b6e95-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="b6e95-111">Il existe deux façons d’alimenter les données de sortie de flux dans le pipeline :</span><span class="sxs-lookup"><span data-stu-id="b6e95-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="b6e95-112">Les données de sortie de flux peuvent être réintégrées à l’étape assembleur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b6e95-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="b6e95-113">Les données de sortie de flux peuvent être lues par des nuanceurs programmables à l’aide de fonctions de chargement (telles que [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span><span class="sxs-lookup"><span data-stu-id="b6e95-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="b6e95-114">Pour utiliser une mémoire tampon en tant que ressource de flux de sortie, créez la mémoire tampon avec l’indicateur de [**\_ sortie de \_ flux \_ de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="b6e95-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="b6e95-115">L’étape flux-sortie prend en charge jusqu’à 4 mémoires tampons simultanément.</span><span class="sxs-lookup"><span data-stu-id="b6e95-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="b6e95-116">Si vous diffusez des données dans plusieurs mémoires tampons, chaque mémoire tampon peut uniquement capturer un seul élément (jusqu’à 4 composants) de données par vertex, avec une Stride de données implicite égale à la largeur d’élément dans chaque mémoire tampon (compatible avec la manière dont les mémoires tampons d’élément unique peuvent être liées à l’entrée dans des étapes de nuanceur).</span><span class="sxs-lookup"><span data-stu-id="b6e95-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="b6e95-117">En outre, si les mémoires tampons ont des tailles différentes, l’écriture s’arrête dès que l’une des mémoires tampons est pleine.</span><span class="sxs-lookup"><span data-stu-id="b6e95-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="b6e95-118">Si vous diffusez des données dans une seule mémoire tampon, la mémoire tampon peut capturer jusqu’à 64 composants scalaires de données par vertex (256 octets ou moins) ou le nombre de vertex peut atteindre jusqu’à 2048 octets.</span><span class="sxs-lookup"><span data-stu-id="b6e95-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="b6e95-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b6e95-119">In this section</span></span>



| <span data-ttu-id="b6e95-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b6e95-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="b6e95-121">Description</span><span class="sxs-lookup"><span data-stu-id="b6e95-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6e95-122">Prise en main avec l’étape de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="b6e95-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="b6e95-123">Cette section décrit comment utiliser un nuanceur Geometry avec l’étape de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="b6e95-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b6e95-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6e95-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e95-125">Pipeline graphique</span><span class="sxs-lookup"><span data-stu-id="b6e95-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="b6e95-126">Étapes de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b6e95-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

