---
description: Annuler le mappage d’une mémoire tampon.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'ID3DX10MeshBuffer :: DEMAPPAGE, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11b15f8bc1e4103503b183672ebd31e92b4daea7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335373"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="6652e-103">ID3DX10MeshBuffer :: DEMAPPAGE, méthode</span><span class="sxs-lookup"><span data-stu-id="6652e-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="6652e-104">Annuler le mappage d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6652e-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6652e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6652e-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="6652e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6652e-106">Parameters</span></span>

<span data-ttu-id="6652e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6652e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6652e-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6652e-108">Return value</span></span>

<span data-ttu-id="6652e-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6652e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6652e-110">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6652e-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6652e-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6652e-111">Remarks</span></span>



<span data-ttu-id="6652e-112">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="6652e-112">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="6652e-113">Le démappage () dans Direct3D 10 est analogue au déverrouillage de ressource () dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6652e-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="6652e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6652e-114">Requirements</span></span>



| <span data-ttu-id="6652e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6652e-115">Requirement</span></span> | <span data-ttu-id="6652e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6652e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6652e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6652e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6652e-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6652e-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6652e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6652e-119">Library</span></span><br/> | <dl> <span data-ttu-id="6652e-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6652e-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6652e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6652e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6652e-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="6652e-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="6652e-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6652e-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




