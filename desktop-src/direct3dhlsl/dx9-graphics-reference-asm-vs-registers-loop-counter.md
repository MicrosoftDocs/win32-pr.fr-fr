---
title: Registre de compteur de boucles (référence HLSL VS)
description: En savoir plus sur le registre de compteur de boucle pour les nuanceurs de vertex. Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405772"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="a93c6-104">Registre de compteur de boucles (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="a93c6-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="a93c6-105">Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).</span><span class="sxs-lookup"><span data-stu-id="a93c6-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="a93c6-106">Elle est incrémentée automatiquement à chaque exécution de la [boucle, par rapport à](loop---vs.md)... bloc [ENDLOOP-vs](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="a93c6-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="a93c6-107">Il peut donc être utilisé dans le bloc pour l’adressage relatif si nécessaire et n’est pas valide pour l’utiliser en dehors de la boucle.</span><span class="sxs-lookup"><span data-stu-id="a93c6-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a93c6-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a93c6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93c6-109">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="a93c6-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




