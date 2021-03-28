---
title: Registre booléen constant (référence PS HLSL)
description: Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, si bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729149"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="591c5-103">Registre booléen constant (référence PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="591c5-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="591c5-104">Ce registre est une collection de bits utilisés dans les instructions de contrôle de Flow statique (par exemple, [si bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="591c5-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="591c5-105">Il y en a 16, donc un nuanceur peut avoir 16 conditions de branche indépendantes.</span><span class="sxs-lookup"><span data-stu-id="591c5-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="591c5-106">Ils peuvent être définis à l’aide [de defb-PS](defb---ps.md) ou [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="591c5-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="591c5-107">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="591c5-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="591c5-108">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="591c5-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="591c5-109">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="591c5-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="591c5-110">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="591c5-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="591c5-111">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="591c5-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="591c5-112">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="591c5-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="591c5-113">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="591c5-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="591c5-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="591c5-114">Pixel shader versions</span></span>     | <span data-ttu-id="591c5-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="591c5-115">1\_1</span></span> | <span data-ttu-id="591c5-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="591c5-116">1\_2</span></span> | <span data-ttu-id="591c5-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="591c5-117">1\_3</span></span> | <span data-ttu-id="591c5-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="591c5-118">1\_4</span></span> | <span data-ttu-id="591c5-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="591c5-119">2\_0</span></span> | <span data-ttu-id="591c5-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="591c5-120">2\_sw</span></span> | <span data-ttu-id="591c5-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="591c5-121">2\_x</span></span> | <span data-ttu-id="591c5-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="591c5-122">3\_0</span></span> | <span data-ttu-id="591c5-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="591c5-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="591c5-124">Registre booléen constant</span><span class="sxs-lookup"><span data-stu-id="591c5-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="591c5-125">x</span><span class="sxs-lookup"><span data-stu-id="591c5-125">x</span></span>    | <span data-ttu-id="591c5-126">x</span><span class="sxs-lookup"><span data-stu-id="591c5-126">x</span></span>    | <span data-ttu-id="591c5-127">x</span><span class="sxs-lookup"><span data-stu-id="591c5-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="591c5-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="591c5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="591c5-129">Inscrit</span><span class="sxs-lookup"><span data-stu-id="591c5-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 