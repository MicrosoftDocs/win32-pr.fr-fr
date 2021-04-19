---
description: Ajoute une sortie d’animation au contrôleur d’animation et enregistre les pointeurs pour les transformations de mise à l’échelle, de rotation et de translation (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController :: RegisterAnimationOutput, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531566"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="49dc7-103">ID3DXAnimationController :: RegisterAnimationOutput, méthode</span><span class="sxs-lookup"><span data-stu-id="49dc7-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="49dc7-104">Ajoute une sortie d’animation au contrôleur d’animation et enregistre les pointeurs pour les transformations de mise à l’échelle, de rotation et de translation (SRT).</span><span class="sxs-lookup"><span data-stu-id="49dc7-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="49dc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49dc7-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="49dc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49dc7-107">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49dc7-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49dc7-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49dc7-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49dc7-109">Nom de la sortie de l’animation.</span><span class="sxs-lookup"><span data-stu-id="49dc7-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="49dc7-110">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49dc7-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49dc7-111">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="49dc7-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="49dc7-112">Pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) contenant les données de transformation SRT.</span><span class="sxs-lookup"><span data-stu-id="49dc7-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="49dc7-113">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="49dc7-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="49dc7-114">*pScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49dc7-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49dc7-115">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="49dc7-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49dc7-116">Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit l’échelle de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="49dc7-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="49dc7-117">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="49dc7-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="49dc7-118">*protique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49dc7-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49dc7-119">Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="49dc7-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="49dc7-120">Pointeur vers un Quaternion [**D3DXQUATERNION**](d3dxquaternion.md) qui décrit la rotation de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="49dc7-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="49dc7-121">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="49dc7-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="49dc7-122">*pTranslation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49dc7-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49dc7-123">Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="49dc7-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="49dc7-124">Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit la traduction de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="49dc7-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="49dc7-125">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="49dc7-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49dc7-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49dc7-126">Return value</span></span>

<span data-ttu-id="49dc7-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49dc7-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49dc7-128">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49dc7-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="49dc7-129">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="49dc7-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="49dc7-130">Notes</span><span class="sxs-lookup"><span data-stu-id="49dc7-130">Remarks</span></span>

<span data-ttu-id="49dc7-131">Si la sortie de l’animation est déjà inscrite, pMatrix est rempli avec les données de transformation d’entrée.</span><span class="sxs-lookup"><span data-stu-id="49dc7-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="49dc7-132">Les jeux d’animations créés avec [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) inscrivent automatiquement tous les jeux d’animations chargés.</span><span class="sxs-lookup"><span data-stu-id="49dc7-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="49dc7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49dc7-133">Requirements</span></span>



| <span data-ttu-id="49dc7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49dc7-134">Requirement</span></span> | <span data-ttu-id="49dc7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="49dc7-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49dc7-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="49dc7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="49dc7-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="49dc7-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="49dc7-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49dc7-138">Library</span></span><br/> | <dl> <span data-ttu-id="49dc7-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49dc7-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49dc7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49dc7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49dc7-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="49dc7-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
