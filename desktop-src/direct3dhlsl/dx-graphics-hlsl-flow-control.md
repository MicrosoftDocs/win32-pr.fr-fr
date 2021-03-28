---
title: Contrôle de flux
description: La plupart du matériel est conçu pour exécuter le code de nuanceur ligne par ligne, en exécutant chaque instruction HLSL une seule fois.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309669"
---
# <a name="flow-control"></a><span data-ttu-id="4c2a0-103">Contrôle de flux</span><span class="sxs-lookup"><span data-stu-id="4c2a0-103">Flow Control</span></span>

<span data-ttu-id="4c2a0-104">La plupart du matériel est conçu pour exécuter le code de nuanceur ligne par ligne, en exécutant chaque instruction HLSL une seule fois.</span><span class="sxs-lookup"><span data-stu-id="4c2a0-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="4c2a0-105">Une instruction Flow-Control détermine au moment de l’exécution le bloc d’instructions HLSL à exécuter ensuite.</span><span class="sxs-lookup"><span data-stu-id="4c2a0-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="4c2a0-106">À l’aide d’une instruction de contrôle de Flow, un nuanceur peut parcourir un ensemble d’instructions ou sauter (branche) à une instruction autre que celle sur la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="4c2a0-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="4c2a0-107">Certaines instructions de contrôle de Flow prennent en charge le contrôle statique spécifié au moment de la compilation. d’autres proposent un contrôle prédicat qui est une décision par composant effectuée au moment de l’exécution, et d’autres encore prennent en charge le contrôle dynamique, qui est une décision prise au moment de l’exécution en fonction du contenu d’une variable.</span><span class="sxs-lookup"><span data-stu-id="4c2a0-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="4c2a0-108">Le langage HLSL prend en charge les instructions de contrôle de Flow suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c2a0-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="4c2a0-109">break</span><span class="sxs-lookup"><span data-stu-id="4c2a0-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="4c2a0-110">pouvoir</span><span class="sxs-lookup"><span data-stu-id="4c2a0-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="4c2a0-111">refuser</span><span class="sxs-lookup"><span data-stu-id="4c2a0-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="4c2a0-112">do</span><span class="sxs-lookup"><span data-stu-id="4c2a0-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="4c2a0-113">for</span><span class="sxs-lookup"><span data-stu-id="4c2a0-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="4c2a0-114">if</span><span class="sxs-lookup"><span data-stu-id="4c2a0-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="4c2a0-115">switch</span><span class="sxs-lookup"><span data-stu-id="4c2a0-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="4c2a0-116">durant</span><span class="sxs-lookup"><span data-stu-id="4c2a0-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="4c2a0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c2a0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c2a0-118">Syntaxe du langage (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c2a0-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




