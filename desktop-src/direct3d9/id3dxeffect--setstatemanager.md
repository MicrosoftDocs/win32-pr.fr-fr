---
description: Définissez le gestionnaire d’état des effets.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'ID3DXEffect :: SetStateManager, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb32e3f668884a6f51bd5c5058a4f27e141f0aa3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394075"
---
# <a name="id3dxeffectsetstatemanager-method"></a><span data-ttu-id="c0817-103">ID3DXEffect :: SetStateManager, méthode</span><span class="sxs-lookup"><span data-stu-id="c0817-103">ID3DXEffect::SetStateManager method</span></span>

<span data-ttu-id="c0817-104">Définissez le gestionnaire d’état des effets.</span><span class="sxs-lookup"><span data-stu-id="c0817-104">Set the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0817-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0817-105">Syntax</span></span>


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a><span data-ttu-id="c0817-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0817-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0817-107">*pManager* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0817-107">*pManager* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0817-108">Type : **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span><span class="sxs-lookup"><span data-stu-id="c0817-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span></span>

<span data-ttu-id="c0817-109">Pointeur vers le gestionnaire d’État.</span><span class="sxs-lookup"><span data-stu-id="c0817-109">A pointer to the state manager.</span></span> <span data-ttu-id="c0817-110">Consultez [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="c0817-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0817-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0817-111">Return value</span></span>

<span data-ttu-id="c0817-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0817-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0817-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0817-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0817-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="c0817-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0817-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c0817-115">Remarks</span></span>

<span data-ttu-id="c0817-116">Le [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) est une interface implémentée par l’utilisateur qui fournit des rappels dans une application pour définir l’état de l’appareil à partir d’un effet.</span><span class="sxs-lookup"><span data-stu-id="c0817-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0817-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0817-117">Requirements</span></span>



| <span data-ttu-id="c0817-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0817-118">Requirement</span></span> | <span data-ttu-id="c0817-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0817-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0817-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0817-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c0817-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0817-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c0817-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0817-122">Library</span></span><br/> | <dl> <span data-ttu-id="c0817-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0817-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0817-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0817-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0817-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c0817-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="c0817-126">**ID3DXEffect::GetStateManager**</span><span class="sxs-lookup"><span data-stu-id="c0817-126">**ID3DXEffect::GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




