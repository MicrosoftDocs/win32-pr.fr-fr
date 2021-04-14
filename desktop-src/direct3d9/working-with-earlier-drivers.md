---
description: Cette section répertorie les problèmes qui peuvent se produire lors de l’utilisation de Direct3D 9 sur des pilotes écrits pour des versions de Direct3D antérieures à Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Utilisation des pilotes antérieurs (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392412"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="cb34c-103">Utilisation des pilotes antérieurs (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cb34c-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="cb34c-104">Cette section répertorie les problèmes qui peuvent se produire lors de l’utilisation de Direct3D 9 sur des pilotes écrits pour des versions de Direct3D antérieures à Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cb34c-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="cb34c-105">Lors de l’utilisation d’un périphérique HAL T&L, l’intensité du brouillard est calculée, mais l’opération de valeur absolue n’est pas appliquée à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="cb34c-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="cb34c-106">Au lieu de cela, la valeur est laissée négative si c’est ce qui est calculé.</span><span class="sxs-lookup"><span data-stu-id="cb34c-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="cb34c-107">La meilleure façon d’éviter cette situation consiste à configurer les transformations de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="cb34c-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="cb34c-108">Une méthode moins recommandée consiste à faire en sorte que les valeurs de début de brouillard et de fin de brouillard soient négatives.</span><span class="sxs-lookup"><span data-stu-id="cb34c-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="cb34c-109">Pour rechercher un pilote Direct3D 9, recherchez une valeur différente de zéro pour D3DDEVCAPS2 \_ STREAMOFFSET dans le membre DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="cb34c-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb34c-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb34c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb34c-111">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="cb34c-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



