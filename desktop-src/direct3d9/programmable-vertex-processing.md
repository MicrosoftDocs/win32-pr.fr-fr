---
description: Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Traitement de vertex programmable (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512868"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="2313e-103">Traitement de vertex programmable (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2313e-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="2313e-104">Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2313e-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="2313e-105">Lorsque l’application écrit dans l’un des registres de vertex de destination, l’élément correspondant dans chaque vertex de la mémoire tampon de vertex de destination est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2313e-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="2313e-106">Les éléments de la mémoire tampon de vertex de destination qui ne sont pas écrits par l’application ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="2313e-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="2313e-107">[**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) échoue si l’application écrit dans des éléments qui ne sont pas présents dans la mémoire tampon de vertex de destination.</span><span class="sxs-lookup"><span data-stu-id="2313e-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2313e-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2313e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2313e-109">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="2313e-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
