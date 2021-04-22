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
ms.openlocfilehash: 3dbc87697750ee07939602dc694468aa68f5c66d
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881848"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="cfa21-103">IDWriteBitmapRenderTarget2 :: GetBitmapData, méthode (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="cfa21-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="cfa21-104">Récupère les données de pixels d’une cible de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="cfa21-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfa21-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="cfa21-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="cfa21-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="cfa21-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="cfa21-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="cfa21-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa21-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfa21-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="cfa21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfa21-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="cfa21-110">Type : \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="cfa21-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="cfa21-111">Pointeur vers les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="cfa21-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfa21-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cfa21-112">Return value</span></span>

<span data-ttu-id="cfa21-113">Type : <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="cfa21-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="cfa21-114">Si cette méthode est réussie, elle retourne <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="cfa21-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="cfa21-115">Sinon, elle retourne un code d’erreur <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="cfa21-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="cfa21-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="cfa21-116">Examples</span></span>

<span data-ttu-id="cfa21-117">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="cfa21-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa21-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfa21-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cfa21-119">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="cfa21-119">**Minimum supported client**</span></span> | <span data-ttu-id="cfa21-120">Windows 10, réunion de projet (applications Win32)</span><span class="sxs-lookup"><span data-stu-id="cfa21-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="cfa21-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="cfa21-121">**Header**</span></span> | <span data-ttu-id="cfa21-122">dwrite_3. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="cfa21-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="cfa21-123">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="cfa21-123">**Library**</span></span> | <span data-ttu-id="cfa21-124">DWrite. lib</span><span class="sxs-lookup"><span data-stu-id="cfa21-124">Dwrite.lib</span></span> |
| <span data-ttu-id="cfa21-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="cfa21-125">**DLL**</span></span> | <span data-ttu-id="cfa21-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="cfa21-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="cfa21-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfa21-127">See also</span></span>

[<span data-ttu-id="cfa21-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="cfa21-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
