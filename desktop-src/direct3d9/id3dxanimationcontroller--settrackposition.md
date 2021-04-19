---
description: Définit le suivi sur l’heure d’animation locale spécifiée.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController :: SetTrackPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535832"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a><span data-ttu-id="52d66-103">ID3DXAnimationController :: SetTrackPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="52d66-103">ID3DXAnimationController::SetTrackPosition method</span></span>

<span data-ttu-id="52d66-104">Définit le suivi sur l’heure d’animation locale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="52d66-104">Sets the track to the specified local animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52d66-105">Syntax</span></span>


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="52d66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d66-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52d66-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d66-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d66-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52d66-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="52d66-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="52d66-110">*Position* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52d66-110">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d66-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d66-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52d66-112">Valeur d’heure d’animation locale à assigner à la piste.</span><span class="sxs-lookup"><span data-stu-id="52d66-112">Local animation time value to assign to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52d66-113">Return value</span></span>

<span data-ttu-id="52d66-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52d66-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52d66-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52d66-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52d66-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="52d66-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d66-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d66-117">Requirements</span></span>



| <span data-ttu-id="52d66-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d66-118">Requirement</span></span> | <span data-ttu-id="52d66-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d66-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52d66-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="52d66-120">Header</span></span><br/>  | <dl> <span data-ttu-id="52d66-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d66-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="52d66-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52d66-122">Library</span></span><br/> | <dl> <span data-ttu-id="52d66-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52d66-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52d66-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d66-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="52d66-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
