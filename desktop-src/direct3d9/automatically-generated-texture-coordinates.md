---
title: Coordonnées de texture générées automatiquement (Direct3D 9)
description: Le système peut utiliser la position transformée de l’espace de caméra ou la normale d’un vertex comme coordonnées de texture, ou il peut calculer les trois vecteurs d’éléments utilisés pour adresser une carte d’environnement cubique.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514756"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="0cbda-103">Coordonnées de texture générées automatiquement (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cbda-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="0cbda-104">Le système peut utiliser la position transformée de l’espace de caméra ou la normale d’un vertex comme coordonnées de texture, ou il peut calculer les trois vecteurs d’éléments utilisés pour adresser une carte d’environnement cubique.</span><span class="sxs-lookup"><span data-stu-id="0cbda-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="0cbda-105">À l’instar des coordonnées de texture que vous spécifiez explicitement dans un vertex, vous pouvez utiliser des coordonnées de texture générées automatiquement comme entrée pour les transformations de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="0cbda-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="0cbda-106">Les coordonnées de texture générées automatiquement peuvent réduire considérablement la bande passante requise pour les données géométriques en éliminant le besoin de coordonnées de texture explicites au format de vertex.</span><span class="sxs-lookup"><span data-stu-id="0cbda-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="0cbda-107">Dans de nombreux cas, les coordonnées de texture générées par le système peuvent être utilisées avec les transformations pour produire des effets spéciaux.</span><span class="sxs-lookup"><span data-stu-id="0cbda-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="0cbda-108">Bien entendu, il s’agit d’une fonctionnalité spéciale, qui vous permet d’utiliser des coordonnées de texture explicites pour de nombreuses occasions.</span><span class="sxs-lookup"><span data-stu-id="0cbda-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="0cbda-109">Configuration des coordonnées de texture générées automatiquement</span><span class="sxs-lookup"><span data-stu-id="0cbda-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="0cbda-110">En C++, l' \_ État D3DTSS TEXCOORDINDEX texture-stage (à partir du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) contrôle la façon dont le système génère des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="0cbda-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="0cbda-111">Normalement, cet État indique au système d’utiliser un ensemble particulier de coordonnées de texture encodées au format de vertex.</span><span class="sxs-lookup"><span data-stu-id="0cbda-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="0cbda-112">Lorsque vous incluez les \_ indicateurs D3DTSS TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION ou D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR dans la valeur que vous affectez à cet État, le comportement système est assez différent.</span><span class="sxs-lookup"><span data-stu-id="0cbda-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="0cbda-113">Si l’un de ces indicateurs est présent, l’étape de texture ignore les coordonnées de texture dans le format de vertex en faveur des coordonnées générées par le système.</span><span class="sxs-lookup"><span data-stu-id="0cbda-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="0cbda-114">La signification de chaque indicateur est indiquée dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="0cbda-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="0cbda-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="0cbda-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="0cbda-116">Utilisez la normale du vertex, transformée en espace de caméra, en tant que coordonnées de texture d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0cbda-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="0cbda-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="0cbda-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="0cbda-118">Utilisez la position du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0cbda-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="0cbda-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="0cbda-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="0cbda-120">Utilisez le vecteur de réflexion, transformé en espace de caméra, en coordonnées de texture d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0cbda-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="0cbda-121">Le vecteur de réflexion est calculé à partir de la position du vertex d’entrée et du vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="0cbda-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="0cbda-122">Les indicateurs d’index de la coordonnée de texture s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="0cbda-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="0cbda-123">Cet exemple utilise :</span><span class="sxs-lookup"><span data-stu-id="0cbda-123">This example uses:</span></span>

-   <span data-ttu-id="0cbda-124">Position du vertex (dans l’espace de caméra) comme coordonnées de texture d’entrée pour cette étape de texture</span><span class="sxs-lookup"><span data-stu-id="0cbda-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="0cbda-125">Mode de renvoi à la ligne défini dans l' \_ État de rendu D3DRENDERSTATE WRAP1</span><span class="sxs-lookup"><span data-stu-id="0cbda-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="0cbda-126">Les coordonnées de texture générées automatiquement sont particulièrement utiles comme valeurs d’entrée pour une transformation de coordonnée de texture, ou pour éliminer la nécessité pour votre application de calculer des vecteurs à trois éléments pour les mappages d’environnements cubiques.</span><span class="sxs-lookup"><span data-stu-id="0cbda-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="0cbda-127">Sphere-Mapping utilise une carte de texture précalculée (au moment du modèle) qui contient l’environnement entier tel qu’il est reflété par une sphère chrome.</span><span class="sxs-lookup"><span data-stu-id="0cbda-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="0cbda-128">Direct3D a une fonctionnalité de génération de coordonnée de texture utilisant l’état de rendu D3DTSS \_ TCI \_ CAMERASPACENORMAL, qui prend la normale du vertex dans l’espace de l’appareil photo et le place par le biais d’une transformation de texture pour générer des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="0cbda-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cbda-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cbda-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cbda-130">Traitement des coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="0cbda-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="0cbda-131">Transformations de coordonnées de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cbda-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="0cbda-132">Mappage d’environnement cubique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cbda-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
