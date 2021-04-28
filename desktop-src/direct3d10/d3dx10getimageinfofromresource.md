---
description: 'Fonction D3DX10GetImageInfoFromResource : récupère des informations sur une image donnée dans une ressource.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: D3DX10GetImageInfoFromResource, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098367"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="37d72-103">D3DX10GetImageInfoFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="37d72-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="37d72-104">Récupère des informations sur une image donnée dans une ressource.</span><span class="sxs-lookup"><span data-stu-id="37d72-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d72-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37d72-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="37d72-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37d72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d72-107">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37d72-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d72-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37d72-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37d72-109">Module dans lequel la ressource est chargée.</span><span class="sxs-lookup"><span data-stu-id="37d72-109">Module where the resource is loaded.</span></span> <span data-ttu-id="37d72-110">Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="37d72-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="37d72-111">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37d72-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d72-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37d72-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37d72-113">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="37d72-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="37d72-114">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="37d72-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="37d72-115">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="37d72-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="37d72-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="37d72-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="37d72-117">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37d72-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d72-118">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="37d72-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="37d72-119">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="37d72-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="37d72-120">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="37d72-120">Can be **NULL**.</span></span> <span data-ttu-id="37d72-121">Consultez [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="37d72-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="37d72-122">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37d72-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d72-123">Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="37d72-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="37d72-124">Pointeur vers une \_ structure d’informations d’image d3dx10 \_ à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="37d72-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="37d72-125">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37d72-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37d72-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="37d72-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="37d72-127">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="37d72-127">A pointer to the return value.</span></span> <span data-ttu-id="37d72-128">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="37d72-128">May be **NULL**.</span></span> <span data-ttu-id="37d72-129">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="37d72-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d72-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37d72-130">Return value</span></span>

<span data-ttu-id="37d72-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37d72-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37d72-132">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37d72-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37d72-133">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="37d72-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="37d72-134">Notes </span><span class="sxs-lookup"><span data-stu-id="37d72-134">Remarks</span></span>

<span data-ttu-id="37d72-135">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="37d72-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="37d72-136">Si Unicode est défini, l’appel de fonction est résolu en D3DX10GetImageInfoFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="37d72-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="37d72-137">Dans le cas contraire, l’appel de fonction est résolu en D3DX10GetImageInfoFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="37d72-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d72-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d72-138">Requirements</span></span>



| <span data-ttu-id="37d72-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37d72-139">Requirement</span></span> | <span data-ttu-id="37d72-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d72-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37d72-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="37d72-141">Header</span></span><br/>  | <dl> <span data-ttu-id="37d72-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="37d72-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="37d72-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37d72-143">Library</span></span><br/> | <dl> <span data-ttu-id="37d72-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37d72-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="37d72-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d72-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d72-146">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="37d72-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
