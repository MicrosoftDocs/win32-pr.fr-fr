---
description: Cette section présente les concepts de base de la transformation de vue et fournit des détails sur la configuration d’une matrice de transformation de vue dans une application Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Vue de la transformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521908"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="d400e-103">Vue de la transformation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d400e-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="d400e-104">Cette section présente les concepts de base de la transformation de vue et fournit des détails sur la configuration d’une matrice de transformation de vue dans une application Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d400e-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="d400e-105">La transformation de vue localise la visionneuse dans l’espace universel, en transformant les vertex en espace de caméra.</span><span class="sxs-lookup"><span data-stu-id="d400e-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="d400e-106">Dans l’espace de l’appareil photo, l’appareil photo, ou la visionneuse, est à l’origine, en regardant l’axe z positif.</span><span class="sxs-lookup"><span data-stu-id="d400e-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="d400e-107">Rappelez-vous que Direct3D utilise un système de coordonnées gauche, donc z est positif dans une scène.</span><span class="sxs-lookup"><span data-stu-id="d400e-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="d400e-108">La matrice de vue déplace les objets dans le monde autour de la position d’un appareil photo : l’origine de l’espace et de l’orientation de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d400e-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="d400e-109">Il existe plusieurs façons de créer une matrice de vue.</span><span class="sxs-lookup"><span data-stu-id="d400e-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="d400e-110">Dans tous les cas, la caméra a une position logique et une orientation dans l’espace universel qui est utilisée comme point de départ pour créer une matrice de vue qui sera appliquée aux modèles dans une scène.</span><span class="sxs-lookup"><span data-stu-id="d400e-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="d400e-111">La matrice de vue traduit et fait pivoter les objets pour les placer dans l’espace de l’appareil photo, où l’appareil photo est à l’origine.</span><span class="sxs-lookup"><span data-stu-id="d400e-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="d400e-112">Une façon de créer une matrice de vue consiste à combiner une matrice de translation avec des matrices de rotation pour chaque axe.</span><span class="sxs-lookup"><span data-stu-id="d400e-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="d400e-113">Dans cette approche, l’équation de matrice générale suivante s’applique.</span><span class="sxs-lookup"><span data-stu-id="d400e-113">In this approach, the following general matrix equation applies.</span></span>

![équation de la transformation de la vue](images/viewtran.png)

<span data-ttu-id="d400e-115">Dans cette formule, V est la matrice de vue en cours de création, T est une matrice de translation qui repositionne les objets dans le monde, et R ₓ à R<sub>z</sub> sont des matrices de rotation qui font pivoter les objets le long des axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="d400e-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="d400e-116">Les matrices translation et rotation sont basées sur la position logique et l’orientation de l’appareil photo dans l’espace universel.</span><span class="sxs-lookup"><span data-stu-id="d400e-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="d400e-117">Donc, si la position logique de l’appareil photo dans le monde est <10 20100>, l’objectif de la matrice de translation est de déplacer les objets de 10 unités le long de l’axe x,-20 unités le long de l’axe y et-100 unités le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="d400e-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="d400e-118">Les matrices de rotation de la formule sont basées sur l’orientation de l’appareil photo, en termes d’alignement de l’espace de l’appareil photo par rapport à l’espace universel.</span><span class="sxs-lookup"><span data-stu-id="d400e-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="d400e-119">Par exemple, si l’appareil photo mentionné précédemment pointe vers le haut, son axe z est de 90 degrés (pi/2 radians) hors alignement avec l’axe z de l’espace universel, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d400e-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![illustration de l’espace d’affichage de la caméra par rapport à l’espace universel](images/camtop.png)

<span data-ttu-id="d400e-121">Les matrices de rotation appliquent des rotations de grandeur égale, mais opposée, aux modèles de la scène.</span><span class="sxs-lookup"><span data-stu-id="d400e-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="d400e-122">La matrice de vue pour cette caméra comprend une rotation de-90 degrés autour de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="d400e-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="d400e-123">La matrice de rotation est associée à la matrice de translation pour créer une matrice de vue qui ajuste la position et l’orientation des objets dans la scène afin que le haut de la caméra soit orienté vers la caméra, ce qui donne l’impression que l’appareil photo est au-dessus du modèle.</span><span class="sxs-lookup"><span data-stu-id="d400e-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="d400e-124">Configuration d’une matrice de vue</span><span class="sxs-lookup"><span data-stu-id="d400e-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="d400e-125">Les fonctions d’assistance [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) et [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) créent une matrice de vue basée sur l’emplacement de l’appareil photo et un point d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d400e-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="d400e-126">L’exemple suivant crée une matrice de vue pour les coordonnées de gauche.</span><span class="sxs-lookup"><span data-stu-id="d400e-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="d400e-127">Direct3D utilise les matrices universelles et de vue pour configurer plusieurs structures de données internes.</span><span class="sxs-lookup"><span data-stu-id="d400e-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="d400e-128">Chaque fois que vous définissez une nouvelle matrice de monde ou d’affichage, le système recalcule les structures internes associées.</span><span class="sxs-lookup"><span data-stu-id="d400e-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="d400e-129">La définition fréquente de ces matrices est fastidieuse.</span><span class="sxs-lookup"><span data-stu-id="d400e-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="d400e-130">Vous pouvez réduire le nombre de calculs requis en concaténant votre monde et en vue des matrices dans une matrice de vue universelle que vous définissez comme matrice universelle, puis en définissant la matrice de vue sur l’identité.</span><span class="sxs-lookup"><span data-stu-id="d400e-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="d400e-131">Conservez les copies mises en cache des matrices de monde et de vue individuelles que vous pouvez modifier, concaténer et réinitialiser la matrice universelle en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="d400e-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="d400e-132">Par souci de clarté, les exemples utilisent rarement cette optimisation.</span><span class="sxs-lookup"><span data-stu-id="d400e-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d400e-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d400e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d400e-134">Transformations</span><span class="sxs-lookup"><span data-stu-id="d400e-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



