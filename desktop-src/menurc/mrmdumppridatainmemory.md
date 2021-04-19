---
title: MrmDumpPriDataInMemory, fonction (MrmResourceIndexer. h)
description: Vide les informations PRI (en tant qu’objet BLOB en mémoire, créées par un appel précédent à MrmCreateResourceFileInMemory) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menus de fonction MrmDumpPriDataInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510773"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="858f1-104">MrmDumpPriDataInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="858f1-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="858f1-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="858f1-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="858f1-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="858f1-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="858f1-107">Vide les informations PRI (en tant qu’objet BLOB en mémoire, créées par un appel précédent à [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="858f1-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="858f1-108">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="858f1-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="858f1-109">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="858f1-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="858f1-110">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="858f1-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="858f1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="858f1-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="858f1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="858f1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858f1-113">*inputPriData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="858f1-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-114">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="858f1-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="858f1-115">Pointeur vers les données PRI créées par un appel précédent à [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="858f1-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="858f1-116">*inputPriSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="858f1-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-117">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="858f1-117">Type: **ULONG**</span></span>

<span data-ttu-id="858f1-118">Taille des données vers lesquelles pointe *inputPriData*.</span><span class="sxs-lookup"><span data-stu-id="858f1-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="858f1-119">*schemaPriData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="858f1-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-120">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="858f1-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="858f1-121">Pointeur facultatif vers les informations PRI (en tant qu’objet BLOB en mémoire) représentant les données de schéma créées par un appel précédent à [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="858f1-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="858f1-122">Ne libérez pas *schemaPriData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="858f1-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="858f1-123">Consultez également la section Notes.</span><span class="sxs-lookup"><span data-stu-id="858f1-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="858f1-124">*schemaPriSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="858f1-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-125">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="858f1-125">Type: **ULONG**</span></span>

<span data-ttu-id="858f1-126">Taille des données vers lesquelles pointe *schemaPriData*.</span><span class="sxs-lookup"><span data-stu-id="858f1-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="858f1-127">*dumpType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="858f1-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-128">Type : **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="858f1-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="858f1-129">Spécifie le degré de détail de la sauvegarde XML, ou si un schéma doit être vidé.</span><span class="sxs-lookup"><span data-stu-id="858f1-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="858f1-130">*outputXmlData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="858f1-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-131">Type : **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="858f1-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="858f1-132">Adresse d’un pointeur vers l’octet.</span><span class="sxs-lookup"><span data-stu-id="858f1-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="858f1-133">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="858f1-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="858f1-134">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="858f1-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="858f1-135">*outputXmlSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="858f1-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="858f1-136">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="858f1-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="858f1-137">Adresse d’un ULONG.</span><span class="sxs-lookup"><span data-stu-id="858f1-137">The address of a ULONG.</span></span> <span data-ttu-id="858f1-138">Dans _outputXmlSize \*, la fonction retourne la taille de la mémoire allouée appelée par *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="858f1-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="858f1-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="858f1-139">Return value</span></span>

<span data-ttu-id="858f1-140">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="858f1-140">Type: **HRESULT**</span></span>

<span data-ttu-id="858f1-141">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="858f1-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="858f1-142">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="858f1-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="858f1-143">Notes</span><span class="sxs-lookup"><span data-stu-id="858f1-143">Remarks</span></span>

<span data-ttu-id="858f1-144">Un pack de ressources sans schéma est un pack créé avec l’argument [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passé à [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou avec le commutateur *omitSchemaFromResourcePacks* dans le fichier de configuration PRI).</span><span class="sxs-lookup"><span data-stu-id="858f1-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="858f1-145">Pour vider un pack de ressources sans schéma, transmettez le chemin d’accès à vos données PRI de package principal en tant qu’argument pour le paramètre *schemaPriData* .</span><span class="sxs-lookup"><span data-stu-id="858f1-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="858f1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="858f1-146">Requirements</span></span>



| <span data-ttu-id="858f1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="858f1-147">Requirement</span></span> | <span data-ttu-id="858f1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="858f1-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="858f1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="858f1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="858f1-150">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="858f1-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="858f1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="858f1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="858f1-152">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="858f1-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="858f1-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="858f1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="858f1-154"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="858f1-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="858f1-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="858f1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="858f1-156"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="858f1-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="858f1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="858f1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="858f1-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858f1-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="858f1-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="858f1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858f1-160">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="858f1-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

