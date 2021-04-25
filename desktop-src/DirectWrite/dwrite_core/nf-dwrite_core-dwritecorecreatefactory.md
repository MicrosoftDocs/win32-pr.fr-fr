---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core. h)
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
ms.openlocfilehash: 43e43e00385e10f0da0ba459cdc16e84562b72ec
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955022"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="fa044-103">DWriteCoreCreateFactory, fonction (dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="fa044-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="fa044-104">Crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.</span><span class="sxs-lookup"><span data-stu-id="fa044-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa044-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fa044-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="fa044-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="fa044-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="fa044-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="fa044-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa044-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa044-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="fa044-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa044-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="fa044-110">Type : <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="fa044-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="fa044-111">Valeur qui spécifie si l’objet de fabrique sera partagé, isolé ou restreint.</span><span class="sxs-lookup"><span data-stu-id="fa044-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="fa044-112">Type : <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="fa044-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="fa044-113">Valeur GUID qui identifie l’interface de fabrique DirectWrite, telle que __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="fa044-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="fa044-114">Type : <b>IUnknown \* \*</b></span><span class="sxs-lookup"><span data-stu-id="fa044-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="fa044-115">Adresse d’un pointeur vers l’objet de fabrique DirectWrite nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="fa044-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa044-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa044-116">Return value</span></span>

<span data-ttu-id="fa044-117">Type : <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="fa044-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="fa044-118">Si cette méthode est réussie, elle retourne <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="fa044-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="fa044-119">Sinon, elle retourne un code d’erreur <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="fa044-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="fa044-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="fa044-120">Examples</span></span>

<span data-ttu-id="fa044-121">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/directwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="fa044-121">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa044-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa044-122">Remarks</span></span>

<span data-ttu-id="fa044-123">Elle fonctionne de la même façon que la fonction [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportée par la version système de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="fa044-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="fa044-124">La fonction DWriteCore a un nom différent pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="fa044-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa044-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa044-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fa044-126">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="fa044-126">**Minimum supported client**</span></span> | <span data-ttu-id="fa044-127">Windows 10, réunion de projet (applications Win32)</span><span class="sxs-lookup"><span data-stu-id="fa044-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="fa044-128">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="fa044-128">**Header**</span></span> | <span data-ttu-id="fa044-129">DWrite. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="fa044-129">dwrite.h (include dwrite_core.h)</span></span> |
