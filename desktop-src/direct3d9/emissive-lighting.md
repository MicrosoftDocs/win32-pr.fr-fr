---
description: L’éclairage émissif est décrit par un terme unique.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Éclairage émissif (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512849"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="65a5c-103">Éclairage émissif (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="65a5c-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="65a5c-104">L’éclairage émissif est décrit par un terme unique.</span><span class="sxs-lookup"><span data-stu-id="65a5c-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="65a5c-105">Éclairage émissif = C ₑ</span><span class="sxs-lookup"><span data-stu-id="65a5c-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="65a5c-106">Où :</span><span class="sxs-lookup"><span data-stu-id="65a5c-106">Where:</span></span>



| <span data-ttu-id="65a5c-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65a5c-107">Parameter</span></span> | <span data-ttu-id="65a5c-108">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="65a5c-108">Default value</span></span> | <span data-ttu-id="65a5c-109">Type</span><span class="sxs-lookup"><span data-stu-id="65a5c-109">Type</span></span>          | <span data-ttu-id="65a5c-110">Description</span><span class="sxs-lookup"><span data-stu-id="65a5c-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="65a5c-111">C ₑ</span><span class="sxs-lookup"><span data-stu-id="65a5c-111">Cₑ</span></span>        | <span data-ttu-id="65a5c-112">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="65a5c-112">(0,0,0,0)</span></span>     | <span data-ttu-id="65a5c-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="65a5c-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="65a5c-114">Couleur émissif.</span><span class="sxs-lookup"><span data-stu-id="65a5c-114">Emissive color.</span></span> |



 

<span data-ttu-id="65a5c-115">La valeur de C ₑ est :</span><span class="sxs-lookup"><span data-stu-id="65a5c-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="65a5c-116">Sommet color1, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="65a5c-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="65a5c-117">le sommet color2, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="65a5c-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="65a5c-118">couleur de matériau émissif</span><span class="sxs-lookup"><span data-stu-id="65a5c-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="65a5c-119">Si l’une des options EMISSIVEMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur de la matière émissif est utilisée.</span><span class="sxs-lookup"><span data-stu-id="65a5c-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="65a5c-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="65a5c-120">Example</span></span>

<span data-ttu-id="65a5c-121">Dans cet exemple, l’objet est coloré à l’aide de la lumière ambiante de scène et d’une couleur ambiante de matériau.</span><span class="sxs-lookup"><span data-stu-id="65a5c-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="65a5c-122">Le code est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="65a5c-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="65a5c-123">D’après l’équation, la couleur résultante pour les vertex de l’objet est la couleur du matériau.</span><span class="sxs-lookup"><span data-stu-id="65a5c-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="65a5c-124">L’illustration suivante montre la couleur de matériau, qui est verte.</span><span class="sxs-lookup"><span data-stu-id="65a5c-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="65a5c-125">Lumière luminescente tous les vertex d’objets avec la même couleur.</span><span class="sxs-lookup"><span data-stu-id="65a5c-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="65a5c-126">Elle n’est pas dépendante de la normale du vertex ou de la direction de la lumière.</span><span class="sxs-lookup"><span data-stu-id="65a5c-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="65a5c-127">Par conséquent, la sphère ressemble à un cercle 2D, car il n’y a aucune différence dans l’ombrage autour de la surface de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65a5c-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![illustration d’une sphère verte](images/lighte.jpg)

<span data-ttu-id="65a5c-129">L’illustration suivante montre comment la lumière émissif fusionne avec les trois autres types d’éclairage, des exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="65a5c-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="65a5c-130">Sur le côté droit de la sphère, il y a une fusion du vert émissif et de la lumière ambiante rouge.</span><span class="sxs-lookup"><span data-stu-id="65a5c-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="65a5c-131">Sur le côté gauche de la sphère, le feu vert émissif est mélangé avec un voyant rouge ambiant et diffus produisant un dégradé rouge.</span><span class="sxs-lookup"><span data-stu-id="65a5c-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="65a5c-132">La surbrillance spéculaire est blanche au centre et crée un anneau jaune lorsque la valeur de la lumière spéculaire s’arrête brusquement en laissant les valeurs ambiantes ambiantes, diffuses et émissif qui se mélangent pour s’afficher en jaune.</span><span class="sxs-lookup"><span data-stu-id="65a5c-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![illustration d’une sphère verte avec une lumière émissif](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="65a5c-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65a5c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65a5c-135">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="65a5c-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



