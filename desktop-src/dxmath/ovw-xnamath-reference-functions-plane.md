---
description: Répertorie les fonctions plan fournies par DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Fonctions du plan de la bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518995"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="71205-103">Fonctions du plan de la bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="71205-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="71205-104">Répertorie les fonctions plan fournies par DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="71205-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="71205-105">Ces fonctions utilisent un vecteur 4 XMVECTOR pour représenter les coefficients de l’équation plan, ax + par + CZ + D = 0, où le composant X est un, le composant Y est B, le Z-Component est C et le composant W est D.</span><span class="sxs-lookup"><span data-stu-id="71205-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71205-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="71205-106">In this section</span></span>



| <span data-ttu-id="71205-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="71205-107">Topic</span></span>                                                               | <span data-ttu-id="71205-108">Description</span><span class="sxs-lookup"><span data-stu-id="71205-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71205-109">**XMPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="71205-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="71205-110">Calcule le produit scalaire entre un plan d’entrée et un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="71205-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="71205-111">**XMPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="71205-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="71205-112">Calcule le produit scalaire entre un plan d’entrée et un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="71205-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="71205-113">**XMPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="71205-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="71205-114">Calcule le produit scalaire entre le vecteur normal d’un plan et un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="71205-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="71205-115">**XMPlaneEqual**</span><span class="sxs-lookup"><span data-stu-id="71205-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="71205-116">Détermine si deux plans sont égaux.</span><span class="sxs-lookup"><span data-stu-id="71205-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="71205-117">**XMPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="71205-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="71205-118">Calcule l’équation d’un plan construit à partir d’un point dans le plan et d’un vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="71205-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="71205-119">**XMPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="71205-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="71205-120">Calcule l’équation d’un plan construit à partir de trois points dans le plan.</span><span class="sxs-lookup"><span data-stu-id="71205-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="71205-121">**XMPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="71205-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="71205-122">Recherche l’intersection entre un plan et une ligne.</span><span class="sxs-lookup"><span data-stu-id="71205-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="71205-123">**XMPlaneIntersectPlane**</span><span class="sxs-lookup"><span data-stu-id="71205-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="71205-124">Recherche l’intersection de deux plans.</span><span class="sxs-lookup"><span data-stu-id="71205-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="71205-125">**XMPlaneIsInfinite**</span><span class="sxs-lookup"><span data-stu-id="71205-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="71205-126">Teste si l’un des coefficients d’un plan est un infini positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="71205-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="71205-127">**XMPlaneIsNaN**</span><span class="sxs-lookup"><span data-stu-id="71205-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="71205-128">Teste si l’un des coefficients d’un plan est une valeur NaN.</span><span class="sxs-lookup"><span data-stu-id="71205-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="71205-129">**XMPlaneNearEqual**</span><span class="sxs-lookup"><span data-stu-id="71205-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="71205-130">Détermine si deux plans sont presque égaux.</span><span class="sxs-lookup"><span data-stu-id="71205-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="71205-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="71205-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="71205-132">Normalise les coefficients d’un plan afin que les coefficients de x, y et z forment un vecteur normal d’unité.</span><span class="sxs-lookup"><span data-stu-id="71205-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="71205-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="71205-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="71205-134">Estime les coefficients d’un plan afin que les coefficients de x, y et z forment un vecteur normal d’unité.</span><span class="sxs-lookup"><span data-stu-id="71205-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="71205-135">**XMPlaneNotEqual**</span><span class="sxs-lookup"><span data-stu-id="71205-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="71205-136">Détermine si deux plans sont inégaux.</span><span class="sxs-lookup"><span data-stu-id="71205-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="71205-137">**XMPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="71205-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="71205-138">Transforme un plan par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="71205-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="71205-139">**XMPlaneTransformStream**</span><span class="sxs-lookup"><span data-stu-id="71205-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="71205-140">Transforme un flux de plans par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="71205-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="71205-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71205-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71205-142">Fonctions de la bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="71205-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
