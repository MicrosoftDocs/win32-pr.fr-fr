---
title: DirectXMath, fonctions de transformation de vecteur 3D
description: Répertorie les fonctions de transformation vectorielle 3D.
ms.assetid: 148972da-e460-63b9-6b01-10201f63d157
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a592071970d69d7ef4b4db42960335c5fc771ac3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517588"
---
# <a name="directxmath-3d-vector-transformation-functions"></a><span data-ttu-id="2da13-103">DirectXMath, fonctions de transformation de vecteur 3D</span><span class="sxs-lookup"><span data-stu-id="2da13-103">DirectXMath 3D vector transformation functions</span></span>

<span data-ttu-id="2da13-104">Répertorie les fonctions de transformation vectorielle 3D.</span><span class="sxs-lookup"><span data-stu-id="2da13-104">Lists the 3D vector transformation functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2da13-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="2da13-105">In this section</span></span>



| <span data-ttu-id="2da13-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2da13-106">Topic</span></span>                                                                               | <span data-ttu-id="2da13-107">Description</span><span class="sxs-lookup"><span data-stu-id="2da13-107">Description</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da13-108">**XMVector3InverseRotate**</span><span class="sxs-lookup"><span data-stu-id="2da13-108">**XMVector3InverseRotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3inverserotate)<br/>                 | <span data-ttu-id="2da13-109">Fait pivoter un vecteur 3D à l’aide de l’inverse d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="2da13-109">Rotates a 3D vector using the inverse of a quaternion.</span></span><br/>                                                                                |
| [<span data-ttu-id="2da13-110">**XMVector3Project**</span><span class="sxs-lookup"><span data-stu-id="2da13-110">**XMVector3Project**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)<br/>                             | <span data-ttu-id="2da13-111">Projetez un vecteur 3D à partir de l’espace d’objet dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2da13-111">Project a 3D vector from object space into screen space.</span></span><br/>                                                                              |
| [<span data-ttu-id="2da13-112">**XMVector3ProjectStream**</span><span class="sxs-lookup"><span data-stu-id="2da13-112">**XMVector3ProjectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)<br/>                 | <span data-ttu-id="2da13-113">Projette un flux de vecteurs 3D à partir de l’espace d’objet dans l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2da13-113">Projects a stream of 3D vectors from object space into screen space.</span></span><br/>                                                                  |
| [<span data-ttu-id="2da13-114">**XMVector3Rotate**</span><span class="sxs-lookup"><span data-stu-id="2da13-114">**XMVector3Rotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3rotate)<br/>                               | <span data-ttu-id="2da13-115">Fait pivoter un vecteur 3D à l’aide d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="2da13-115">Rotates a 3D vector using a quaternion.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2da13-116">**XMVector3Transform**</span><span class="sxs-lookup"><span data-stu-id="2da13-116">**XMVector3Transform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)<br/>                         | <span data-ttu-id="2da13-117">Transforme un vecteur 3D par une matrice.</span><span class="sxs-lookup"><span data-stu-id="2da13-117">Transforms a 3D vector by a matrix.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2da13-118">**XMVector3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="2da13-118">**XMVector3TransformCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)<br/>               | <span data-ttu-id="2da13-119">Transforme un vecteur 3D par une matrice donnée, en reprojetant le résultat dans w = 1.</span><span class="sxs-lookup"><span data-stu-id="2da13-119">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span><br/>                                                      |
| [<span data-ttu-id="2da13-120">**XMVector3TransformCoordStream**</span><span class="sxs-lookup"><span data-stu-id="2da13-120">**XMVector3TransformCoordStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)<br/>   | <span data-ttu-id="2da13-121">Transforme un flux de vecteurs 3D par une matrice donnée, en projetant les vecteurs résultants de telle sorte que leurs coordonnées w soient égales à 1,0.</span><span class="sxs-lookup"><span data-stu-id="2da13-121">Transforms a stream of 3D vectors by a given matrix, projecting the resulting vectors such that their w coordinates are equal to 1.0.</span></span><br/> |
| [<span data-ttu-id="2da13-122">**XMVector3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="2da13-122">**XMVector3TransformNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)<br/>             | <span data-ttu-id="2da13-123">Transforme le vecteur 3D normal par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="2da13-123">Transforms the 3D vector normal by the given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="2da13-124">**XMVector3TransformNormalStream**</span><span class="sxs-lookup"><span data-stu-id="2da13-124">**XMVector3TransformNormalStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)<br/> | <span data-ttu-id="2da13-125">Transforme un flux de vecteurs normaux 3D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="2da13-125">Transforms a stream of 3D normal vectors by a given matrix.</span></span><br/>                                                                           |
| [<span data-ttu-id="2da13-126">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="2da13-126">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)<br/>             | <span data-ttu-id="2da13-127">Transforme un flux de vecteurs 3D par une matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="2da13-127">Transforms a stream of 3D vectors by a given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="2da13-128">**XMVector3Unproject**</span><span class="sxs-lookup"><span data-stu-id="2da13-128">**XMVector3Unproject**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)<br/>                         | <span data-ttu-id="2da13-129">Projette un vecteur 3D à partir de l’espace à l’écran dans l’espace d’objet.</span><span class="sxs-lookup"><span data-stu-id="2da13-129">Projects a 3D vector from screen space into object space.</span></span><br/>                                                                             |
| [<span data-ttu-id="2da13-130">**XMVector3UnprojectStream**</span><span class="sxs-lookup"><span data-stu-id="2da13-130">**XMVector3UnprojectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)<br/>             | <span data-ttu-id="2da13-131">Transforme un flux de vecteurs 3D de l’espace à l’écran en espace d’objet.</span><span class="sxs-lookup"><span data-stu-id="2da13-131">Transforms a stream of 3D vectors from screen space to object space.</span></span><br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="2da13-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2da13-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da13-133">Fonctions de vecteur 3D de la bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="2da13-133">DirectXMath Library 3D Vector Functions</span></span>](ovw-xnamath-reference-functions-vector3.md)
</dt> </dl>

 

 
