---
description: Utilisé pour définir la topologie de texture de chaque visage dans un retour à la ligne. La valeur du membre nFaceWrapValues doit être égale au nombre de faces dans une maille.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520484"
---
# <a name="meshfacewraps"></a><span data-ttu-id="c2a75-104">MeshFaceWraps</span><span class="sxs-lookup"><span data-stu-id="c2a75-104">MeshFaceWraps</span></span>

<span data-ttu-id="c2a75-105">Utilisé pour définir la topologie de texture de chaque visage dans un retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="c2a75-105">Used to define the texture topology of each face in a wrap.</span></span> <span data-ttu-id="c2a75-106">La valeur du membre nFaceWrapValues doit être égale au nombre de faces dans une maille.</span><span class="sxs-lookup"><span data-stu-id="c2a75-106">The value of the nFaceWrapValues member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

<span data-ttu-id="c2a75-107">Ce modèle n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2a75-107">This template is no longer used.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2a75-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2a75-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a75-109">Modèles</span><span class="sxs-lookup"><span data-stu-id="c2a75-109">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



