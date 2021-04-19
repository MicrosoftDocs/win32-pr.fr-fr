---
description: Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: D3DX10CheckVersion, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542192"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="070d2-103">D3DX10CheckVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="070d2-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="070d2-104">Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="070d2-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="070d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="070d2-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="070d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="070d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070d2-107">*D3DSdkVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="070d2-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070d2-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="070d2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="070d2-109">Utilisez la \_ version du SDK D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="070d2-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="070d2-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="070d2-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="070d2-111">*D3DX10SdkVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="070d2-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070d2-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="070d2-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="070d2-113">Utilisez la \_ version du SDK d3dx10 \_ .</span><span class="sxs-lookup"><span data-stu-id="070d2-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="070d2-114">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="070d2-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="070d2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="070d2-115">Return value</span></span>

<span data-ttu-id="070d2-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="070d2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="070d2-117">Si la version ne correspond pas, la fonction retourne FALSe (un nombre inférieur ou égal à 0, le nombre lui-même n’a aucune signification).</span><span class="sxs-lookup"><span data-stu-id="070d2-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="070d2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="070d2-118">Remarks</span></span>

<span data-ttu-id="070d2-119">Utilisez cette fonction pendant l’initialisation de votre application.</span><span class="sxs-lookup"><span data-stu-id="070d2-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="070d2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="070d2-120">Requirements</span></span>



| <span data-ttu-id="070d2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="070d2-121">Requirement</span></span> | <span data-ttu-id="070d2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="070d2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="070d2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="070d2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="070d2-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="070d2-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="070d2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="070d2-125">Library</span></span><br/> | <dl> <span data-ttu-id="070d2-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="070d2-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="070d2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="070d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070d2-128">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="070d2-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
