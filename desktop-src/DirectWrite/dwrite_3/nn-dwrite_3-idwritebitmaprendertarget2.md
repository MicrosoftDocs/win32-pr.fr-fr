---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes.
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211191"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="1ee36-103">Interface IDWriteBitmapRenderTarget2 (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="1ee36-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="1ee36-104">Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes.</span><span class="sxs-lookup"><span data-stu-id="1ee36-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ee36-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="1ee36-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="1ee36-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="1ee36-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="1ee36-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="1ee36-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="inheritance"></a><span data-ttu-id="1ee36-108">Héritage</span><span class="sxs-lookup"><span data-stu-id="1ee36-108">Inheritance</span></span>

<span data-ttu-id="1ee36-109">L’interface **IDWriteBitmapRenderTarget2** hérite de [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span><span class="sxs-lookup"><span data-stu-id="1ee36-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="1ee36-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1ee36-110">Methods</span></span>

<span data-ttu-id="1ee36-111">L’interface **IDWriteBitmapRenderTarget2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1ee36-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="1ee36-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="1ee36-112">Method</span></span> | <span data-ttu-id="1ee36-113">Description</span><span class="sxs-lookup"><span data-stu-id="1ee36-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="1ee36-114">IDWriteBitmapRenderTarget2::GetBitmapData</span><span class="sxs-lookup"><span data-stu-id="1ee36-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="1ee36-115">Récupère les données de pixels d’une cible de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="1ee36-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="1ee36-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ee36-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1ee36-117">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="1ee36-117">**Minimum supported client**</span></span> | <span data-ttu-id="1ee36-118">Windows 10, projet Réunion 0,1 version préliminaire [applications Win32]</span><span class="sxs-lookup"><span data-stu-id="1ee36-118">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="1ee36-119">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="1ee36-119">**Header**</span></span> | <span data-ttu-id="1ee36-120">dwrite_3. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="1ee36-120">dwrite_3.h (include dwrite_core.h)</span></span> |