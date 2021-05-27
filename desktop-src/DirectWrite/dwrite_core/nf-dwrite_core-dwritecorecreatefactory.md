---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 3ba1b8f6e09212c1ba2f4a0093e2205acaa2e835
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548934"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="3583f-103">DWriteCoreCreateFactory, fonction (dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="3583f-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="3583f-104">Crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.</span><span class="sxs-lookup"><span data-stu-id="3583f-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3583f-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="3583f-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="3583f-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="3583f-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="3583f-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](../dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3583f-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3583f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3583f-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="3583f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3583f-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="3583f-110">Type : <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="3583f-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="3583f-111">Valeur qui spécifie si l’objet de fabrique sera partagé, isolé ou restreint.</span><span class="sxs-lookup"><span data-stu-id="3583f-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="3583f-112">Type : <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="3583f-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="3583f-113">Valeur GUID qui identifie l’interface de fabrique DirectWrite, telle que __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="3583f-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="3583f-114">Type : <b>IUnknown \* \*</b></span><span class="sxs-lookup"><span data-stu-id="3583f-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="3583f-115">Adresse d’un pointeur vers l’objet de fabrique DirectWrite nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="3583f-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="3583f-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3583f-116">Return value</span></span>

<span data-ttu-id="3583f-117">Type : <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="3583f-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="3583f-118">Si cette méthode est réussie, elle retourne <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="3583f-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="3583f-119">Sinon, elle retourne un code d’erreur <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="3583f-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="3583f-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3583f-120">Examples</span></span>

<span data-ttu-id="3583f-121">Consultez la rubrique [vue d’ensemble de DWriteCore](../dwritecore-overview.md) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="3583f-121">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="3583f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="3583f-122">Remarks</span></span>

<span data-ttu-id="3583f-123">Elle fonctionne de la même façon que la fonction [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportée par la version système de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="3583f-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="3583f-124">La fonction DWriteCore a un nom différent pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="3583f-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="3583f-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3583f-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3583f-126">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="3583f-126">**Minimum supported client**</span></span> | <span data-ttu-id="3583f-127">Windows 10, réunion de projet (applications Win32)</span><span class="sxs-lookup"><span data-stu-id="3583f-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="3583f-128">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="3583f-128">**Header**</span></span> | <span data-ttu-id="3583f-129">DWrite. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="3583f-129">dwrite.h (include dwrite_core.h)</span></span> |