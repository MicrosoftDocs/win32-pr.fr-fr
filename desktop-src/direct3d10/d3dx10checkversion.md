---
description: 'Fonction D3DX10CheckVersion : Vérifiez que la version de D3DX avec laquelle vous avez compilé est la version que vous exécutez.'
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
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105347"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="41d8b-103">D3DX10CheckVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="41d8b-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="41d8b-104">Vérifiez que la version de D3DX que vous avez compilée est la version que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="41d8b-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41d8b-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="41d8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41d8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d8b-107">*D3DSdkVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41d8b-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d8b-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41d8b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41d8b-109">Utilisez la \_ version du SDK D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="41d8b-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="41d8b-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="41d8b-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="41d8b-111">*D3DX10SdkVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41d8b-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d8b-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41d8b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41d8b-113">Utilisez la \_ version du SDK d3dx10 \_ .</span><span class="sxs-lookup"><span data-stu-id="41d8b-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="41d8b-114">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="41d8b-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d8b-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41d8b-115">Return value</span></span>

<span data-ttu-id="41d8b-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41d8b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41d8b-117">Si la version ne correspond pas, la fonction retourne FALSe (un nombre inférieur ou égal à 0, le nombre lui-même n’a aucune signification).</span><span class="sxs-lookup"><span data-stu-id="41d8b-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="41d8b-118">Notes </span><span class="sxs-lookup"><span data-stu-id="41d8b-118">Remarks</span></span>

<span data-ttu-id="41d8b-119">Utilisez cette fonction pendant l’initialisation de votre application.</span><span class="sxs-lookup"><span data-stu-id="41d8b-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="41d8b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41d8b-120">Requirements</span></span>



| <span data-ttu-id="41d8b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d8b-121">Requirement</span></span> | <span data-ttu-id="41d8b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="41d8b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d8b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="41d8b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="41d8b-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d8b-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="41d8b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41d8b-125">Library</span></span><br/> | <dl> <span data-ttu-id="41d8b-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41d8b-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41d8b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41d8b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d8b-128">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="41d8b-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
