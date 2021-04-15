---
description: La discussion sur la transformation universelle présente les concepts de base et fournit des détails sur la configuration d’une transformation universelle.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformation universelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392415"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="05c5b-103">Transformation universelle (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05c5b-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="05c5b-104">La discussion sur la transformation universelle présente les concepts de base et fournit des détails sur la configuration d’une transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="05c5b-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="05c5b-105">Qu’est-ce qu’une transformation universelle ?</span><span class="sxs-lookup"><span data-stu-id="05c5b-105">What Is a World Transform?</span></span>

<span data-ttu-id="05c5b-106">Une transformation universelle change les coordonnées de l’espace de modèle, où les vertex sont définis par rapport à l’origine locale d’un modèle, à l’espace universel, où les vertex sont définis par rapport à une origine commune à tous les objets d’une scène.</span><span class="sxs-lookup"><span data-stu-id="05c5b-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="05c5b-107">En résumé, la transformation universelle place un modèle dans le monde entier. donc son nom.</span><span class="sxs-lookup"><span data-stu-id="05c5b-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="05c5b-108">Le diagramme suivant montre la relation entre le système de coordonnées universelles et le système de coordonnées local d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="05c5b-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![diagramme de la relation entre les coordonnées universelles et les coordonnées locales](images/worldcrd.png)

<span data-ttu-id="05c5b-110">La transformation universelle peut inclure n’importe quelle combinaison de traductions, de rotations et de mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="05c5b-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="05c5b-111">Configuration d’une matrice mondiale</span><span class="sxs-lookup"><span data-stu-id="05c5b-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="05c5b-112">Comme pour toute autre transformation, créez la transformation universelle en concaténant une série de matrices dans une matrice unique qui contient la somme totale de leurs effets.</span><span class="sxs-lookup"><span data-stu-id="05c5b-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="05c5b-113">Dans le cas le plus simple, lorsqu’un modèle est à l’origine mondiale et que ses axes de coordonnées locales sont orientés de la même façon que l’espace universel, la matrice universelle est la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="05c5b-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="05c5b-114">Plus généralement, la matrice universelle est une combinaison d’une traduction en espace universel et éventuellement d’une ou plusieurs rotations pour transformer le modèle en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="05c5b-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="05c5b-115">L’exemple suivant, issu d’une classe de modèle 3D fictive écrite en C++, utilise les fonctions d’assistance incluses dans la bibliothèque de l’utilitaire D3DX pour créer une matrice universelle qui inclut trois rotations pour orienter un modèle et une translation pour le déplacer par rapport à sa position dans l’espace universel.</span><span class="sxs-lookup"><span data-stu-id="05c5b-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="05c5b-116">Après avoir préparé la matrice universelle, appelez la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) pour la définir, en spécifiant la macro [**D3DTS \_ World**](d3dts-world.md) pour le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="05c5b-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="05c5b-117">Direct3D utilise les matrices universelles et de vue que vous avez définies pour configurer plusieurs structures de données internes.</span><span class="sxs-lookup"><span data-stu-id="05c5b-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="05c5b-118">Chaque fois que vous définissez une nouvelle matrice de monde ou d’affichage, le système recalcule les structures internes associées.</span><span class="sxs-lookup"><span data-stu-id="05c5b-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="05c5b-119">La définition fréquente de ces matrices, par exemple, des milliers de fois par trame, prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="05c5b-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="05c5b-120">Vous pouvez réduire le nombre de calculs requis en concaténant votre monde et en vue des matrices dans une matrice de vue universelle que vous définissez comme matrice universelle, puis en définissant la matrice de vue sur l’identité.</span><span class="sxs-lookup"><span data-stu-id="05c5b-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="05c5b-121">Conservez les copies mises en cache des matrices de monde et de vue individuelles afin de pouvoir modifier, concaténer et réinitialiser la matrice universelle en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="05c5b-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="05c5b-122">Par souci de clarté, dans cette documentation, les exemples Direct3D utilisent rarement cette optimisation.</span><span class="sxs-lookup"><span data-stu-id="05c5b-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="05c5b-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05c5b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05c5b-124">Transformations</span><span class="sxs-lookup"><span data-stu-id="05c5b-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



