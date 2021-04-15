---
title: Comment concevoir un nuanceur de coque
description: Cette rubrique montre comment concevoir un nuanceur de coque.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990912"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="138c8-103">Comment : concevoir un nuanceur de coque</span><span class="sxs-lookup"><span data-stu-id="138c8-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="138c8-104">Un nuanceur de coque est la première des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md) (les deux autres étapes sont du paveur et un nuanceur de domaine).</span><span class="sxs-lookup"><span data-stu-id="138c8-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="138c8-105">Cette rubrique montre comment concevoir un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="138c8-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="138c8-106">Un nuanceur de coque requiert deux fonctions, le nuanceur de coque principal et une fonction de constante de patch.</span><span class="sxs-lookup"><span data-stu-id="138c8-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="138c8-107">Le nuanceur de coque implémente des calculs sur chaque point de contrôle ; le nuanceur de coque appelle également la fonction de constante de patch qui implémente les calculs sur chaque correctif.</span><span class="sxs-lookup"><span data-stu-id="138c8-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="138c8-108">Une fois que vous avez conçu un nuanceur de coque, consultez [Comment : créer un nuanceur](direct3d-11-advanced-stages-hull-shader-create.md) de coque pour apprendre à créer un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="138c8-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="138c8-109">**Pour concevoir un nuanceur de coque**</span><span class="sxs-lookup"><span data-stu-id="138c8-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="138c8-110">Définir le contrôle d’entrée du nuanceur de coque et les points de contrôle de sortie.</span><span class="sxs-lookup"><span data-stu-id="138c8-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="138c8-111">Définir des données de constante de correctif de sortie.</span><span class="sxs-lookup"><span data-stu-id="138c8-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="138c8-112">Dans le cas d’un domaine à quatre cœurs, [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) définit 4 facteurs de pavage Edge (pour paver les bords), puisque la fonction fixe du paveur a besoin de connaître la quantité à paver.</span><span class="sxs-lookup"><span data-stu-id="138c8-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="138c8-113">Les sorties requises sont différentes pour les domaines triangle et isoligne.</span><span class="sxs-lookup"><span data-stu-id="138c8-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="138c8-114">La fonction Fixed du paveur n’examine pas les autres sorties de nuanceur de coque, telles que d’autres données de constante de correctif ou l’un des points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="138c8-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="138c8-115">Le nuanceur de domaine, qui est appelé pour chaque point, la fonction fixe du paveur génère, en tant qu’entrée, tous les points de contrôle de sortie du nuanceur de coque et toutes les données de constante de correctif de sortie. le nuanceur évalue le correctif à son emplacement.</span><span class="sxs-lookup"><span data-stu-id="138c8-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="138c8-116">Définissez une fonction de constante de patch.</span><span class="sxs-lookup"><span data-stu-id="138c8-116">Define a patch constant function.</span></span> <span data-ttu-id="138c8-117">Une fonction de constante de patch s’exécute une fois pour chaque correctif pour calculer toutes les données qui sont constantes pour le correctif entier (par opposition aux données de point de contrôle, qui sont calculées dans le nuanceur de coque).</span><span class="sxs-lookup"><span data-stu-id="138c8-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="138c8-118">Les propriétés de la fonction patch constant sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="138c8-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="138c8-119">Une entrée spécifie une variable contenant un ID de correctif et est identifiée par la valeur système **SV \_ PrimitiveID** (voir [sémantiques](../direct3dhlsl/dx-graphics-hlsl-semantics.md) dans le nuancier modèle 4).</span><span class="sxs-lookup"><span data-stu-id="138c8-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="138c8-120">Un paramètre d’entrée correspond aux points de contrôle d’entrée, déclarés dans la **\_ sortie du \_ point \_ de contrôle vs** dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="138c8-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="138c8-121">Une fonction patch peut voir tous les points de contrôle d’entrée pour chaque correctif, il y a 32 points de contrôle par correctif dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="138c8-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="138c8-122">Au minimum, la fonction doit calculer les facteurs de pavage par correctif pour l’étape du paveur qui sont identifiés avec [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span><span class="sxs-lookup"><span data-stu-id="138c8-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="138c8-123">Un domaine quadruple nécessite quatre facteurs de pavage pour les bords et deux facteurs supplémentaires (identifiés par [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) pour le pavage dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="138c8-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="138c8-124">La fonction Fixed du paveur n’examine pas les autres sorties de nuanceur de coque (telles que les données de constante de correctif ou l’un des points de contrôle).</span><span class="sxs-lookup"><span data-stu-id="138c8-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="138c8-125">Les sorties sont généralement définies par une structure et sont identifiées par la sortie de données de la **\_ constante \_ \_ HS** dans cet exemple ; la structure dépend du type de domaine et serait différente pour les domaines de triangle ou d’isoligne.</span><span class="sxs-lookup"><span data-stu-id="138c8-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="138c8-126">Un nuanceur de domaine en revanche est appelé pour chaque point que la fonction fixe du paveur génère et doit afficher les points de contrôle de sortie et les données de constante de correctif de sortie (à la fois à partir du nuanceur de coque) pour évaluer un correctif à son emplacement.</span><span class="sxs-lookup"><span data-stu-id="138c8-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="138c8-127">Définissez un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="138c8-127">Define a hull shader.</span></span> <span data-ttu-id="138c8-128">Un nuanceur de coque identifie les propriétés d’un correctif, y compris une fonction de constante de patch.</span><span class="sxs-lookup"><span data-stu-id="138c8-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="138c8-129">Un nuanceur de coque est appelé une fois pour chaque point de contrôle de sortie.</span><span class="sxs-lookup"><span data-stu-id="138c8-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="138c8-130">Un nuanceur de coque utilise les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="138c8-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="138c8-131">Attribut de [domaine](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .</span><span class="sxs-lookup"><span data-stu-id="138c8-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="138c8-132">Attribut de [partitionnement](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .</span><span class="sxs-lookup"><span data-stu-id="138c8-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="138c8-133">Attribut [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .</span><span class="sxs-lookup"><span data-stu-id="138c8-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="138c8-134">Attribut [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .</span><span class="sxs-lookup"><span data-stu-id="138c8-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="138c8-135">Attribut [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) .</span><span class="sxs-lookup"><span data-stu-id="138c8-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="138c8-136">Un nuanceur de coque calcule les points de contrôle de sortie. il y a 16 points de contrôle Bézier de sortie dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="138c8-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="138c8-137">Tous les points de contrôle d’entrée (identifiés par la **\_ sortie du \_ point \_ de contrôle vs**) sont visibles pour chaque appel de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="138c8-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="138c8-138">Dans cet exemple, il y a 32 points de contrôle d’entrée.</span><span class="sxs-lookup"><span data-stu-id="138c8-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="138c8-139">Un nuanceur de coque est appelé une fois par point de contrôle de sortie (identifié avec [SV \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) pour chaque correctif (identifié avec SV \_ PrimitiveID).</span><span class="sxs-lookup"><span data-stu-id="138c8-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="138c8-140">L’objectif de ce nuanceur particulier est de calculer la sortie *i*, qui a été définie pour être un point de contrôle Bézier (cet exemple comporte 16 points de contrôle de sortie définis par outputcontrolpoints).</span><span class="sxs-lookup"><span data-stu-id="138c8-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="138c8-141">Un nuanceur de coque exécute une routine une fois par correctif (fonction de constante de patch) pour calculer des données de constantes de correctifs (facteurs de pavage au minimum).</span><span class="sxs-lookup"><span data-stu-id="138c8-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="138c8-142">Séparément, un nuanceur de coque exécute une fonction de constante de patch (appelée SubDToBezierConstantsHS) sur chaque correctif pour calculer des données constantes de correctif, telles que les facteurs de pavage pour l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="138c8-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="138c8-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="138c8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="138c8-144">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="138c8-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="138c8-145">Vue d’ensemble de la polygonalisation</span><span class="sxs-lookup"><span data-stu-id="138c8-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 