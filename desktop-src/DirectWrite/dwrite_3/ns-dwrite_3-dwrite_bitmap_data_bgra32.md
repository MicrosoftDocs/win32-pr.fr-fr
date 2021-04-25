---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Représente des données bitmap au format BGRA32.
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: ad36eb8fe691330b471db0b7e8b5378f3e7614db
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955052"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a><span data-ttu-id="69fe6-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="69fe6-103">DWRITE_BITMAP_DATA_BGRA32 structure (dwrite_3.h)</span></span>

<span data-ttu-id="69fe6-104">Représente des données bitmap au format BGRA32.</span><span class="sxs-lookup"><span data-stu-id="69fe6-104">Represents bitmap data in BGRA32 format.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69fe6-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="69fe6-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="69fe6-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="69fe6-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="69fe6-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="69fe6-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="69fe6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69fe6-108">Syntax</span></span>

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a><span data-ttu-id="69fe6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="69fe6-109">Members</span></span>

`width`

<span data-ttu-id="69fe6-110">Type : **[UInt32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69fe6-110">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69fe6-111">Largeur, en pixels, de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="69fe6-111">The width, in pixels, of the bitmap.</span></span>


`height`

<span data-ttu-id="69fe6-112">Type : **[UInt32](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69fe6-112">Type: **[UINT32](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69fe6-113">Hauteur, en pixels, de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="69fe6-113">The height, in pixels, of the bitmap.</span></span>


`pixels`

<span data-ttu-id="69fe6-114">Type : \_ taille du champ \_ \_ (largeur \* hauteur)**[UInt32](../../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69fe6-114">Type: \_Field\_size\_(width \* height)**[UINT32](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69fe6-115">Pointeur vers l’emplacement des valeurs de bit de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="69fe6-115">A pointer to the location of the bit values for the bitmap.</span></span>


## <a name="examples"></a><span data-ttu-id="69fe6-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="69fe6-116">Examples</span></span>

<span data-ttu-id="69fe6-117">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/directwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="69fe6-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fe6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69fe6-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="69fe6-119">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="69fe6-119">**Minimum supported client**</span></span> | <span data-ttu-id="69fe6-120">Windows 10, réunion de projet (applications Win32)</span><span class="sxs-lookup"><span data-stu-id="69fe6-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="69fe6-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="69fe6-121">**Header**</span></span> | <span data-ttu-id="69fe6-122">dwrite_3. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="69fe6-122">dwrite_3.h (include dwrite_core.h)</span></span> |