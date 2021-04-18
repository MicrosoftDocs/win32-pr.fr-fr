---
description: Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: D3DXCheckVersion, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536247"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="d2e6e-103">D3DXCheckVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="d2e6e-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="d2e6e-104">Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="d2e6e-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2e6e-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d2e6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2e6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e6e-107">*D3DSDKVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2e6e-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e6e-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2e6e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2e6e-109">Utilisez la \_ version du kit de développement logiciel D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="d2e6e-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="d2e6e-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="d2e6e-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d2e6e-111">*D3DXSDKVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2e6e-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e6e-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2e6e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2e6e-113">Utilisez la \_ version du kit de développement logiciel D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="d2e6e-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="d2e6e-114">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="d2e6e-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e6e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2e6e-115">Return value</span></span>

<span data-ttu-id="d2e6e-116">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2e6e-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2e6e-117">Retourne la **valeur true** si la version de D3DX avec laquelle vous avez compilé est la version avec laquelle vous exécutez. Sinon, la **valeur false** est retournée.</span><span class="sxs-lookup"><span data-stu-id="d2e6e-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e6e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d2e6e-118">Remarks</span></span>

<span data-ttu-id="d2e6e-119">Utilisez cette fonction pendant l’initialisation de votre application comme suit :</span><span class="sxs-lookup"><span data-stu-id="d2e6e-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="d2e6e-120">Utilisez [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) pour vérifier que le runtime approprié est installé.</span><span class="sxs-lookup"><span data-stu-id="d2e6e-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e6e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2e6e-121">Requirements</span></span>



| <span data-ttu-id="d2e6e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2e6e-122">Requirement</span></span> | <span data-ttu-id="d2e6e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2e6e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e6e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2e6e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d2e6e-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e6e-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d2e6e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2e6e-126">Library</span></span><br/> | <dl> <span data-ttu-id="d2e6e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2e6e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2e6e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e6e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e6e-129">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="d2e6e-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
