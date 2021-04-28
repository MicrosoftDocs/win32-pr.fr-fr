---
description: 'Fonction D3DX10GetImageInfoFromFile : récupère des informations sur un fichier image donné.'
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
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098330"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="9032a-103">D3DX10GetImageInfoFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="9032a-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="9032a-104">Récupère des informations sur un fichier image donné.</span><span class="sxs-lookup"><span data-stu-id="9032a-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9032a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9032a-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="9032a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9032a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9032a-107">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9032a-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9032a-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9032a-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9032a-109">Nom de fichier de l’image sur laquelle récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="9032a-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="9032a-110">Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9032a-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9032a-111">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9032a-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9032a-112">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9032a-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="9032a-113">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9032a-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="9032a-114">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9032a-114">Can be **NULL**.</span></span> <span data-ttu-id="9032a-115">Consultez [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9032a-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="9032a-116">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9032a-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9032a-117">Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9032a-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="9032a-118">Pointeur vers une \_ structure d’informations d’image d3dx10 \_ à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="9032a-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="9032a-119">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9032a-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9032a-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="9032a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="9032a-121">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9032a-121">A pointer to the return value.</span></span> <span data-ttu-id="9032a-122">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9032a-122">May be **NULL**.</span></span> <span data-ttu-id="9032a-123">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="9032a-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9032a-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9032a-124">Return value</span></span>

<span data-ttu-id="9032a-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9032a-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9032a-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9032a-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9032a-127">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9032a-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="9032a-128">Notes </span><span class="sxs-lookup"><span data-stu-id="9032a-128">Remarks</span></span>

<span data-ttu-id="9032a-129">Cette fonction prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="9032a-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="9032a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9032a-130">Requirements</span></span>



| <span data-ttu-id="9032a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9032a-131">Requirement</span></span> | <span data-ttu-id="9032a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9032a-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9032a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9032a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9032a-134"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9032a-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9032a-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9032a-135">Library</span></span><br/> | <dl> <span data-ttu-id="9032a-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9032a-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9032a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9032a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9032a-138">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="9032a-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
