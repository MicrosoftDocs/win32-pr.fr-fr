---
title: Registre de compteur de boucles (référence du PS HLSL)
description: Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679226"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="234dc-103">Registre de compteur de boucles (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="234dc-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="234dc-104">Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).</span><span class="sxs-lookup"><span data-stu-id="234dc-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="234dc-105">Elle est incrémentée automatiquement à chaque exécution du bloc [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="234dc-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="234dc-106">Il peut donc être utilisé dans le bloc pour l’adressage relatif si nécessaire et n’est pas valide pour l’utiliser en dehors de la boucle.</span><span class="sxs-lookup"><span data-stu-id="234dc-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="234dc-107">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="234dc-107">Pixel shader versions</span></span> | <span data-ttu-id="234dc-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="234dc-108">1\_1</span></span> | <span data-ttu-id="234dc-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="234dc-109">1\_2</span></span> | <span data-ttu-id="234dc-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="234dc-110">1\_3</span></span> | <span data-ttu-id="234dc-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="234dc-111">1\_4</span></span> | <span data-ttu-id="234dc-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="234dc-112">2\_0</span></span> | <span data-ttu-id="234dc-113">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="234dc-113">2\_sw</span></span> | <span data-ttu-id="234dc-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="234dc-114">2\_x</span></span> | <span data-ttu-id="234dc-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="234dc-115">3\_0</span></span> | <span data-ttu-id="234dc-116">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="234dc-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="234dc-117">Registre de compteur de boucle</span><span class="sxs-lookup"><span data-stu-id="234dc-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="234dc-118">x</span><span class="sxs-lookup"><span data-stu-id="234dc-118">x</span></span>    | <span data-ttu-id="234dc-119">x</span><span class="sxs-lookup"><span data-stu-id="234dc-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="234dc-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="234dc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="234dc-121">Inscrit</span><span class="sxs-lookup"><span data-stu-id="234dc-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




