---
description: Un ensemble secondaire d’interfaces de rendu prend en charge la transmission de données de vertex et d’index directement à partir de pointeurs de mémoire utilisateur. Ces interfaces ne prennent en charge qu’un seul flux de données de vertex. Pour plus d’informations, consultez les rubriques de référence suivantes.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Rendu à partir de pointeurs de mémoire utilisateur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200777"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a><span data-ttu-id="f3b28-105">Rendu à partir de pointeurs de mémoire utilisateur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f3b28-105">Rendering from User Memory Pointers (Direct3D 9)</span></span>

<span data-ttu-id="f3b28-106">Un ensemble secondaire d’interfaces de rendu prend en charge la transmission de données de vertex et d’index directement à partir de pointeurs de mémoire utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3b28-106">A secondary set of rendering interfaces supports passing vertex and index data directly from user memory pointers.</span></span> <span data-ttu-id="f3b28-107">Ces interfaces ne prennent en charge qu’un seul flux de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="f3b28-107">These interfaces support a single stream of vertex data only.</span></span> <span data-ttu-id="f3b28-108">Pour plus d’informations, consultez les rubriques de référence suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3b28-108">For more information, see the following reference topics.</span></span>

-   [<span data-ttu-id="f3b28-109">**IDirect3DDevice9 ::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="f3b28-109">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [<span data-ttu-id="f3b28-110">**IDirect3DDevice9 ::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="f3b28-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

<span data-ttu-id="f3b28-111">Ces méthodes s’affichent avec les données spécifiées par les pointeurs de mémoire utilisateur, au lieu des mémoires tampons de vertex et d’index.</span><span class="sxs-lookup"><span data-stu-id="f3b28-111">These methods render with data specified by user memory pointers, instead of vertex and index buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3b28-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3b28-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b28-113">Rendu des primitives</span><span class="sxs-lookup"><span data-stu-id="f3b28-113">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
