---
description: Ces constantes sont utilisées lors de la création d’un effet pour définir le comportement de compilation ou le comportement de l’effet d’exécution.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Constantes D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317841"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="7d171-103">\_Constantes d’effet D3D10</span><span class="sxs-lookup"><span data-stu-id="7d171-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="7d171-104">Ces constantes sont utilisées lors de la création d’un effet pour définir le comportement de compilation ou le comportement de l’effet d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7d171-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="7d171-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="7d171-105">\#define</span></span>                                 | <span data-ttu-id="7d171-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d171-106">Value</span></span>        | <span data-ttu-id="7d171-107">Description</span><span class="sxs-lookup"><span data-stu-id="7d171-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d171-108">Effet D3D10 compiler l’effet \_ \_ \_ enfant \_</span><span class="sxs-lookup"><span data-stu-id="7d171-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="7d171-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="7d171-109">1 << 0</span></span> | <span data-ttu-id="7d171-110">Compilez le fichier. FX à un effet enfant.</span><span class="sxs-lookup"><span data-stu-id="7d171-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="7d171-111">Les effets enfants n’ont aucune initialisation pour les valeurs partagées, car celles-ci sont initialisées dans le pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="7d171-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="7d171-112">D3D10 \_ effet \_ compiler \_ autoriser \_ les \_ opérations lentes</span><span class="sxs-lookup"><span data-stu-id="7d171-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="7d171-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="7d171-113">1 << 1</span></span> | <span data-ttu-id="7d171-114">Par défaut, le mode de performance est activé.</span><span class="sxs-lookup"><span data-stu-id="7d171-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="7d171-115">Le mode de performance interdit les objets d’État mutable en empêchant les expressions non littérales d’apparaître dans les définitions d’objets d’État.</span><span class="sxs-lookup"><span data-stu-id="7d171-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="7d171-116">La spécification de cet indicateur désactivera le mode et autorisera les objets d’État mutable.</span><span class="sxs-lookup"><span data-stu-id="7d171-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="7d171-117">D3D10 \_ effet \_ à \_ thread unique</span><span class="sxs-lookup"><span data-stu-id="7d171-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="7d171-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="7d171-118">1 << 3</span></span> | <span data-ttu-id="7d171-119">N’essayez pas de synchroniser avec d’autres threads qui chargent des effets dans le même pool.</span><span class="sxs-lookup"><span data-stu-id="7d171-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="7d171-120">Ces constantes sont définies en tant que macros dans d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="7d171-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d171-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d171-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d171-122">Effets, constantes (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7d171-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



