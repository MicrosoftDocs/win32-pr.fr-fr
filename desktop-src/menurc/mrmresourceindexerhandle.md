---
title: MrmResourceIndexerHandle, structure (MrmResourceIndexer. h)
description: Représente un handle opaque d’un objet indexeur de ressource. Le handle est géré par le système d’exploitation. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menus de la structure MrmResourceIndexerHandle et autres ressources
- Menus du pointeur de structure PMrmResourceIndexerHandle et autres ressources
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385251"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="070ab-107">MrmResourceIndexerHandle, structure</span><span class="sxs-lookup"><span data-stu-id="070ab-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="070ab-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="070ab-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="070ab-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="070ab-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="070ab-110">Représente un handle opaque d’un objet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="070ab-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="070ab-111">Le handle est géré par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="070ab-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="070ab-112">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="070ab-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="070ab-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="070ab-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="070ab-114">Membres</span><span class="sxs-lookup"><span data-stu-id="070ab-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="070ab-115">**traitée**</span><span class="sxs-lookup"><span data-stu-id="070ab-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="070ab-116">Type : **pVoid**</span><span class="sxs-lookup"><span data-stu-id="070ab-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="070ab-117">Handle opaque vers un objet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="070ab-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="070ab-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="070ab-118">Requirements</span></span>



| <span data-ttu-id="070ab-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="070ab-119">Requirement</span></span> | <span data-ttu-id="070ab-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="070ab-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070ab-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="070ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="070ab-122">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="070ab-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="070ab-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="070ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="070ab-124">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="070ab-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="070ab-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="070ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="070ab-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="070ab-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="070ab-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="070ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070ab-128">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="070ab-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

