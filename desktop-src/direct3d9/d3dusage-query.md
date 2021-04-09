---
description: Ces options identifient les types de ressources de requête.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110762"
---
# <a name="d3dusage_query"></a><span data-ttu-id="cac27-103">\_Requête D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="cac27-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="cac27-104">Ces options identifient les types de ressources de requête.</span><span class="sxs-lookup"><span data-stu-id="cac27-104">These options identify query resource types.</span></span>



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac27-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="cac27-105">\#define</span></span>                                   | <span data-ttu-id="cac27-106">Description</span><span class="sxs-lookup"><span data-stu-id="cac27-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cac27-107">\_Filtre de requête D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="cac27-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="cac27-108">Interrogez le format de ressource pour voir s’il prend en charge les types de filtre de texture autres que le point de D3DTEXF \_ (qui est toujours pris en charge).</span><span class="sxs-lookup"><span data-stu-id="cac27-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="cac27-109">D3DUSAGE \_ requête \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="cac27-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="cac27-110">Interrogez la ressource sur une carte d’un relief hérité.</span><span class="sxs-lookup"><span data-stu-id="cac27-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cac27-111">\_ \_ Fusion POSTPIXELSHADER de requête D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="cac27-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="cac27-112">Interrogez la ressource pour vérifier la prise en charge de la prise en charge de la fusion de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cac27-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="cac27-113">Si [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) échoue avec la \_ fusion de POSTPIXELSHADER de requêtes D3DUSAGE \_ \_ , les opérations de fusion de pixels ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cac27-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="cac27-114">Il s’agit notamment du test alpha, du brouillard de pixel, de la fusion de cibles de rendu, de l’activation de l’écriture des couleurs et du tramage.</span><span class="sxs-lookup"><span data-stu-id="cac27-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="cac27-115">D3DUSAGE \_ requête \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="cac27-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="cac27-116">Interrogez la ressource pour vérifier si une texture prend en charge la correction gamma au cours d’une opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="cac27-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cac27-117">D3DUSAGE \_ requête \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="cac27-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="cac27-118">Interrogez la ressource pour vérifier si une texture prend en charge la correction gamma au cours d’une opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="cac27-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cac27-119">D3DUSAGE \_ requête \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="cac27-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="cac27-120">Interrogez la ressource pour vérifier la prise en charge de l’échantillonnage de texture vertex shader.</span><span class="sxs-lookup"><span data-stu-id="cac27-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cac27-121">D3DUSAGE \_ requête \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="cac27-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="cac27-122">Interrogez la ressource pour vérifier la prise en charge de l’encapsulation de texture et du mappage MIP.</span><span class="sxs-lookup"><span data-stu-id="cac27-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="cac27-123">Utilisez [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) pour interroger la prise en charge matérielle de ces utilisations et d’autres utilisations listées dans [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="cac27-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="cac27-124">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="cac27-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="cac27-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="cac27-125">Header</span></span>                   | <span data-ttu-id="cac27-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="cac27-126">d3d9types.h</span></span> |
| <span data-ttu-id="cac27-127">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="cac27-127">Minimum operating system</span></span> | <span data-ttu-id="cac27-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cac27-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="cac27-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cac27-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac27-130">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="cac27-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
