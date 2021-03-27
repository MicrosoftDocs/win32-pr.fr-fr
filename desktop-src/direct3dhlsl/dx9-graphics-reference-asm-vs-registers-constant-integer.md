---
title: Registre d’entiers constants (référence HLSL VS)
description: Les registres d’entiers constants sont utilisés uniquement par Loop-vs et REP-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971759"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="bf3f9-103">Registre d’entiers constants (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="bf3f9-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="bf3f9-104">Les registres d’entiers constants sont utilisés uniquement par [Loop-vs](loop---vs.md) et [REP-vs](rep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f9-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="bf3f9-105">Ils peuvent être définis à l’aide de la définition [-vs](defi---vs.md) ou [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="bf3f9-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="bf3f9-106">En cas d’utilisation comme argument de l’instruction [Loop-vs](loop---vs.md) :</span><span class="sxs-lookup"><span data-stu-id="bf3f9-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="bf3f9-107">. x est le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-107">.x is the iteration count.</span></span> <span data-ttu-id="bf3f9-108">([REP-vs](rep---vs.md) utilise uniquement ce composant).</span><span class="sxs-lookup"><span data-stu-id="bf3f9-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="bf3f9-109">. y est la valeur initiale du compteur de boucle.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="bf3f9-110">. z est l’étape d’incrément du compteur de boucles.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="bf3f9-111">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="bf3f9-112">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="bf3f9-113">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="bf3f9-114">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="bf3f9-115">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="bf3f9-116">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="bf3f9-117">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="bf3f9-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf3f9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf3f9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf3f9-119">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="bf3f9-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 