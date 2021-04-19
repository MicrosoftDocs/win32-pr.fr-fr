---
description: Enregistre une mémoire tampon de transfert luminance (PRT) précalculée sur le disque.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: D3DXSavePRTBufferToFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529608"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="f0750-103">D3DXSavePRTBufferToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="f0750-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="f0750-104">Enregistre une mémoire tampon de transfert luminance (PRT) précalculée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="f0750-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0750-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0750-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="f0750-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0750-106">Parameters</span></span>

<span data-ttu-id="f0750-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0750-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="f0750-108">Type : **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0750-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0750-109">Nom du fichier dans lequel la mémoire tampon doit être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="f0750-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="f0750-110">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0750-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="f0750-111">Type : **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f0750-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f0750-112">Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f0750-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0750-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0750-113">Return value</span></span>

<span data-ttu-id="f0750-114">Type : **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f0750-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f0750-115">Si la méthode est réussie, la valeur de retour est **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f0750-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="f0750-116">Si la méthode échoue, la valeur de retour peut être **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="f0750-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0750-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f0750-117">Remarks</span></span>

<span data-ttu-id="f0750-118">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f0750-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f0750-119">Si Unicode est défini, l’appel de fonction est résolu en [D3DXSavePRTBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="f0750-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="f0750-120">Dans le cas contraire, l’appel de fonction est résolu en **D3DXSavePRTBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="f0750-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="f0750-121">Le format de fichier PRT est un fichier binaire sous la forme d’un en-tête, puis d’un bloc de données.</span><span class="sxs-lookup"><span data-stu-id="f0750-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="f0750-122">Pour le cas de *bIsTex* qui est différent de zéro, *échantillons* doit être égal à `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="f0750-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="f0750-123">Le bloc de données qui suit l’en-tête est `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="f0750-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0750-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0750-124">Requirements</span></span>

| <span data-ttu-id="f0750-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0750-125">Requirement</span></span> | <span data-ttu-id="f0750-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0750-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0750-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0750-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f0750-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0750-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f0750-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0750-129">Library</span></span><br/> | <dl> <span data-ttu-id="f0750-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0750-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="f0750-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0750-131">See also</span></span>

[<span data-ttu-id="f0750-132">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="f0750-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
