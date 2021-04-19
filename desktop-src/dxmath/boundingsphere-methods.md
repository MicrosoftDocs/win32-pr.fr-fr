---
description: Méthodes BoundingSphere
ms.assetid: 902e69c1-4006-4d36-a14c-4b0b0cae8494
title: Méthodes BoundingSphere
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa908250155a0da45dcefccbbaf7fb3c019b8624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544248"
---
# <a name="boundingsphere-methods"></a><span data-ttu-id="a490e-103">Méthodes BoundingSphere</span><span class="sxs-lookup"><span data-stu-id="a490e-103">BoundingSphere Methods</span></span>



| <span data-ttu-id="a490e-104">Méthode</span><span class="sxs-lookup"><span data-stu-id="a490e-104">Method</span></span>                                                                           | <span data-ttu-id="a490e-105">Description</span><span class="sxs-lookup"><span data-stu-id="a490e-105">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a490e-106">**Comprend**</span><span class="sxs-lookup"><span data-stu-id="a490e-106">**Contains**</span></span>](boundingsphere-contains.md)<br/>                           | <span data-ttu-id="a490e-107">Teste si le BoundingSphere contient un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="a490e-107">Tests whether the BoundingSphere contains a specified object.</span></span><br/>                                     |
| [<span data-ttu-id="a490e-108">**Croise**</span><span class="sxs-lookup"><span data-stu-id="a490e-108">**Intersects**</span></span>](boundingsphere-intersects.md)<br/>                       | <span data-ttu-id="a490e-109">Teste le BoundingSphere pour l’intersection avec un objet.</span><span class="sxs-lookup"><span data-stu-id="a490e-109">Tests the BoundingSphere for intersection with an object.</span></span><br/>                                         |
| [<span data-ttu-id="a490e-110">**Transform**</span><span class="sxs-lookup"><span data-stu-id="a490e-110">**Transform**</span></span>](boundingsphere-transform.md)<br/>                         | <span data-ttu-id="a490e-111">Transforme le BoundingSphere.</span><span class="sxs-lookup"><span data-stu-id="a490e-111">Transforms the BoundingSphere.</span></span><br/>                                                                    |
| [<span data-ttu-id="a490e-112">**ContainedBy**</span><span class="sxs-lookup"><span data-stu-id="a490e-112">**ContainedBy**</span></span>](/windows/desktop/api/DirectXCollision/nf-directxcollision-boundingbox-containedby)<br/>                     | <span data-ttu-id="a490e-113">Teste si le [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) est contenu dans le frustum spécifié.</span><span class="sxs-lookup"><span data-stu-id="a490e-113">Tests whether the [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere) is contained by the specified frustum.</span></span><br/> |
| <span data-ttu-id="a490e-114">[**CreateFromBoundingBox**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfromboundingbox(boundingsphere__constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="a490e-114">[**CreateFromBoundingBox**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfromboundingbox(boundingsphere__constboundingorientedbox_))</span></span><br/> | <span data-ttu-id="a490e-115">Crée un BoundingSphere contenant le BoundingBox spécifié.</span><span class="sxs-lookup"><span data-stu-id="a490e-115">Creates a BoundingSphere containing the specified BoundingBox.</span></span><br/>                                    |
| [<span data-ttu-id="a490e-116">**CreateFromPoints**</span><span class="sxs-lookup"><span data-stu-id="a490e-116">**CreateFromPoints**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)<br/>           | <span data-ttu-id="a490e-117">Crée un BoundingSphere à partir d’une liste de points.</span><span class="sxs-lookup"><span data-stu-id="a490e-117">Creates a new BoundingSphere from a list of points.</span></span><br/>                                               |
| [<span data-ttu-id="a490e-118">**CreateMerged**</span><span class="sxs-lookup"><span data-stu-id="a490e-118">**CreateMerged**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createmerged)<br/>                   | <span data-ttu-id="a490e-119">Crée un BoundingSphere qui contient les deux objets BoundingSphere spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a490e-119">Creates a BoundingSphere that contains the two specified BoundingSphere objects.</span></span><br/>                  |
| <span data-ttu-id="a490e-120">[**affectation d’opérations \_**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-operator-assign(boundingsphere__))</span><span class="sxs-lookup"><span data-stu-id="a490e-120">[**op\_Assignment**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-operator-assign(boundingsphere__))</span></span><br/>                | <span data-ttu-id="a490e-121">Initialise le BoundingSphere avec les valeurs d’un BoundingSphere spécifié.</span><span class="sxs-lookup"><span data-stu-id="a490e-121">Initializes the BoundingSphere with values from a specified BoundingSphere.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="a490e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a490e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a490e-123">BoundingSphere</span><span class="sxs-lookup"><span data-stu-id="a490e-123">BoundingSphere</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere)
</dt> </dl>

 

 
