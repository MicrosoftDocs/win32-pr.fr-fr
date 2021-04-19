---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Récupère les données de pixels d’une cible de rendu bitmap.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106545195"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="93100-103">IDWriteBitmapRenderTarget2 :: GetBitmapData, méthode (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="93100-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="93100-104">Récupère les données de pixels d’une cible de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="93100-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93100-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="93100-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="93100-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="93100-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="93100-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="93100-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="93100-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93100-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="93100-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93100-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="93100-110">Type : \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="93100-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="93100-111">Pointeur vers les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="93100-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="93100-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93100-112">Return value</span></span>

<span data-ttu-id="93100-113">Type : <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="93100-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="93100-114">Si cette méthode est réussie, elle retourne <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="93100-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="93100-115">Sinon, elle retourne un code d’erreur <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="93100-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="93100-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="93100-116">Examples</span></span>

<span data-ttu-id="93100-117">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="93100-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="93100-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93100-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="93100-119">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="93100-119">**Minimum supported client**</span></span> | <span data-ttu-id="93100-120">Windows 10, projet Réunion 0,1 version préliminaire [applications Win32]</span><span class="sxs-lookup"><span data-stu-id="93100-120">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="93100-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="93100-121">**Header**</span></span> | <span data-ttu-id="93100-122">dwrite_3. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="93100-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="93100-123">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="93100-123">**Library**</span></span> | <span data-ttu-id="93100-124">DWrite. lib</span><span class="sxs-lookup"><span data-stu-id="93100-124">Dwrite.lib</span></span> |
| <span data-ttu-id="93100-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="93100-125">**DLL**</span></span> | <span data-ttu-id="93100-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="93100-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="93100-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93100-127">See also</span></span>

[<span data-ttu-id="93100-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="93100-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)