---
description: Ces constantes s’appliquent aux variables d’effet.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Constantes D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514741"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="56f3d-103">\_Constantes de variable d’effet D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="56f3d-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="56f3d-104">Ces constantes s’appliquent aux variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="56f3d-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="56f3d-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="56f3d-105">\#define</span></span>                                       | <span data-ttu-id="56f3d-106">Description</span><span class="sxs-lookup"><span data-stu-id="56f3d-106">Description</span></span>  | <span data-ttu-id="56f3d-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="56f3d-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f3d-108">\_Annotation de \_ variable d’effet D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="56f3d-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="56f3d-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="56f3d-109">1 << 0</span></span> | <span data-ttu-id="56f3d-110">Indique qu’il s’agit d’une annotation ou d’une variable globale.</span><span class="sxs-lookup"><span data-stu-id="56f3d-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="56f3d-111">\_Variable d’effet D3D10 \_ \_ regroupée</span><span class="sxs-lookup"><span data-stu-id="56f3d-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="56f3d-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="56f3d-112">1 << 1</span></span> | <span data-ttu-id="56f3d-113">Indique que cette variable ou cette mémoire tampon constante réside dans un pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="56f3d-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="56f3d-114">Si cet indicateur n’est pas défini, la variable réside dans un effet autonome ou un effet enfant (les effets autonomes renvoient la valeur false à partir de [**ID3D10Effect :: IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span><span class="sxs-lookup"><span data-stu-id="56f3d-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="56f3d-115">\_Point de \_ \_ liaison explicite \_ \_ de la variable d’effet D3D10</span><span class="sxs-lookup"><span data-stu-id="56f3d-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="56f3d-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="56f3d-116">1 << 2</span></span> | <span data-ttu-id="56f3d-117">Indique que la variable a été explicitement liée à l’aide du mot clé Register.</span><span class="sxs-lookup"><span data-stu-id="56f3d-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="56f3d-118">Ces indicateurs sont définis en tant que macros dans d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="56f3d-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56f3d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56f3d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f3d-120">Effets, constantes (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="56f3d-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



