---
description: Les effets de brouillard peuvent offrir une scène 3D plus réaliste.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: État de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385496"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="d7011-103">État de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d7011-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="d7011-104">Les effets de brouillard peuvent offrir une scène 3D plus réaliste.</span><span class="sxs-lookup"><span data-stu-id="d7011-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="d7011-105">Vous pouvez utiliser des effets de brouillard pour plus de simulation du brouillard.</span><span class="sxs-lookup"><span data-stu-id="d7011-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="d7011-106">Ils peuvent également réduire la clarté d’une scène avec une distance.</span><span class="sxs-lookup"><span data-stu-id="d7011-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="d7011-107">Cela reflète ce qui se passe dans le monde réel. comme les objets deviennent plus éloignés de l’utilisateur, leurs détails sont moins distincts.</span><span class="sxs-lookup"><span data-stu-id="d7011-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="d7011-108">Pour plus d’informations sur l’utilisation du brouillard dans votre application, consultez [brouillard (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="d7011-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="d7011-109">Une application C++ contrôle le brouillard via les États de rendu de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d7011-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="d7011-110">Le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) comprend des États pour contrôler si le brouillard de pixel (table) ou de vertex est utilisé, la couleur qu’il est, la formule de brouillard appliquée par le système et les paramètres de la formule.</span><span class="sxs-lookup"><span data-stu-id="d7011-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="d7011-111">Vous activez le brouillard en affectant \_ à l’état de rendu D3DRS FOGENABLE la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d7011-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="d7011-112">La couleur de brouillard peut être définie sur n’importe quelle valeur de couleur à l’aide de l' \_ État de rendu D3DRS FOGCOLOR ; le composant alpha de la couleur de brouillard est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d7011-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="d7011-113">Les \_ États de rendu D3DRS FOGTABLEMODE et D3DRS \_ FOGVERTEXMODE contrôlent la formule de brouillard appliquée pour les calculs de brouillard et ils contrôlent indirectement le type de brouillard appliqué.</span><span class="sxs-lookup"><span data-stu-id="d7011-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="d7011-114">Les deux États de rendu peuvent être définis sur un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="d7011-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="d7011-115">La définition de l’état de rendu sur D3DFOG \_ None désactive le brouillard de pixel ou vertex, respectivement.</span><span class="sxs-lookup"><span data-stu-id="d7011-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="d7011-116">Si les deux États de rendu sont définis sur des modes valides, le système applique uniquement les effets de brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="d7011-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="d7011-117">Les \_ États de rendu D3DRS FOGSTART et D3DRS \_ FOGEND contrôlent les paramètres de formule de brouillard pour le \_ mode D3DFOG Linear.</span><span class="sxs-lookup"><span data-stu-id="d7011-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="d7011-118">L' \_ État de rendu D3DRS FOGDENSITY contrôle la densité de brouillard dans les modes de brouillard exponentiels.</span><span class="sxs-lookup"><span data-stu-id="d7011-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="d7011-119">Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d7011-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7011-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7011-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7011-121">États de rendu</span><span class="sxs-lookup"><span data-stu-id="d7011-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
