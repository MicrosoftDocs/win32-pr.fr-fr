---
title: MrmCreateResourceFileInMemory, fonction (MrmResourceIndexer. h)
description: Crée des informations PRI en tant qu’objet BLOB en mémoire, et non en tant que fichier sur le disque.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menus de fonction MrmCreateResourceFileInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466598"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="f5a47-104">MrmCreateResourceFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="f5a47-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="f5a47-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f5a47-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f5a47-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f5a47-107">Crée des informations PRI en tant qu’objet BLOB en mémoire, et non en tant que fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="f5a47-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="f5a47-108">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="f5a47-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="f5a47-109">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f5a47-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="f5a47-110">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="f5a47-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a47-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5a47-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="f5a47-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5a47-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a47-113">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a47-114">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a47-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="f5a47-115">Handle identifiant l’indexeur de ressource à partir duquel créer les informations PRI.</span><span class="sxs-lookup"><span data-stu-id="f5a47-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="f5a47-116">*packagingMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a47-117">Type : **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a47-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="f5a47-118">Spécifie si les informations PRI doivent être autonomes ou être un pack de ressources.</span><span class="sxs-lookup"><span data-stu-id="f5a47-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="f5a47-119">**MrmPackagingModeAutoSplit** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f5a47-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f5a47-120">*packagingOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a47-121">Type : **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="f5a47-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="f5a47-122">Spécifie des options supplémentaires sur les informations PRI.</span><span class="sxs-lookup"><span data-stu-id="f5a47-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="f5a47-123">*outputPriData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a47-124">Type : **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="f5a47-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="f5a47-125">Adresse d’un pointeur vers l’octet.</span><span class="sxs-lookup"><span data-stu-id="f5a47-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="f5a47-126">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="f5a47-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="f5a47-127">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="f5a47-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="f5a47-128">*outputPriSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a47-129">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="f5a47-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f5a47-130">Adresse d’un ULONG.</span><span class="sxs-lookup"><span data-stu-id="f5a47-130">The address of a ULONG.</span></span> <span data-ttu-id="f5a47-131">Dans _outputPriSize \*, la fonction retourne la taille de la mémoire allouée appelée par *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="f5a47-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a47-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5a47-132">Return value</span></span>

<span data-ttu-id="f5a47-133">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5a47-133">Type: **HRESULT**</span></span>

<span data-ttu-id="f5a47-134">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="f5a47-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="f5a47-135">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="f5a47-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a47-136">Notes</span><span class="sxs-lookup"><span data-stu-id="f5a47-136">Remarks</span></span>

<span data-ttu-id="f5a47-137">Si vous transmettez *outputPriData* à [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), ne libérez pas la mémoire tant que vous n’avez pas fini d’utiliser l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="f5a47-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a47-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a47-138">Requirements</span></span>



| <span data-ttu-id="f5a47-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a47-139">Requirement</span></span> | <span data-ttu-id="f5a47-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a47-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a47-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5a47-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a47-142">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f5a47-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5a47-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a47-144">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5a47-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5a47-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5a47-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a47-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a47-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="f5a47-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5a47-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5a47-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a47-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="f5a47-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a47-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a47-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a47-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f5a47-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a47-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a47-152">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="f5a47-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

