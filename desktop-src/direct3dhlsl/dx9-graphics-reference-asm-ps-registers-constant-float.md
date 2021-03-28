---
title: Registre à virgule flottante constante (référence PS HLSL)
description: Registre d’entrée de nuanceur de pixels pour une constante à virgule flottante 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382392"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="695bc-103">Registre à virgule flottante constante (référence PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="695bc-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="695bc-104">Registre d’entrée de nuanceur de pixels pour une constante à virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="695bc-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="695bc-105">Ils peuvent être définis à l’aide [de def-PS](def---ps.md) ou [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="695bc-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="695bc-106">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="695bc-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="695bc-107">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="695bc-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="695bc-108">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="695bc-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="695bc-109">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="695bc-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="695bc-110">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="695bc-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="695bc-111">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="695bc-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="695bc-112">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="695bc-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="695bc-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="695bc-113">Examples</span></span>

<span data-ttu-id="695bc-114">Voici un exemple de déclaration de deux constantes à virgule flottante dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="695bc-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="695bc-115">Ces constantes sont chargées chaque fois que [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) est appelé.</span><span class="sxs-lookup"><span data-stu-id="695bc-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="695bc-116">Si vous définissez des valeurs constantes avec l’API, aucune déclaration de nuanceur n’est requise.</span><span class="sxs-lookup"><span data-stu-id="695bc-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="695bc-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="695bc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695bc-118">Inscrit</span><span class="sxs-lookup"><span data-stu-id="695bc-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 