---
description: 'L’application implémente cette méthode. Cette méthode est appelée quand un rappel se produit pour une animation définie dans l’une des pistes pendant un appel à ID3DXAnimationController :: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler :: HandleCallback, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525299"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="bfdde-104">ID3DXAnimationCallbackHandler :: HandleCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="bfdde-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="bfdde-105">L’application implémente cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bfdde-105">The application implements this method.</span></span> <span data-ttu-id="bfdde-106">Cette méthode est appelée quand un rappel se produit pour une animation définie dans l’une des pistes pendant un appel à [**ID3DXAnimationController :: AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="bfdde-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdde-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfdde-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="bfdde-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfdde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfdde-109">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfdde-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfdde-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfdde-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bfdde-111">Identificateur de la piste sur laquelle le rappel se produit.</span><span class="sxs-lookup"><span data-stu-id="bfdde-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="bfdde-112">*pCallbackData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfdde-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfdde-113">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfdde-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bfdde-114">Pointeur vers des données de rappel appartenant à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bfdde-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfdde-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfdde-115">Return value</span></span>

<span data-ttu-id="bfdde-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bfdde-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bfdde-117">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="bfdde-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="bfdde-118">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bfdde-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="bfdde-119">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="bfdde-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfdde-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfdde-120">Requirements</span></span>



| <span data-ttu-id="bfdde-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfdde-121">Requirement</span></span> | <span data-ttu-id="bfdde-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfdde-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdde-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfdde-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bfdde-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfdde-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bfdde-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bfdde-125">Library</span></span><br/> | <dl> <span data-ttu-id="bfdde-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfdde-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfdde-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfdde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdde-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="bfdde-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
