---
description: Méthodes BoundingBox
ms.assetid: 68db5936-f0f8-4dbd-a183-b6c3089af0f0
title: Méthodes BoundingBox
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b58c79f202304a289bf1e30447b76ba9ad6dc83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531682"
---
# <a name="boundingbox-methods"></a><span data-ttu-id="c663b-103">Méthodes BoundingBox</span><span class="sxs-lookup"><span data-stu-id="c663b-103">BoundingBox Methods</span></span>



| <span data-ttu-id="c663b-104">Méthode</span><span class="sxs-lookup"><span data-stu-id="c663b-104">Method</span></span>                                                              | <span data-ttu-id="c663b-105">Description</span><span class="sxs-lookup"><span data-stu-id="c663b-105">Description</span></span>                                                                                            |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c663b-106">**Comprend**</span><span class="sxs-lookup"><span data-stu-id="c663b-106">**Contains**</span></span>](boundingbox-contains.md)<br/>                 | <span data-ttu-id="c663b-107">Teste si BoundingBox contient un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="c663b-107">Tests whether the BoundingBox contains a specified object.</span></span><br/>                                  |
| [<span data-ttu-id="c663b-108">**CreateFromPoints**</span><span class="sxs-lookup"><span data-stu-id="c663b-108">**CreateFromPoints**</span></span>](boundingbox-createfrompoints.md)<br/> | <span data-ttu-id="c663b-109">Crée un BoundingBox à partir de points.</span><span class="sxs-lookup"><span data-stu-id="c663b-109">Creates a BoundingBox from points.</span></span><br/>                                                          |
| [<span data-ttu-id="c663b-110">**Croise**</span><span class="sxs-lookup"><span data-stu-id="c663b-110">**Intersects**</span></span>](boundingbox-intersects.md)<br/>             | <span data-ttu-id="c663b-111">Teste BoundingBox pour l’intersection avec un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c663b-111">Tests the BoundingBox for intersection with another object.</span></span><br/>                                 |
| [<span data-ttu-id="c663b-112">**Transform**</span><span class="sxs-lookup"><span data-stu-id="c663b-112">**Transform**</span></span>](boundingbox-transform.md)<br/>               | <span data-ttu-id="c663b-113">Transforme le BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="c663b-113">Transforms the BoundingBox.</span></span><br/>                                                                 |
| [<span data-ttu-id="c663b-114">**ContainedBy**</span><span class="sxs-lookup"><span data-stu-id="c663b-114">**ContainedBy**</span></span>](/windows/desktop/api/DirectXCollision/nf-directxcollision-boundingbox-containedby)<br/>           | <span data-ttu-id="c663b-115">Teste si l' [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) est contenu dans le frustum spécifié.</span><span class="sxs-lookup"><span data-stu-id="c663b-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) is contained by the specified frustum.</span></span><br/> |
| [<span data-ttu-id="c663b-116">**CreateFromSphere**</span><span class="sxs-lookup"><span data-stu-id="c663b-116">**CreateFromSphere**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfromsphere)<br/> | <span data-ttu-id="c663b-117">Crée un BoundingBox suffisamment grand pour contenir le BoundingSphere spécifié.</span><span class="sxs-lookup"><span data-stu-id="c663b-117">Creates a BoundingBox large enough to contain the a specified BoundingSphere.</span></span><br/>               |
| [<span data-ttu-id="c663b-118">**CreateMerged**</span><span class="sxs-lookup"><span data-stu-id="c663b-118">**CreateMerged**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createmerged)<br/>         | <span data-ttu-id="c663b-119">Crée un BoundingBox suffisamment grand pour contenir deux instances BoundBox spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c663b-119">Creates a BoundingBox large enough to contains two specified BoundBox intances.</span></span><br/>             |
| [<span data-ttu-id="c663b-120">**GetCorners**</span><span class="sxs-lookup"><span data-stu-id="c663b-120">**GetCorners**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-getcorners)<br/>             | <span data-ttu-id="c663b-121">Récupère les angles du BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="c663b-121">Retrieves the corners of the BoundingBox.</span></span><br/>                                                   |
| [<span data-ttu-id="c663b-122">**affectation d’opérations \_**</span><span class="sxs-lookup"><span data-stu-id="c663b-122">**op\_Assignment**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-operator-assign)<br/>      | <span data-ttu-id="c663b-123">Copie les valeurs d’un autre BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="c663b-123">Copies values from another BoundingBox.</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c663b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c663b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c663b-125">BoundingBox</span><span class="sxs-lookup"><span data-stu-id="c663b-125">BoundingBox</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
