---
description: Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'ID3DXEffect :: OnResetDevice, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543560"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="93f6b-103">ID3DXEffect :: OnResetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="93f6b-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="93f6b-104">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="93f6b-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93f6b-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="93f6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93f6b-106">Parameters</span></span>

<span data-ttu-id="93f6b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="93f6b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93f6b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93f6b-108">Return value</span></span>

<span data-ttu-id="93f6b-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93f6b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93f6b-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93f6b-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93f6b-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="93f6b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f6b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="93f6b-112">Remarks</span></span>

<span data-ttu-id="93f6b-113">**ID3DXEffect :: OnResetDevice** doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="93f6b-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="93f6b-114">Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="93f6b-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f6b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93f6b-115">Requirements</span></span>



| <span data-ttu-id="93f6b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93f6b-116">Requirement</span></span> | <span data-ttu-id="93f6b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="93f6b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f6b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="93f6b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="93f6b-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="93f6b-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="93f6b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93f6b-120">Library</span></span><br/> | <dl> <span data-ttu-id="93f6b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93f6b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="93f6b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93f6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f6b-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="93f6b-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
