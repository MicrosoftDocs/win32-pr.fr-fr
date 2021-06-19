---
title: Registre de compteur de boucles (référence du PS HLSL)
description: En savoir plus sur le registre de compteur de boucle pour les nuanceurs de pixels. Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405512"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="c4164-104">Registre de compteur de boucles (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4164-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="c4164-105">Le seul registre de cette banque est le Registre du compteur de boucles actuel (aL).</span><span class="sxs-lookup"><span data-stu-id="c4164-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="c4164-106">Elle est incrémentée automatiquement à chaque exécution du bloc [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="c4164-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="c4164-107">Il peut donc être utilisé dans le bloc pour l’adressage relatif si nécessaire et n’est pas valide pour l’utiliser en dehors de la boucle.</span><span class="sxs-lookup"><span data-stu-id="c4164-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="c4164-108">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c4164-108">Pixel shader versions</span></span> | <span data-ttu-id="c4164-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="c4164-109">1\_1</span></span> | <span data-ttu-id="c4164-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="c4164-110">1\_2</span></span> | <span data-ttu-id="c4164-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c4164-111">1\_3</span></span> | <span data-ttu-id="c4164-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="c4164-112">1\_4</span></span> | <span data-ttu-id="c4164-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4164-113">2\_0</span></span> | <span data-ttu-id="c4164-114">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c4164-114">2\_sw</span></span> | <span data-ttu-id="c4164-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4164-115">2\_x</span></span> | <span data-ttu-id="c4164-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4164-116">3\_0</span></span> | <span data-ttu-id="c4164-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c4164-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="c4164-118">Registre de compteur de boucle</span><span class="sxs-lookup"><span data-stu-id="c4164-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="c4164-119">x</span><span class="sxs-lookup"><span data-stu-id="c4164-119">x</span></span>    | <span data-ttu-id="c4164-120">x</span><span class="sxs-lookup"><span data-stu-id="c4164-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c4164-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4164-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4164-122">Inscrit</span><span class="sxs-lookup"><span data-stu-id="c4164-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




