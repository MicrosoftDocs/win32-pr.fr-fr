---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Spécifie le type d’objet de fabrique DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881808"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="32667-103">Énumération DWRITE_FACTORY_TYPE (DWRITE. h)</span><span class="sxs-lookup"><span data-stu-id="32667-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="32667-104">Spécifie le type d’objet de fabrique DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="32667-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32667-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="32667-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="32667-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="32667-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="32667-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="32667-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="32667-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32667-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="32667-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="32667-109">Constants</span></span>

| <span data-ttu-id="32667-110">Nom</span><span class="sxs-lookup"><span data-stu-id="32667-110">Name</span></span> | <span data-ttu-id="32667-111">Description</span><span class="sxs-lookup"><span data-stu-id="32667-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="32667-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="32667-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="32667-113">Indique que la fabrique DirectWrite est une fabrique partagée et qu’elle permet la réutilisation des données de police mises en cache sur plusieurs composants in-process.</span><span class="sxs-lookup"><span data-stu-id="32667-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="32667-114">De telles fabriques tirent également parti des composants de mise en cache des polices inter-processus pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="32667-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="32667-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="32667-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="32667-116">Indique que l’objet de fabrique DirectWrite est isolé.</span><span class="sxs-lookup"><span data-stu-id="32667-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="32667-117">Les objets créés à partir de la fabrique isolée n’interagissent pas avec l’État DirectWrite interne à partir d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="32667-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="32667-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="32667-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="32667-119">Indique que l’objet de fabrique DirectWrite est limité.</span><span class="sxs-lookup"><span data-stu-id="32667-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="32667-120">Les objets créés à partir d’une fabrique limitée n’utilisent pas et ne modifient pas l’état interne ni les données mises en cache utilisées par d’autres fabriques.</span><span class="sxs-lookup"><span data-stu-id="32667-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="32667-121">En outre, la collection de polices système contient uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="32667-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="32667-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="32667-122">Examples</span></span>

<span data-ttu-id="32667-123">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="32667-123">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="32667-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="32667-124">Remarks</span></span>

<span data-ttu-id="32667-125">Un objet de fabrique DirectWrite contient des informations sur son état interne, telles que l’inscription du chargeur de polices et les données de police mises en cache.</span><span class="sxs-lookup"><span data-stu-id="32667-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="32667-126">Dans la plupart des cas, vous devez utiliser l’objet de fabrique partagée, car il permet à plusieurs composants qui utilisent DirectWrite de partager des informations d’État DirectWrite internes, réduisant ainsi l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="32667-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="32667-127">Toutefois, dans certains cas, il est souhaitable de réduire l’impact d’un composant sur le reste du processus, par exemple un plug-in à partir d’une source non fiable, en le sandboxant et en l’isolant du reste des composants de processus.</span><span class="sxs-lookup"><span data-stu-id="32667-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="32667-128">Dans ce cas, vous devez utiliser une fabrique isolée pour le composant sandbox.</span><span class="sxs-lookup"><span data-stu-id="32667-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="32667-129">Une fabrique restreinte est plus verrouillée qu’une fabrique isolée.</span><span class="sxs-lookup"><span data-stu-id="32667-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="32667-130">Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant.</span><span class="sxs-lookup"><span data-stu-id="32667-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="32667-131">En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="32667-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="32667-132">Si vous transmettez **DWRITE_FACTORY_TYPE_ISOLATED2** à une version de DWRITE antérieure à DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) retourne **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="32667-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="32667-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32667-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="32667-134">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="32667-134">**Minimum supported client**</span></span> | <span data-ttu-id="32667-135">Windows 10, réunion de projet (applications Win32)</span><span class="sxs-lookup"><span data-stu-id="32667-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="32667-136">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="32667-136">**Header**</span></span> | <span data-ttu-id="32667-137">DWrite. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="32667-137">dwrite.h (include dwrite_core.h)</span></span> |
