---
description: Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer :: LockBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522368"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="9aba5-103">ID3DXPRTBuffer :: LockBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="9aba5-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="9aba5-104">Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9aba5-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aba5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9aba5-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="9aba5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9aba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aba5-107">*Démarrer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9aba5-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aba5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aba5-109">Index de l’exemple de données de vertex ou de Texel.</span><span class="sxs-lookup"><span data-stu-id="9aba5-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="9aba5-110">*Échantillons* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9aba5-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba5-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aba5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aba5-112">Nombre de vertex (ou de texels) échantillonnés.</span><span class="sxs-lookup"><span data-stu-id="9aba5-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="9aba5-113">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9aba5-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aba5-114">Type : **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9aba5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="9aba5-115">Pointeur vers l’emplacement dans la mémoire où commence l’exemple de démarrage.</span><span class="sxs-lookup"><span data-stu-id="9aba5-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="9aba5-116">La disposition de la mémoire des données de la mémoire tampon est :</span><span class="sxs-lookup"><span data-stu-id="9aba5-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aba5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9aba5-117">Return value</span></span>

<span data-ttu-id="9aba5-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9aba5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9aba5-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9aba5-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9aba5-120">Si la méthode échoue, la valeur suivante est retournée :</span><span class="sxs-lookup"><span data-stu-id="9aba5-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="9aba5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9aba5-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9aba5-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9aba5-122">Requirements</span></span>



| <span data-ttu-id="9aba5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9aba5-123">Requirement</span></span> | <span data-ttu-id="9aba5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9aba5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aba5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9aba5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9aba5-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aba5-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9aba5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9aba5-127">Library</span></span><br/> | <dl> <span data-ttu-id="9aba5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aba5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9aba5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aba5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aba5-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="9aba5-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="9aba5-131">**ID3DXPRTBuffer::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="9aba5-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="9aba5-132">**ID3DXPRTBuffer::GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="9aba5-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="9aba5-133">**ID3DXPRTBuffer::GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="9aba5-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
