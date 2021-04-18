---
title: MrmFreeMemory, fonction (MrmResourceIndexer. h)
description: Libère de la mémoire allouée par MrmCreateConfigInMemory, MrmCreateResourceFileInMemory, MrmDumpPriFileInMemory et MrmDumpPriDataInMemory.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Menus de fonction MrmFreeMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512417"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="c80f5-104">MrmFreeMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="c80f5-104">MrmFreeMemory function</span></span>

<span data-ttu-id="c80f5-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c80f5-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c80f5-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c80f5-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c80f5-107">Libère de la mémoire allouée par [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)et [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c80f5-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="c80f5-108">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="c80f5-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="c80f5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c80f5-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="c80f5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c80f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c80f5-111">*données* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c80f5-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c80f5-112">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="c80f5-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="c80f5-113">Pointeur vers la mémoire allouée et retournée par [_ *MrmCreateConfigInMemory* \*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c80f5-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c80f5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c80f5-114">Return value</span></span>

<span data-ttu-id="c80f5-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c80f5-115">Type: **HRESULT**</span></span>

<span data-ttu-id="c80f5-116">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="c80f5-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="c80f5-117">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="c80f5-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c80f5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c80f5-118">Requirements</span></span>



| <span data-ttu-id="c80f5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c80f5-119">Requirement</span></span> | <span data-ttu-id="c80f5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c80f5-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80f5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c80f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c80f5-122">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c80f5-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c80f5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c80f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c80f5-124">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c80f5-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c80f5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c80f5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c80f5-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c80f5-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="c80f5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c80f5-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c80f5-128"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c80f5-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="c80f5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c80f5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c80f5-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c80f5-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c80f5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c80f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80f5-132">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="c80f5-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

