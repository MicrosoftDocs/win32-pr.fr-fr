---
description: 'ID3DXLine :: OnResetDevice, méthode : utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.'
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: 'ID3DXLine :: OnResetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7e1275e7a7ec894601dc67503e25e1fa82545f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093657"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="b4353-103">ID3DXLine :: OnResetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="b4353-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="b4353-104">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="b4353-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4353-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4353-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="b4353-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4353-106">Parameters</span></span>

<span data-ttu-id="b4353-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4353-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4353-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4353-108">Return value</span></span>

<span data-ttu-id="b4353-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4353-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4353-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4353-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b4353-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b4353-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4353-112">Notes </span><span class="sxs-lookup"><span data-stu-id="b4353-112">Remarks</span></span>

<span data-ttu-id="b4353-113">**ID3DXLine :: OnResetDevice** doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="b4353-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="b4353-114">Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="b4353-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4353-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4353-115">Requirements</span></span>



| <span data-ttu-id="b4353-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4353-116">Requirement</span></span> | <span data-ttu-id="b4353-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4353-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4353-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4353-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b4353-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4353-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b4353-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4353-120">Library</span></span><br/> | <dl> <span data-ttu-id="b4353-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4353-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4353-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4353-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4353-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="b4353-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
