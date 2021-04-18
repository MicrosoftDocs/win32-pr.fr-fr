---
description: Définit des points de contrôle pour l’interpolation sphérique Quadrangle.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: D3DXQuaternionSquadSetup, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523220"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="6cdaa-103">D3DXQuaternionSquadSetup, fonction (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6cdaa-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="6cdaa-104">Définit des points de contrôle pour l’interpolation sphérique Quadrangle.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdaa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cdaa-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="6cdaa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cdaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cdaa-107">*pAOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-108">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-109">Pointeur vers sur.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-110">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-111">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-112">Pointeur vers à propos de.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-113">*pCOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-114">Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-115">Pointeur vers COut.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-116">*pQ0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-117">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-118">Pointeur vers le point de contrôle d’entrée, Q0.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-119">*pQ1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-120">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-121">Pointeur vers le point de contrôle d’entrée, Q1.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-122">*pQ2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-123">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-124">Pointeur vers le point de contrôle d’entrée, Q2.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="6cdaa-125">*pQ3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cdaa-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdaa-126">Type : **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6cdaa-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6cdaa-127">Pointeur vers le point de contrôle d’entrée, Q3.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cdaa-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cdaa-128">Return value</span></span>

<span data-ttu-id="6cdaa-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cdaa-130">Notes</span><span class="sxs-lookup"><span data-stu-id="6cdaa-130">Remarks</span></span>

<span data-ttu-id="6cdaa-131">Cette fonction prend quatre points de contrôle, qui sont fournis aux entrées pQ0, pQ1, pQ2 et pQ3.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="6cdaa-132">La fonction modifie ensuite ces valeurs pour trouver une courbe qui circule le long du chemin le plus rapide.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="6cdaa-133">Les valeurs de q0, Q2 et Q3 sont calculées comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="6cdaa-134">Une fois les nouvelles valeurs Q calculées, les valeurs pour sur, à propos de et COut sont calculées comme suit :</span><span class="sxs-lookup"><span data-stu-id="6cdaa-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="6cdaa-135">Sur = T1 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q1) \* T2 \] \ + \ ln \[ exp (Q1) \* Q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="6cdaa-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="6cdaa-136">À propos de = Q2 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (2e trimestre) \* Q3 \] \ + \ ln \[ exp (2e trimestre) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="6cdaa-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="6cdaa-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="6cdaa-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="6cdaa-138">Ln est la méthode d’API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) et exp est la méthode d’API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="6cdaa-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="6cdaa-139">Utilisez [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="6cdaa-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="6cdaa-140">Examples</span></span>

<span data-ttu-id="6cdaa-141">L’exemple suivant montre comment utiliser un ensemble de clés Quaternion (q0, T1, Q2, Q3) pour calculer les points Quadrangle internes (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="6cdaa-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="6cdaa-142">Cela permet de s’assurer que les tangentes sont continues sur les segments adjacents.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="6cdaa-143">L’exemple de code suivant montre comment vous pouvez interpoler entre Q1 et Q2.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="6cdaa-144">C est +/-Q2 en fonction du résultat de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="6cdaa-145">Qt est le résultat de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="6cdaa-146">Le résultat est une rotation de 45 degrés autour de l’axe z pour Time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="6cdaa-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6cdaa-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cdaa-147">Requirements</span></span>



| <span data-ttu-id="6cdaa-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cdaa-148">Requirement</span></span> | <span data-ttu-id="6cdaa-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdaa-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdaa-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cdaa-150">Header</span></span><br/>  | <dl> <span data-ttu-id="6cdaa-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cdaa-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6cdaa-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cdaa-152">Library</span></span><br/> | <dl> <span data-ttu-id="6cdaa-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cdaa-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6cdaa-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cdaa-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cdaa-155">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="6cdaa-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
