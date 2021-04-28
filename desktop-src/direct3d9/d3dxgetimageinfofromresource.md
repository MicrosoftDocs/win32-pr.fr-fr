---
description: 'Fonction D3DXGetImageInfoFromResource : récupère des informations sur une image donnée dans une ressource.'
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114447"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="5ef47-103">D3DXGetImageInfoFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="5ef47-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="5ef47-104">Récupère des informations sur une image donnée dans une ressource.</span><span class="sxs-lookup"><span data-stu-id="5ef47-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ef47-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5ef47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ef47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef47-107">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ef47-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef47-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ef47-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ef47-109">Module dans lequel la ressource est chargée.</span><span class="sxs-lookup"><span data-stu-id="5ef47-109">Module where the resource is loaded.</span></span> <span data-ttu-id="5ef47-110">Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="5ef47-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="5ef47-111">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ef47-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef47-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ef47-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ef47-113">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="5ef47-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="5ef47-114">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5ef47-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5ef47-115">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5ef47-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5ef47-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5ef47-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5ef47-117">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ef47-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef47-118">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ef47-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="5ef47-119">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="5ef47-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef47-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ef47-120">Return value</span></span>

<span data-ttu-id="5ef47-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ef47-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ef47-122">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ef47-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5ef47-123">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="5ef47-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef47-124">Notes </span><span class="sxs-lookup"><span data-stu-id="5ef47-124">Remarks</span></span>

<span data-ttu-id="5ef47-125">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5ef47-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5ef47-126">Si Unicode est défini, l’appel de fonction est résolu en D3DXGetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="5ef47-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="5ef47-127">Dans le cas contraire, l’appel de fonction est résolu en D3DXGetImageInfoFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="5ef47-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef47-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ef47-128">Requirements</span></span>



| <span data-ttu-id="5ef47-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ef47-129">Requirement</span></span> | <span data-ttu-id="5ef47-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ef47-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef47-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ef47-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5ef47-132"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef47-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5ef47-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ef47-133">Library</span></span><br/> | <dl> <span data-ttu-id="5ef47-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ef47-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5ef47-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ef47-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef47-136">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5ef47-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="5ef47-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="5ef47-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="5ef47-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="5ef47-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
