---
title: Registre à virgule flottante constante (référence HLSL VS)
description: Registre d’entrée du nuanceur de sommets pour une constante à virgule flottante à quatre composants. Définissez un registre de constante avec Def-vs ou SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382105"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="259df-104">Registre à virgule flottante constante (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="259df-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="259df-105">Registre d’entrée du nuanceur de sommets pour une constante à virgule flottante à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="259df-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="259df-106">Définissez un registre de constante avec [def-vs](def---vs.md) ou [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="259df-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="259df-107">Le fichier de registre de constante est en lecture seule du point de vue du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="259df-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="259df-108">Toute instruction unique ne peut accéder qu’à un seul registre de constantes.</span><span class="sxs-lookup"><span data-stu-id="259df-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="259df-109">Toutefois, chaque source de cette instruction peut Swizzle et inverser ce vecteur au fur et à mesure de sa lecture.</span><span class="sxs-lookup"><span data-stu-id="259df-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="259df-110">Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="259df-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="259df-111">Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="259df-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="259df-112">La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement.</span><span class="sxs-lookup"><span data-stu-id="259df-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="259df-113">À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global.</span><span class="sxs-lookup"><span data-stu-id="259df-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="259df-114">Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="259df-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="259df-115">Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="259df-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="259df-116">Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.</span><span class="sxs-lookup"><span data-stu-id="259df-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="259df-117">Un registre de constante est désigné comme étant absolu ou relatif :</span><span class="sxs-lookup"><span data-stu-id="259df-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="259df-118">Le registre de constante peut être lu, par conséquent, soit à l’aide d’un index absolu, soit à l’aide d’un index relatif à partir d’un registre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="259df-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="259df-119">Les lectures à partir des registres hors limites sont retournées (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="259df-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="259df-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="259df-120">Examples</span></span>

<span data-ttu-id="259df-121">Voici un exemple de déclaration de deux constantes à virgule flottante dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="259df-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="259df-122">Ces constantes sont chargées chaque fois que [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) est appelé.</span><span class="sxs-lookup"><span data-stu-id="259df-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="259df-123">Voici un exemple d’utilisation de l’API.</span><span class="sxs-lookup"><span data-stu-id="259df-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="259df-124">Si vous définissez des valeurs constantes avec l’API, aucune déclaration de nuanceur n’est requise.</span><span class="sxs-lookup"><span data-stu-id="259df-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="259df-125">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="259df-125">Vertex shader versions</span></span> | <span data-ttu-id="259df-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="259df-126">1\_1</span></span> | <span data-ttu-id="259df-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="259df-127">2\_0</span></span> | <span data-ttu-id="259df-128">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="259df-128">2\_sw</span></span> | <span data-ttu-id="259df-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="259df-129">2\_x</span></span> | <span data-ttu-id="259df-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="259df-130">3\_0</span></span> | <span data-ttu-id="259df-131">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="259df-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="259df-132">Registre de constante</span><span class="sxs-lookup"><span data-stu-id="259df-132">Constant Register</span></span>      | <span data-ttu-id="259df-133">x</span><span class="sxs-lookup"><span data-stu-id="259df-133">x</span></span>    | <span data-ttu-id="259df-134">x</span><span class="sxs-lookup"><span data-stu-id="259df-134">x</span></span>    | <span data-ttu-id="259df-135">x</span><span class="sxs-lookup"><span data-stu-id="259df-135">x</span></span>     | <span data-ttu-id="259df-136">x</span><span class="sxs-lookup"><span data-stu-id="259df-136">x</span></span>    | <span data-ttu-id="259df-137">x</span><span class="sxs-lookup"><span data-stu-id="259df-137">x</span></span>    | <span data-ttu-id="259df-138">x</span><span class="sxs-lookup"><span data-stu-id="259df-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="259df-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="259df-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="259df-140">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="259df-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 