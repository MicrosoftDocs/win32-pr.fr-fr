---
title: Registre booléen constant (référence HLSL VS)
description: Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, si bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971747"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="e1d38-103">Registre booléen constant (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="e1d38-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="e1d38-104">Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, [si bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="e1d38-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="e1d38-105">Il y en a 16, donc un nuanceur peut avoir 16 conditions de branche indépendantes.</span><span class="sxs-lookup"><span data-stu-id="e1d38-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="e1d38-106">Ils peuvent être définis à l’aide [de defb-vs](defb---vs.md) ou [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="e1d38-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="e1d38-107">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e1d38-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="e1d38-108">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e1d38-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="e1d38-109">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1d38-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="e1d38-110">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="e1d38-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="e1d38-111">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="e1d38-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="e1d38-112">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e1d38-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="e1d38-113">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="e1d38-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1d38-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1d38-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1d38-115">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e1d38-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 