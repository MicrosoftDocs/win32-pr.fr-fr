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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "104032280"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="80d77-103">Énumération DWRITE_FACTORY_TYPE (DWRITE. h)</span><span class="sxs-lookup"><span data-stu-id="80d77-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="80d77-104">Spécifie le type d’objet de fabrique DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="80d77-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80d77-105">Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="80d77-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="80d77-106">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="80d77-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="80d77-107">Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="80d77-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="80d77-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80d77-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a><span data-ttu-id="80d77-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="80d77-109">Constants</span></span>

| <span data-ttu-id="80d77-110">Nom</span><span class="sxs-lookup"><span data-stu-id="80d77-110">Name</span></span> | <span data-ttu-id="80d77-111">Description</span><span class="sxs-lookup"><span data-stu-id="80d77-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="80d77-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="80d77-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="80d77-113">Indique que la fabrique DirectWrite est une fabrique partagée et qu’elle permet la réutilisation des données de police mises en cache sur plusieurs composants in-process.</span><span class="sxs-lookup"><span data-stu-id="80d77-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="80d77-114">De telles fabriques tirent également parti des composants de mise en cache des polices inter-processus pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="80d77-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="80d77-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="80d77-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="80d77-116">Indique que l’objet de fabrique DirectWrite est isolé.</span><span class="sxs-lookup"><span data-stu-id="80d77-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="80d77-117">Les objets créés à partir de la fabrique isolée n’interagissent pas avec l’État DirectWrite interne à partir d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="80d77-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="80d77-118">DWRITE_FACTORY_TYPE_RESTRICTED</span><span class="sxs-lookup"><span data-stu-id="80d77-118">DWRITE_FACTORY_TYPE_RESTRICTED</span></span> | <span data-ttu-id="80d77-119">Les objets créés à partir d’une fabrique limitée n’utilisent pas et ne modifient pas l’état interne ni les données mises en cache utilisées par d’autres fabriques.</span><span class="sxs-lookup"><span data-stu-id="80d77-119">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="80d77-120">En outre, la collection de polices système contient uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="80d77-120">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="80d77-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="80d77-121">Examples</span></span>

<span data-ttu-id="80d77-122">Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="80d77-122">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="80d77-123">Notes</span><span class="sxs-lookup"><span data-stu-id="80d77-123">Remarks</span></span>

<span data-ttu-id="80d77-124">Un objet de fabrique DirectWrite contient des informations sur son état interne, telles que l’inscription du chargeur de polices et les données de police mises en cache.</span><span class="sxs-lookup"><span data-stu-id="80d77-124">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="80d77-125">Dans la plupart des cas, vous devez utiliser l’objet de fabrique partagée, car il permet à plusieurs composants qui utilisent DirectWrite de partager des informations d’État DirectWrite internes, réduisant ainsi l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="80d77-125">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="80d77-126">Toutefois, dans certains cas, il est souhaitable de réduire l’impact d’un composant sur le reste du processus, par exemple un plug-in à partir d’une source non fiable, en le sandboxant et en l’isolant du reste des composants de processus.</span><span class="sxs-lookup"><span data-stu-id="80d77-126">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="80d77-127">Dans ce cas, vous devez utiliser une fabrique isolée pour le composant sandbox.</span><span class="sxs-lookup"><span data-stu-id="80d77-127">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="80d77-128">Une fabrique restreinte est plus verrouillée qu’une fabrique isolée.</span><span class="sxs-lookup"><span data-stu-id="80d77-128">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="80d77-129">Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant.</span><span class="sxs-lookup"><span data-stu-id="80d77-129">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="80d77-130">En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="80d77-130">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="80d77-131">Si vous transmettez **DWRITE_FACTORY_TYPE_RESTRICTED** à une version de DWRITE antérieure à DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) retourne **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="80d77-131">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d77-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80d77-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="80d77-133">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="80d77-133">**Minimum supported client**</span></span> | <span data-ttu-id="80d77-134">Windows 10, projet Réunion 0,1 version préliminaire [applications Win32]</span><span class="sxs-lookup"><span data-stu-id="80d77-134">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="80d77-135">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="80d77-135">**Header**</span></span> | <span data-ttu-id="80d77-136">DWrite. h (inclure dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="80d77-136">dwrite.h (include dwrite_core.h)</span></span> |
