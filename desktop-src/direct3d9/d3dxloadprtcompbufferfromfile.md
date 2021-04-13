---
description: Charge en mémoire une mémoire tampon de transfert luminance précalculée (PRT) compressée qui a été enregistrée sur le disque.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: D3DXLoadPRTCompBufferFromFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323302"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="fedc5-103">D3DXLoadPRTCompBufferFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="fedc5-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="fedc5-104">Charge en mémoire une mémoire tampon de transfert luminance précalculée (PRT) compressée qui a été enregistrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="fedc5-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="fedc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fedc5-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fedc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fedc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fedc5-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fedc5-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fedc5-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fedc5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fedc5-109">Nom du fichier à partir duquel charger les données de la mémoire tampon compressées.</span><span class="sxs-lookup"><span data-stu-id="fedc5-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="fedc5-110">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fedc5-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fedc5-111">Type : **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fedc5-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="fedc5-112">Adresse d’un pointeur vers l’objet [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="fedc5-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fedc5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fedc5-113">Return value</span></span>

<span data-ttu-id="fedc5-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fedc5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fedc5-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fedc5-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fedc5-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fedc5-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fedc5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fedc5-117">Remarks</span></span>

<span data-ttu-id="fedc5-118">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fedc5-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fedc5-119">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadPRTCompBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="fedc5-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="fedc5-120">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadPRTCompBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="fedc5-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedc5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fedc5-121">Requirements</span></span>



| <span data-ttu-id="fedc5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fedc5-122">Requirement</span></span> | <span data-ttu-id="fedc5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fedc5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fedc5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fedc5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fedc5-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedc5-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fedc5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fedc5-126">Library</span></span><br/> | <dl> <span data-ttu-id="fedc5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fedc5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fedc5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fedc5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedc5-129">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="fedc5-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
