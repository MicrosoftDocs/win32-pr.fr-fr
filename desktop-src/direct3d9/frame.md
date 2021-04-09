---
description: Définit un cadre de coordonnées, ou &\# 0034 ; cadre de référence. &\# 0034 ; Le modèle de frame est ouvert et peut contenir n’importe quel objet. Les fonctions de maillage de D3DX reconnaissent les instances de modèle Mesh, FrameTransformMatrix et Frame comme des objets enfants lors du chargement d’une instance de frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (Direct3D 9 Graphics)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845969"
---
# <a name="frame-direct3d-9-graphics"></a><span data-ttu-id="c6686-104">Frame (Direct3D 9 Graphics)</span><span class="sxs-lookup"><span data-stu-id="c6686-104">Frame (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="c6686-105">Définit un cadre de coordonnées, ou « cadre de référence ».</span><span class="sxs-lookup"><span data-stu-id="c6686-105">Defines a coordinate frame, or "frame of reference."</span></span> <span data-ttu-id="c6686-106">Le modèle de frame est ouvert et peut contenir n’importe quel objet.</span><span class="sxs-lookup"><span data-stu-id="c6686-106">The Frame template is open and can contain any object.</span></span> <span data-ttu-id="c6686-107">Les fonctions de maillage de D3DX reconnaissent les instances de modèle [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)et **Frame** comme des objets enfants lors du chargement d’une instance de **Frame** .</span><span class="sxs-lookup"><span data-stu-id="c6686-107">The D3DX mesh-loading functions recognize [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md), and **Frame** template instances as child objects when loading a **Frame** instance.</span></span>

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

<span data-ttu-id="c6686-108">Le modèle de frame reconnaît les nœuds **Frame** et de [**maillage**](mesh.md) enfants à l’intérieur d’un frame et peut reconnaître les modèles définis par l’utilisateur par le biais d’une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="c6686-108">The frame template recognizes child **Frame** and [**Mesh**](mesh.md) nodes inside a frame and can recognize user-defined templates through a callback function.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6686-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6686-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6686-110">Modèles</span><span class="sxs-lookup"><span data-stu-id="c6686-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



