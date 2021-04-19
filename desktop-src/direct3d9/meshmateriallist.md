---
description: Utilisé dans un objet de maillage pour spécifier les éléments qui s’appliquent aux visages. Le membre nMaterials spécifie le nombre de matériaux présents, et les matériaux spécifient la matière à appliquer.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514068"
---
# <a name="meshmateriallist"></a><span data-ttu-id="ec16a-104">MeshMaterialList</span><span class="sxs-lookup"><span data-stu-id="ec16a-104">MeshMaterialList</span></span>

<span data-ttu-id="ec16a-105">Utilisé dans un objet de maillage pour spécifier les éléments qui s’appliquent aux visages.</span><span class="sxs-lookup"><span data-stu-id="ec16a-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="ec16a-106">Le membre nMaterials spécifie le nombre de matériaux présents, et les matériaux spécifient la matière à appliquer.</span><span class="sxs-lookup"><span data-stu-id="ec16a-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="ec16a-107">Où :</span><span class="sxs-lookup"><span data-stu-id="ec16a-107">Where:</span></span>

-   <span data-ttu-id="ec16a-108">nMaterials : DWORD.</span><span class="sxs-lookup"><span data-stu-id="ec16a-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="ec16a-109">Nombre de matériaux.</span><span class="sxs-lookup"><span data-stu-id="ec16a-109">The number of materials.</span></span>
-   <span data-ttu-id="ec16a-110">nFaceIndexes : DWORD.</span><span class="sxs-lookup"><span data-stu-id="ec16a-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="ec16a-111">Nombre d'indices.</span><span class="sxs-lookup"><span data-stu-id="ec16a-111">The number of indices.</span></span>
-   <span data-ttu-id="ec16a-112">faceIndexes \[ nFaceIndexes \] : tableau de DWORDS contenant les indices de face.</span><span class="sxs-lookup"><span data-stu-id="ec16a-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec16a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec16a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec16a-114">Modèles</span><span class="sxs-lookup"><span data-stu-id="ec16a-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



