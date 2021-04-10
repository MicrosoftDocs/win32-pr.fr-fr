---
description: L’API Direct3D définit plusieurs éléments d’API pour vous aider à créer et à gérer le système d’effet.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Référence des effets (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950598"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="75f64-103">Référence des effets (graphiques Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="75f64-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="75f64-104">L’API Direct3D définit plusieurs éléments d’API pour vous aider à créer et à gérer le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="75f64-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="75f64-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="75f64-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="75f64-106">Fonctions</span><span class="sxs-lookup"><span data-stu-id="75f64-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="75f64-107">Structures</span><span class="sxs-lookup"><span data-stu-id="75f64-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="75f64-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="75f64-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="75f64-109">Le système d’effet encapsule les assignations d’État dans un effet.</span><span class="sxs-lookup"><span data-stu-id="75f64-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="75f64-110">Chaque effet est une collection d’États de pipeline qui peut être décomposée en affectations d’État à l’aide de blocs d’État, de ressources et de nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="75f64-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="75f64-111">Selon la taille d’un effet, vous pouvez choisir d’en implémenter un dans une chaîne de texte ASCII ou un fichier d’effet (. FX).</span><span class="sxs-lookup"><span data-stu-id="75f64-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="75f64-112">Pour organiser les informations dans un effet, consultez le format de l' [effet](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="75f64-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="75f64-113">Après avoir conçu un effet, utilisez l’API Effect pour définir l’état de l’appareil pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="75f64-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="75f64-114">En outre, le système d’effet prend en charge une série d’API de réflexion pour l’obtention et la définition des données d’effet.</span><span class="sxs-lookup"><span data-stu-id="75f64-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="75f64-115">Pour plus d’informations, consultez [effets système interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="75f64-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75f64-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75f64-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f64-117">Référence Direct3D</span><span class="sxs-lookup"><span data-stu-id="75f64-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



