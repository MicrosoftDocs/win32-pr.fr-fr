---
title: Registre d’entiers constant (référence PS HLSL)
description: Les registres d’entiers constants sont utilisés uniquement par Loop-PS et REP-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971750"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="cd74e-103">Registre d’entiers constant (référence PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd74e-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="cd74e-104">Les registres d’entiers constants sont utilisés uniquement par [Loop-PS](loop---ps.md) et [REP-PS](rep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="cd74e-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="cd74e-105">Ils peuvent être définis à l’aide de la définition [-PS](defi---ps.md) ou [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="cd74e-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="cd74e-106">En cas d’utilisation comme argument de l’instruction [Loop-PS](loop---ps.md) :</span><span class="sxs-lookup"><span data-stu-id="cd74e-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="cd74e-107">. x est le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="cd74e-107">.x is the iteration count.</span></span> <span data-ttu-id="cd74e-108">([REP-PS](rep---ps.md) utilise uniquement ce composant).</span><span class="sxs-lookup"><span data-stu-id="cd74e-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="cd74e-109">. y est la valeur initiale du compteur de boucle.</span><span class="sxs-lookup"><span data-stu-id="cd74e-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="cd74e-110">. z est l’étape d’incrément du compteur de boucles.</span><span class="sxs-lookup"><span data-stu-id="cd74e-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="cd74e-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="cd74e-111">Pixel shader versions</span></span>     | <span data-ttu-id="cd74e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd74e-112">1\_1</span></span> | <span data-ttu-id="cd74e-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="cd74e-113">1\_2</span></span> | <span data-ttu-id="cd74e-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cd74e-114">1\_3</span></span> | <span data-ttu-id="cd74e-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="cd74e-115">1\_4</span></span> | <span data-ttu-id="cd74e-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd74e-116">2\_0</span></span> | <span data-ttu-id="cd74e-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd74e-117">2\_sw</span></span> | <span data-ttu-id="cd74e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd74e-118">2\_x</span></span> | <span data-ttu-id="cd74e-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd74e-119">3\_0</span></span> | <span data-ttu-id="cd74e-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd74e-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="cd74e-121">Registre d’entiers constant</span><span class="sxs-lookup"><span data-stu-id="cd74e-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="cd74e-122">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-122">x</span></span>    | <span data-ttu-id="cd74e-123">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-123">x</span></span>    | <span data-ttu-id="cd74e-124">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-124">x</span></span>     |



 

<span data-ttu-id="cd74e-125">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cd74e-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="cd74e-126">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="cd74e-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="cd74e-127">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="cd74e-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="cd74e-128">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="cd74e-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="cd74e-129">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="cd74e-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="cd74e-130">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="cd74e-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="cd74e-131">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="cd74e-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd74e-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd74e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd74e-133">Inscrit</span><span class="sxs-lookup"><span data-stu-id="cd74e-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 