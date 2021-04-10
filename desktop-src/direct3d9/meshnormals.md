---
description: Définit les normales d’une maille.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200767"
---
# <a name="meshnormals"></a><span data-ttu-id="936b2-103">MeshNormals</span><span class="sxs-lookup"><span data-stu-id="936b2-103">MeshNormals</span></span>

<span data-ttu-id="936b2-104">Définit les normales d’une maille.</span><span class="sxs-lookup"><span data-stu-id="936b2-104">Defines normals for a mesh.</span></span> <span data-ttu-id="936b2-105">Le premier tableau de vecteurs est les vecteurs normaux eux-mêmes, et le deuxième tableau est un tableau d’index spécifiant les normales qui doivent être appliquées à une face donnée.</span><span class="sxs-lookup"><span data-stu-id="936b2-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="936b2-106">La valeur du membre nFaceNormals doit être égale au nombre de faces dans une maille.</span><span class="sxs-lookup"><span data-stu-id="936b2-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

<span data-ttu-id="936b2-107">Où :</span><span class="sxs-lookup"><span data-stu-id="936b2-107">Where:</span></span>

-   <span data-ttu-id="936b2-108">nNormals-nombre de normales.</span><span class="sxs-lookup"><span data-stu-id="936b2-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="936b2-109">Normals de vecteurs \[ de tableau nNormals \] -tableau de normales.</span><span class="sxs-lookup"><span data-stu-id="936b2-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="936b2-110">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="936b2-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="936b2-111">nFaceNormals-nombre de normales de visage.</span><span class="sxs-lookup"><span data-stu-id="936b2-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="936b2-112">Tableau MeshFace faceNormals \[ nFaceNormals \] -tableau de la face normale de la maille.</span><span class="sxs-lookup"><span data-stu-id="936b2-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="936b2-113">Consultez [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="936b2-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="936b2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="936b2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936b2-115">Modèles</span><span class="sxs-lookup"><span data-stu-id="936b2-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



