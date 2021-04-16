---
description: Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'ID3DXFont :: OnResetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6e65001f484ed7d7a984ed1f9463b996056e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394172"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="41104-103">ID3DXFont :: OnResetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="41104-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="41104-104">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="41104-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="41104-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41104-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="41104-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41104-106">Parameters</span></span>

<span data-ttu-id="41104-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="41104-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41104-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41104-108">Return value</span></span>

<span data-ttu-id="41104-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41104-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41104-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41104-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="41104-111">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="41104-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="41104-112">Notes</span><span class="sxs-lookup"><span data-stu-id="41104-112">Remarks</span></span>

<span data-ttu-id="41104-113">**OnResetDevice** doit être appelé chaque fois que l’appareil est réinitialisé (à l’aide de la [**réinitialisation**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), avant d’appeler d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="41104-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="41104-114">Il s’agit d’un bon emplacement pour acquérir à nouveau des ressources de mémoire vidéo et capturer des blocs d’État.</span><span class="sxs-lookup"><span data-stu-id="41104-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="41104-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41104-115">Requirements</span></span>



| <span data-ttu-id="41104-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41104-116">Requirement</span></span> | <span data-ttu-id="41104-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="41104-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41104-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="41104-118">Header</span></span><br/>  | <dl> <span data-ttu-id="41104-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="41104-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="41104-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41104-120">Library</span></span><br/> | <dl> <span data-ttu-id="41104-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41104-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41104-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41104-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41104-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="41104-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
