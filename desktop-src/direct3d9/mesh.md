---
description: Définit un maillage simple. Le premier tableau est une liste de vertex, tandis que le deuxième tableau définit les visages de la maille en indexant dans le tableau de vertex.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Maillage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480697"
---
# <a name="mesh"></a><span data-ttu-id="f174a-104">Maillage</span><span class="sxs-lookup"><span data-stu-id="f174a-104">Mesh</span></span>

<span data-ttu-id="f174a-105">Définit un maillage simple.</span><span class="sxs-lookup"><span data-stu-id="f174a-105">Defines a simple mesh.</span></span> <span data-ttu-id="f174a-106">Le premier tableau est une liste de vertex, tandis que le deuxième tableau définit les visages de la maille en indexant dans le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="f174a-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

<span data-ttu-id="f174a-107">Où :</span><span class="sxs-lookup"><span data-stu-id="f174a-107">Where:</span></span>

-   <span data-ttu-id="f174a-108">nVertices-nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="f174a-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="f174a-109">sommets de vecteurs \[ de tableau nVertices \] -tableau de vertex, chacun de type Vector.</span><span class="sxs-lookup"><span data-stu-id="f174a-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="f174a-110">Consultez [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="f174a-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="f174a-111">nFaces-nombre de visages.</span><span class="sxs-lookup"><span data-stu-id="f174a-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="f174a-112">le tableau MeshFace \[ face \] à nFaces-Array of faces, chacun de type MeshFace.</span><span class="sxs-lookup"><span data-stu-id="f174a-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="f174a-113">Consultez [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="f174a-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="f174a-114">\[ ... \] -N’importe quel modèle de fichier. x peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="f174a-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="f174a-115">L’architecture est ainsi extensible.</span><span class="sxs-lookup"><span data-stu-id="f174a-115">This makes the architecture extensible.</span></span> <span data-ttu-id="f174a-116">Les modèles [**Material**](material.md) et [**TextureFilename**](texturefilename.md) sont généralement utilisés.</span><span class="sxs-lookup"><span data-stu-id="f174a-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="f174a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f174a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f174a-118">Modèles</span><span class="sxs-lookup"><span data-stu-id="f174a-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



