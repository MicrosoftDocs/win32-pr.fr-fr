---
description: Récupère des informations sur un fichier image donné.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: D3DX10GetImageInfoFromFile, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 836d2e18b5c1c48bbe64d0026e97f8ebc5a066ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531515"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="936e5-103">D3DX10GetImageInfoFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="936e5-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="936e5-104">Récupère des informations sur un fichier image donné.</span><span class="sxs-lookup"><span data-stu-id="936e5-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="936e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="936e5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="936e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="936e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936e5-107">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="936e5-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936e5-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="936e5-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="936e5-109">Nom de fichier de l’image sur laquelle récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="936e5-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="936e5-110">Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="936e5-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="936e5-111">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="936e5-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936e5-112">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="936e5-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="936e5-113">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="936e5-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="936e5-114">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="936e5-114">Can be **NULL**.</span></span> <span data-ttu-id="936e5-115">Consultez [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="936e5-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="936e5-116">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="936e5-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936e5-117">Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="936e5-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="936e5-118">Pointeur vers une \_ structure d’informations d’image d3dx10 \_ à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="936e5-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="936e5-119">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="936e5-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="936e5-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="936e5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="936e5-121">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="936e5-121">A pointer to the return value.</span></span> <span data-ttu-id="936e5-122">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="936e5-122">May be **NULL**.</span></span> <span data-ttu-id="936e5-123">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="936e5-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936e5-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="936e5-124">Return value</span></span>

<span data-ttu-id="936e5-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="936e5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="936e5-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="936e5-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="936e5-127">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="936e5-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="936e5-128">Notes</span><span class="sxs-lookup"><span data-stu-id="936e5-128">Remarks</span></span>

<span data-ttu-id="936e5-129">Cette fonction prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="936e5-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="936e5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="936e5-130">Requirements</span></span>



| <span data-ttu-id="936e5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="936e5-131">Requirement</span></span> | <span data-ttu-id="936e5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="936e5-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="936e5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="936e5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="936e5-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="936e5-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="936e5-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="936e5-135">Library</span></span><br/> | <dl> <span data-ttu-id="936e5-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="936e5-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="936e5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="936e5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936e5-138">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="936e5-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
