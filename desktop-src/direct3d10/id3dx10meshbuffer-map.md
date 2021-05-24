---
description: Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer :: Map, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335353"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="c50aa-103">ID3DX10MeshBuffer :: Map, méthode</span><span class="sxs-lookup"><span data-stu-id="c50aa-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="c50aa-104">Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.</span><span class="sxs-lookup"><span data-stu-id="c50aa-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c50aa-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="c50aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c50aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50aa-107">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c50aa-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c50aa-108">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="c50aa-108">Type: **void\*\***</span></span>

<span data-ttu-id="c50aa-109">Pointeur vers les données de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c50aa-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="c50aa-110">*psize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c50aa-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c50aa-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c50aa-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c50aa-112">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c50aa-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50aa-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c50aa-113">Return value</span></span>

<span data-ttu-id="c50aa-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c50aa-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c50aa-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c50aa-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c50aa-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c50aa-116">Remarks</span></span>



 <span data-ttu-id="c50aa-117">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="c50aa-117">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="c50aa-118">Map () dans Direct3D 10 est analogue à la carte de ressources () dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c50aa-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="c50aa-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c50aa-119">Requirements</span></span>



| <span data-ttu-id="c50aa-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c50aa-120">Requirement</span></span> | <span data-ttu-id="c50aa-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c50aa-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c50aa-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c50aa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c50aa-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50aa-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c50aa-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c50aa-124">Library</span></span><br/> | <dl> <span data-ttu-id="c50aa-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c50aa-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50aa-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c50aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50aa-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="c50aa-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="c50aa-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="c50aa-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
