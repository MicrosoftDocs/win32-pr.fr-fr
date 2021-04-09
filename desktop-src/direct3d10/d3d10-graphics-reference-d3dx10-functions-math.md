---
description: La bibliothèque mathématique fournie par la bibliothèque de l’utilitaire D3DX fournit des fonctions permettant de calculer les opérations mathématiques 3D.
ms.assetid: 6e180c12-8cbe-4013-8bb4-3ac5bb9c65f1
title: Fonctions mathématiques (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5401299b1aafd5663d8aaefefa4c7fa0da88a89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861546"
---
# <a name="math-functions-direct3d-10-graphics"></a><span data-ttu-id="7384a-103">Fonctions mathématiques (graphiques Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7384a-103">Math Functions (Direct3D 10 Graphics)</span></span>

> [!Note]  
> <span data-ttu-id="7384a-104">Les fonctions mathématiques de la bibliothèque de l’utilitaire D3DX sont déconseillées pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7384a-104">The math functions of the D3DX utility library are deprecated for Windows 8.</span></span> <span data-ttu-id="7384a-105">Nous vous recommandons d’utiliser [DirectXMath](../dxmath/directxmath-portal.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="7384a-105">We recommend that you use [DirectXMath](../dxmath/directxmath-portal.md) instead.</span></span>

 

<span data-ttu-id="7384a-106">La bibliothèque mathématique fournie par la bibliothèque de l’utilitaire D3DX fournit des fonctions permettant de calculer les opérations mathématiques 3D.</span><span class="sxs-lookup"><span data-stu-id="7384a-106">The math library provided by the D3DX utility library supplies functions to compute 3D mathematical operations.</span></span> <span data-ttu-id="7384a-107">Chacune des fonctions peut prendre le même objet que les paramètres transmis \[ \] et retournés \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="7384a-107">Each of the functions can take the same object as the passed \[in\] and returned \[out\] parameters.</span></span> <span data-ttu-id="7384a-108">En outre, les paramètres de sortie sont généralement retournés en tant que valeurs de retour, de sorte que la sortie d’une fonction mathématique peut être utilisée comme paramètre pour une autre fonction mathématique.</span><span class="sxs-lookup"><span data-stu-id="7384a-108">Also, out parameters are typically returned as return values, so that the output of one math function can be used as a parameter for another math function.</span></span>

-   [<span data-ttu-id="7384a-109">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="7384a-109">**D3DXColorAdjustContrast**</span></span>](d3d10-d3dxcoloradjustcontrast.md)
-   [<span data-ttu-id="7384a-110">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="7384a-110">**D3DXColorAdjustSaturation**</span></span>](d3d10-d3dxcoloradjustsaturation.md)
-   [<span data-ttu-id="7384a-111">**D3DXCreateMatrixStack**</span><span class="sxs-lookup"><span data-stu-id="7384a-111">**D3DXCreateMatrixStack**</span></span>](d3d10-d3dxcreatematrixstack.md)
-   [<span data-ttu-id="7384a-112">**D3DXCpuOptimizations**</span><span class="sxs-lookup"><span data-stu-id="7384a-112">**D3DXCpuOptimizations**</span></span>](d3d10-d3dxcpuoptimizations.md)
-   [<span data-ttu-id="7384a-113">**D3DXFloat16To32Array**</span><span class="sxs-lookup"><span data-stu-id="7384a-113">**D3DXFloat16To32Array**</span></span>](d3d10-d3dxfloat16to32array.md)
-   [<span data-ttu-id="7384a-114">**D3DXFloat32To16Array**</span><span class="sxs-lookup"><span data-stu-id="7384a-114">**D3DXFloat32To16Array**</span></span>](d3d10-d3dxfloat32to16array.md)
-   [<span data-ttu-id="7384a-115">**D3DXFresnelTerm**</span><span class="sxs-lookup"><span data-stu-id="7384a-115">**D3DXFresnelTerm**</span></span>](d3d10-d3dxfresnelterm.md)
-   [<span data-ttu-id="7384a-116">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="7384a-116">**D3DXMatrixAffineTransformation**</span></span>](d3d10-d3dxmatrixaffinetransformation.md)
-   [<span data-ttu-id="7384a-117">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="7384a-117">**D3DXMatrixAffineTransformation2D**</span></span>](d3d10-d3dxmatrixaffinetransformation2d.md)
-   [<span data-ttu-id="7384a-118">**D3DXMatrixDecompose**</span><span class="sxs-lookup"><span data-stu-id="7384a-118">**D3DXMatrixDecompose**</span></span>](d3d10-d3dxmatrixdecompose.md)
-   [<span data-ttu-id="7384a-119">**D3DXMatrixDeterminant**</span><span class="sxs-lookup"><span data-stu-id="7384a-119">**D3DXMatrixDeterminant**</span></span>](d3d10-d3dxmatrixdeterminant.md)
-   [<span data-ttu-id="7384a-120">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="7384a-120">**D3DXMatrixInverse**</span></span>](d3d10-d3dxmatrixinverse.md)
-   [<span data-ttu-id="7384a-121">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="7384a-121">**D3DXMatrixLookAtLH**</span></span>](d3d10-d3dxmatrixlookatlh.md)
-   [<span data-ttu-id="7384a-122">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="7384a-122">**D3DXMatrixLookAtRH**</span></span>](d3d10-d3dxmatrixlookatrh.md)
-   [<span data-ttu-id="7384a-123">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="7384a-123">**D3DXMatrixMultiply**</span></span>](d3d10-d3dxmatrixmultiply.md)
-   [<span data-ttu-id="7384a-124">**D3DXMatrixMultiplyTranspose**</span><span class="sxs-lookup"><span data-stu-id="7384a-124">**D3DXMatrixMultiplyTranspose**</span></span>](d3d10-d3dxmatrixmultiplytranspose.md)
-   [<span data-ttu-id="7384a-125">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="7384a-125">**D3DXMatrixOrthoLH**</span></span>](d3d10-d3dxmatrixortholh.md)
-   [<span data-ttu-id="7384a-126">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="7384a-126">**D3DXMatrixOrthoRH**</span></span>](d3d10-d3dxmatrixorthorh.md)
-   [<span data-ttu-id="7384a-127">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="7384a-127">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3d10-d3dxmatrixorthooffcenterlh.md)
-   [<span data-ttu-id="7384a-128">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="7384a-128">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3d10-d3dxmatrixorthooffcenterrh.md)
-   [<span data-ttu-id="7384a-129">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="7384a-129">**D3DXMatrixPerspectiveFovLH**</span></span>](d3d10-d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="7384a-130">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="7384a-130">**D3DXMatrixPerspectiveFovRH**</span></span>](d3d10-d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="7384a-131">**D3DXMatrixReflect**</span><span class="sxs-lookup"><span data-stu-id="7384a-131">**D3DXMatrixReflect**</span></span>](d3d10-d3dxmatrixreflect.md)
-   [<span data-ttu-id="7384a-132">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7384a-132">**D3DXMatrixRotationAxis**</span></span>](d3d10-d3dxmatrixrotationaxis.md)
-   [<span data-ttu-id="7384a-133">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="7384a-133">**D3DXMatrixRotationX**</span></span>](d3d10-d3dxmatrixrotationx.md)
-   [<span data-ttu-id="7384a-134">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="7384a-134">**D3DXMatrixRotationY**</span></span>](d3d10-d3dxmatrixrotationy.md)
-   [<span data-ttu-id="7384a-135">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="7384a-135">**D3DXMatrixRotationZ**</span></span>](d3d10-d3dxmatrixrotationz.md)
-   [<span data-ttu-id="7384a-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7384a-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3d10-d3dxmatrixrotationyawpitchroll.md)
-   [<span data-ttu-id="7384a-137">**D3DXMatrixScaling**</span><span class="sxs-lookup"><span data-stu-id="7384a-137">**D3DXMatrixScaling**</span></span>](d3d10-d3dxmatrixscaling.md)
-   [<span data-ttu-id="7384a-138">**D3DXMatrixShadow**</span><span class="sxs-lookup"><span data-stu-id="7384a-138">**D3DXMatrixShadow**</span></span>](d3d10-d3dxmatrixshadow.md)
-   [<span data-ttu-id="7384a-139">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="7384a-139">**D3DXMatrixTransformation**</span></span>](d3d10-d3dxmatrixtransformation.md)
-   [<span data-ttu-id="7384a-140">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="7384a-140">**D3DXMatrixTransformation2D**</span></span>](d3d10-d3dxmatrixtransformation2d.md)
-   [<span data-ttu-id="7384a-141">**D3DXMatrixTranslation**</span><span class="sxs-lookup"><span data-stu-id="7384a-141">**D3DXMatrixTranslation**</span></span>](d3d10-d3dxmatrixtranslation.md)
-   [<span data-ttu-id="7384a-142">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="7384a-142">**D3DXMatrixTranspose**</span></span>](d3d10-d3dxmatrixtranspose.md)
-   [<span data-ttu-id="7384a-143">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="7384a-143">**D3DXPlaneFromPointNormal**</span></span>](d3d10-d3dxplanefrompointnormal.md)
-   [<span data-ttu-id="7384a-144">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="7384a-144">**D3DXPlaneFromPoints**</span></span>](d3d10-d3dxplanefrompoints.md)
-   [<span data-ttu-id="7384a-145">**D3DXPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="7384a-145">**D3DXPlaneIntersectLine**</span></span>](d3d10-d3dxplaneintersectline.md)
-   [<span data-ttu-id="7384a-146">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="7384a-146">**D3DXPlaneNormalize**</span></span>](d3d10-d3dxplanenormalize.md)
-   [<span data-ttu-id="7384a-147">**D3DXPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="7384a-147">**D3DXPlaneTransform**</span></span>](d3d10-d3dxplanetransform.md)
-   [<span data-ttu-id="7384a-148">**D3DXPlaneTransformArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-148">**D3DXPlaneTransformArray**</span></span>](d3d10-d3dxplanetransformarray.md)
-   [<span data-ttu-id="7384a-149">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7384a-149">**D3DXQuaternionBaryCentric**</span></span>](d3d10-d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="7384a-150">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="7384a-150">**D3DXQuaternionExp**</span></span>](d3d10-d3dxquaternionexp.md)
-   [<span data-ttu-id="7384a-151">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="7384a-151">**D3DXQuaternionInverse**</span></span>](d3d10-d3dxquaternioninverse.md)
-   [<span data-ttu-id="7384a-152">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="7384a-152">**D3DXQuaternionLn**</span></span>](d3d10-d3dxquaternionln.md)
-   [<span data-ttu-id="7384a-153">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="7384a-153">**D3DXQuaternionMultiply**</span></span>](d3d10-d3dxquaternionmultiply.md)
-   [<span data-ttu-id="7384a-154">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="7384a-154">**D3DXQuaternionNormalize**</span></span>](d3d10-d3dxquaternionnormalize.md)
-   [<span data-ttu-id="7384a-155">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7384a-155">**D3DXQuaternionRotationAxis**</span></span>](d3d10-d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="7384a-156">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="7384a-156">**D3DXQuaternionRotationMatrix**</span></span>](d3d10-d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="7384a-157">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7384a-157">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3d10-d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="7384a-158">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="7384a-158">**D3DXQuaternionSlerp**</span></span>](d3d10-d3dxquaternionslerp.md)
-   [<span data-ttu-id="7384a-159">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="7384a-159">**D3DXQuaternionSquad**</span></span>](d3d10-d3dxquaternionsquad.md)
-   [<span data-ttu-id="7384a-160">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="7384a-160">**D3DXQuaternionSquadSetup**</span></span>](d3d10-d3dxquaternionsquadsetup.md)
-   [<span data-ttu-id="7384a-161">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="7384a-161">**D3DXQuaternionToAxisAngle**</span></span>](d3d10-d3dxquaterniontoaxisangle.md)
-   [<span data-ttu-id="7384a-162">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="7384a-162">**D3DXSHEvalConeLight**</span></span>](d3d10-d3dxshevalconelight.md)
-   [<span data-ttu-id="7384a-163">**D3DXSHEvalDirection**</span><span class="sxs-lookup"><span data-stu-id="7384a-163">**D3DXSHEvalDirection**</span></span>](d3d10-d3dxshevaldirection.md)
-   [<span data-ttu-id="7384a-164">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="7384a-164">**D3DXSHEvalDirectionalLight**</span></span>](d3d10-d3dxshevaldirectionallight.md)
-   [<span data-ttu-id="7384a-165">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="7384a-165">**D3DXSHEvalHemisphereLight**</span></span>](d3d10-d3dxshevalhemispherelight.md)
-   [<span data-ttu-id="7384a-166">**D3DXSHMultiply2**</span><span class="sxs-lookup"><span data-stu-id="7384a-166">**D3DXSHMultiply2**</span></span>](d3d10-d3dxshmultiply2.md)
-   [<span data-ttu-id="7384a-167">**D3DXSHMultiply3**</span><span class="sxs-lookup"><span data-stu-id="7384a-167">**D3DXSHMultiply3**</span></span>](d3d10-d3dxshmultiply3.md)
-   [<span data-ttu-id="7384a-168">**D3DXSHMultiply4**</span><span class="sxs-lookup"><span data-stu-id="7384a-168">**D3DXSHMultiply4**</span></span>](d3d10-d3dxshmultiply4.md)
-   [<span data-ttu-id="7384a-169">**D3DXSHMultiply5**</span><span class="sxs-lookup"><span data-stu-id="7384a-169">**D3DXSHMultiply5**</span></span>](d3d10-d3dxshmultiply5.md)
-   [<span data-ttu-id="7384a-170">**D3DXSHMultiply6**</span><span class="sxs-lookup"><span data-stu-id="7384a-170">**D3DXSHMultiply6**</span></span>](d3d10-d3dxshmultiply6.md)
-   [<span data-ttu-id="7384a-171">**D3DX10SHProjectCubeMap**</span><span class="sxs-lookup"><span data-stu-id="7384a-171">**D3DX10SHProjectCubeMap**</span></span>](d3dx10shprojectcubemap.md)
-   [<span data-ttu-id="7384a-172">**D3DXSHRotate**</span><span class="sxs-lookup"><span data-stu-id="7384a-172">**D3DXSHRotate**</span></span>](d3d10-d3dxshrotate.md)
-   [<span data-ttu-id="7384a-173">**D3DXSHRotateZ**</span><span class="sxs-lookup"><span data-stu-id="7384a-173">**D3DXSHRotateZ**</span></span>](d3d10-d3dxshrotatez.md)
-   [<span data-ttu-id="7384a-174">**D3DXSHScale**</span><span class="sxs-lookup"><span data-stu-id="7384a-174">**D3DXSHScale**</span></span>](d3d10-d3dxshscale.md)
-   [<span data-ttu-id="7384a-175">**D3DXVec2BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7384a-175">**D3DXVec2BaryCentric**</span></span>](d3d10-d3dxvec2barycentric.md)
-   [<span data-ttu-id="7384a-176">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="7384a-176">**D3DXVec2CatmullRom**</span></span>](d3d10-d3dxvec2catmullrom.md)
-   [<span data-ttu-id="7384a-177">**D3DXVec2Hermite**</span><span class="sxs-lookup"><span data-stu-id="7384a-177">**D3DXVec2Hermite**</span></span>](d3d10-d3dxvec2hermite.md)
-   [<span data-ttu-id="7384a-178">**D3DXVec2Normalize**</span><span class="sxs-lookup"><span data-stu-id="7384a-178">**D3DXVec2Normalize**</span></span>](d3d10-d3dxvec2normalize.md)
-   [<span data-ttu-id="7384a-179">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="7384a-179">**D3DXVec2Transform**</span></span>](d3d10-d3dxvec2transform.md)
-   [<span data-ttu-id="7384a-180">**D3DXVec2TransformArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-180">**D3DXVec2TransformArray**</span></span>](d3d10-d3dxvec2transformarray.md)
-   [<span data-ttu-id="7384a-181">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="7384a-181">**D3DXVec2TransformCoord**</span></span>](d3d10-d3dxvec2transformcoord.md)
-   [<span data-ttu-id="7384a-182">**D3DXVec2TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-182">**D3DXVec2TransformCoordArray**</span></span>](d3d10-d3dxvec2transformcoordarray.md)
-   [<span data-ttu-id="7384a-183">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="7384a-183">**D3DXVec2TransformNormal**</span></span>](d3d10-d3dxvec2transformnormal.md)
-   [<span data-ttu-id="7384a-184">**D3DXVec2TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-184">**D3DXVec2TransformNormalArray**</span></span>](d3d10-d3dxvec2transformnormalarray.md)
-   [<span data-ttu-id="7384a-185">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7384a-185">**D3DXVec3BaryCentric**</span></span>](d3d10-d3dxvec3barycentric.md)
-   [<span data-ttu-id="7384a-186">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="7384a-186">**D3DXVec3CatmullRom**</span></span>](d3d10-d3dxvec3catmullrom.md)
-   [<span data-ttu-id="7384a-187">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="7384a-187">**D3DXVec3Hermite**</span></span>](d3d10-d3dxvec3hermite.md)
-   [<span data-ttu-id="7384a-188">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="7384a-188">**D3DXVec3Normalize**</span></span>](d3d10-d3dxvec3normalize.md)
-   [<span data-ttu-id="7384a-189">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="7384a-189">**D3DXVec3Project**</span></span>](d3d10-d3dxvec3project.md)
-   [<span data-ttu-id="7384a-190">**D3DXVec3ProjectArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-190">**D3DXVec3ProjectArray**</span></span>](d3d10-d3dxvec3projectarray.md)
-   [<span data-ttu-id="7384a-191">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="7384a-191">**D3DXVec3Transform**</span></span>](d3d10-d3dxvec3transform.md)
-   [<span data-ttu-id="7384a-192">**D3DXVec3TransformArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-192">**D3DXVec3TransformArray**</span></span>](d3d10-d3dxvec3transformarray.md)
-   [<span data-ttu-id="7384a-193">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="7384a-193">**D3DXVec3TransformCoord**</span></span>](d3d10-d3dxvec3transformcoord.md)
-   [<span data-ttu-id="7384a-194">**D3DXVec3TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-194">**D3DXVec3TransformCoordArray**</span></span>](d3d10-d3dxvec3transformcoordarray.md)
-   [<span data-ttu-id="7384a-195">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="7384a-195">**D3DXVec3TransformNormal**</span></span>](d3d10-d3dxvec3transformnormal.md)
-   [<span data-ttu-id="7384a-196">**D3DXVec3TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-196">**D3DXVec3TransformNormalArray**</span></span>](d3d10-d3dxvec3transformnormalarray.md)
-   [<span data-ttu-id="7384a-197">**D3DXVec4BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="7384a-197">**D3DXVec4BaryCentric**</span></span>](d3d10-d3dxvec4barycentric.md)
-   [<span data-ttu-id="7384a-198">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="7384a-198">**D3DXVec4CatmullRom**</span></span>](d3d10-d3dxvec4catmullrom.md)
-   [<span data-ttu-id="7384a-199">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="7384a-199">**D3DXVec4Cross**</span></span>](d3d10-d3dxvec4cross.md)
-   [<span data-ttu-id="7384a-200">**D3DXVec4Hermite**</span><span class="sxs-lookup"><span data-stu-id="7384a-200">**D3DXVec4Hermite**</span></span>](d3d10-d3dxvec4hermite.md)
-   [<span data-ttu-id="7384a-201">**D3DXVec4Normalize**</span><span class="sxs-lookup"><span data-stu-id="7384a-201">**D3DXVec4Normalize**</span></span>](d3d10-d3dxvec4normalize.md)
-   [<span data-ttu-id="7384a-202">**D3DXVec4Transform**</span><span class="sxs-lookup"><span data-stu-id="7384a-202">**D3DXVec4Transform**</span></span>](d3d10-d3dxvec4transform.md)
-   [<span data-ttu-id="7384a-203">**D3DXVec4TransformArray**</span><span class="sxs-lookup"><span data-stu-id="7384a-203">**D3DXVec4TransformArray**</span></span>](d3d10-d3dxvec4transformarray.md)

## <a name="resolving-link-errors-with-d3dx-math-functions"></a><span data-ttu-id="7384a-204">Résolution des erreurs de lien avec les fonctions mathématiques D3DX</span><span class="sxs-lookup"><span data-stu-id="7384a-204">Resolving Link Errors with D3DX Math Functions</span></span>

<span data-ttu-id="7384a-205">Les fonctions mathématiques D3DX sont implémentées de manière identique dans D3DX10 (D3DX10math. h) et D3DX9 (D3DX9math. h).</span><span class="sxs-lookup"><span data-stu-id="7384a-205">The D3DX math functions are implemented identically in D3DX10 (D3DX10math.h) and D3DX9 (D3DX9math.h).</span></span> <span data-ttu-id="7384a-206">Cela peut provoquer des erreurs de liaison si un projet implémente à la fois le code DirectX 9 et DirectX 10, et tente de lier une fonction d’un en-tête à la bibliothèque opposée.</span><span class="sxs-lookup"><span data-stu-id="7384a-206">This can cause link errors if a project implements both DirectX 9 and DirectX 10 code, and attempts to link a function from one header with the opposite library.</span></span>

<span data-ttu-id="7384a-207">Pour éliminer le problème d’inclusion des deux en-têtes, D3DX10math. h inclut les éléments suivants \# :</span><span class="sxs-lookup"><span data-stu-id="7384a-207">To eliminate the problem of including both headers, D3DX10math.h includes the following \#define:</span></span>


```
#ifndef __D3DX9MATH_H__
#define __D3DX9MATH_H__
```



<span data-ttu-id="7384a-208">Pour éliminer les erreurs de liaison possibles, les exemples du kit de développement logiciel (SDK) DX sont d’abord liés aux bibliothèques D3DX9 (D3DX9d. lib et D3DX9. lib), puis aux bibliothèques D3DX10 (D3DX10d. lib et D3DX10. lib).</span><span class="sxs-lookup"><span data-stu-id="7384a-208">To eliminate possible link errors, the DX SDK samples link to D3DX9 libraries first (D3DX9d.lib and D3DX9.lib) and then the D3DX10 libraries second (D3DX10d.lib and D3DX10.lib).</span></span> <span data-ttu-id="7384a-209">Ces paramètres sont sous projet/propriétés si vous utilisez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7384a-209">These settings are under Project/Properties if you are using Visual Studio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7384a-210">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7384a-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7384a-211">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="7384a-211">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
