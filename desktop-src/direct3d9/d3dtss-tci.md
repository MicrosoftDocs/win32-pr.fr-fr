---
description: Indicateurs de capacité de la texture du pilote.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950811"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="87199-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="87199-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="87199-104">Indicateurs de capacité de la texture du pilote.</span><span class="sxs-lookup"><span data-stu-id="87199-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87199-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="87199-105">\#define</span></span>                                 | <span data-ttu-id="87199-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="87199-106">Value</span></span>       | <span data-ttu-id="87199-107">Description</span><span class="sxs-lookup"><span data-stu-id="87199-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="87199-108">D3DTSS \_ TCI \_</span><span class="sxs-lookup"><span data-stu-id="87199-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="87199-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="87199-109">0x00000000L</span></span> | <span data-ttu-id="87199-110">Utilise les coordonnées de texture spécifiées contenues dans le format de vertex.</span><span class="sxs-lookup"><span data-stu-id="87199-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="87199-111">Cette valeur est résolue à zéro.</span><span class="sxs-lookup"><span data-stu-id="87199-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="87199-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="87199-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="87199-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="87199-113">0x00010000L</span></span> | <span data-ttu-id="87199-114">Utilisez la normale du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée pour la transformation de texture de cette étape.</span><span class="sxs-lookup"><span data-stu-id="87199-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="87199-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="87199-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="87199-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="87199-116">0x00020000L</span></span> | <span data-ttu-id="87199-117">Utilisez la position du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée pour la transformation de texture de cette étape.</span><span class="sxs-lookup"><span data-stu-id="87199-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="87199-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="87199-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="87199-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="87199-119">0x00030000L</span></span> | <span data-ttu-id="87199-120">Utilisez le vecteur de réflexion, transformé en espace de caméra, comme coordonnée de texture d’entrée pour la transformation de texture de cette étape.</span><span class="sxs-lookup"><span data-stu-id="87199-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="87199-121">Le vecteur de réflexion est calculé à partir de la position du vertex d’entrée et du vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="87199-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="87199-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="87199-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="87199-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="87199-123">0x00040000L</span></span> | <span data-ttu-id="87199-124">Utilisez les coordonnées de texture spécifiées pour le mappage de sphère.</span><span class="sxs-lookup"><span data-stu-id="87199-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="87199-125">Ces constantes sont utilisées par D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="87199-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="87199-126">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="87199-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="87199-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="87199-127">Header</span></span>                   | <span data-ttu-id="87199-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="87199-128">d3d9caps.h</span></span> |
| <span data-ttu-id="87199-129">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="87199-129">Minimum operating system</span></span> | <span data-ttu-id="87199-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="87199-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="87199-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87199-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87199-132">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="87199-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



