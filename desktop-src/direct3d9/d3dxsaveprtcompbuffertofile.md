---
description: Enregistre une mémoire tampon de transfert luminance précalculée (PRT) compressée sur le disque.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: D3DXSavePRTCompBufferToFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953840"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="4e4c8-103">D3DXSavePRTCompBufferToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="4e4c8-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="4e4c8-104">Enregistre une mémoire tampon de transfert luminance précalculée (PRT) compressée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e4c8-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="4e4c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e4c8-106">Parameters</span></span>

<span data-ttu-id="4e4c8-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e4c8-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="4e4c8-108">Type : **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e4c8-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e4c8-109">Nom du fichier dans lequel la mémoire tampon compressée doit être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="4e4c8-110">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e4c8-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="4e4c8-111">Type : **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4e4c8-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="4e4c8-112">Adresse d’un pointeur vers l’objet [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e4c8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e4c8-113">Return value</span></span>

<span data-ttu-id="4e4c8-114">Type : **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="4e4c8-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="4e4c8-115">Si la méthode est réussie, la valeur de retour est **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="4e4c8-116">Si la méthode échoue, la valeur de retour peut être **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e4c8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4e4c8-117">Remarks</span></span>

<span data-ttu-id="4e4c8-118">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4e4c8-119">Si Unicode est défini, l’appel de fonction est résolu en [D3DXSavePRTCompBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="4e4c8-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="4e4c8-120">Dans le cas contraire, l’appel de fonction est résolu en **D3DXSavePRTCompBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="4e4c8-121">Le format de fichier de l’APC est un fichier binaire sous la forme d’un en-tête, puis de deux ou trois blocs de données.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="4e4c8-122">Pour le cas de *bIsTex* qui est différent de zéro, *échantillons* doit être égal à `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="4e4c8-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="4e4c8-123">Le bloc de données de base qui suit l’en-tête est `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="4e4c8-124">Voici le bloc de données de pondérations de l’APC, qui est de `NumPCA * NumSamples * sizeof(float)` octets.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="4e4c8-125">Si *NumClusters* est supérieur à 1, le fichier se termine par le bloc de données des ID de cluster d' `NumSamples * sizeof(UINT)` octets.</span><span class="sxs-lookup"><span data-stu-id="4e4c8-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4c8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e4c8-126">Requirements</span></span>

| <span data-ttu-id="4e4c8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e4c8-127">Requirement</span></span> | <span data-ttu-id="4e4c8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e4c8-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4c8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e4c8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4e4c8-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e4c8-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4e4c8-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e4c8-131">Library</span></span><br/> | <dl> <span data-ttu-id="4e4c8-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e4c8-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="4e4c8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e4c8-133">See also</span></span>

[<span data-ttu-id="4e4c8-134">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="4e4c8-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
