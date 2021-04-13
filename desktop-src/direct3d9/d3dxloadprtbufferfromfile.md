---
description: Charge dans la mémoire une mémoire tampon de transfert luminance (PRT) précalculée qui a été enregistrée sur le disque.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: D3DXLoadPRTBufferFromFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322666"
---
# <a name="d3dxloadprtbufferfromfile-function"></a><span data-ttu-id="acb2c-103">D3DXLoadPRTBufferFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="acb2c-103">D3DXLoadPRTBufferFromFile function</span></span>

<span data-ttu-id="acb2c-104">Charge dans la mémoire une mémoire tampon de transfert luminance (PRT) précalculée qui a été enregistrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="acb2c-104">Loads into memory a precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="acb2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acb2c-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="acb2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acb2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb2c-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acb2c-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acb2c-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="acb2c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="acb2c-109">Nom du fichier à partir duquel charger les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="acb2c-109">Name of the file from which to load the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="acb2c-110">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="acb2c-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb2c-111">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="acb2c-111">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="acb2c-112">Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="acb2c-112">Address of a pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb2c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acb2c-113">Return value</span></span>

<span data-ttu-id="acb2c-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="acb2c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="acb2c-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="acb2c-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="acb2c-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="acb2c-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb2c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="acb2c-117">Remarks</span></span>

<span data-ttu-id="acb2c-118">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="acb2c-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="acb2c-119">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadPRTBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="acb2c-119">If Unicode is defined, the function call resolves to D3DXLoadPRTBufferFromFileW.</span></span> <span data-ttu-id="acb2c-120">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadPRTBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="acb2c-120">Otherwise, the function call resolves to D3DXLoadPRTBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb2c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acb2c-121">Requirements</span></span>



| <span data-ttu-id="acb2c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acb2c-122">Requirement</span></span> | <span data-ttu-id="acb2c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="acb2c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acb2c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="acb2c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="acb2c-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb2c-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="acb2c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="acb2c-126">Library</span></span><br/> | <dl> <span data-ttu-id="acb2c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acb2c-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="acb2c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acb2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb2c-129">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="acb2c-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
