---
title: MrmDumpPriFileInMemory, fonction (MrmResourceIndexer. h)
description: Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menus de fonction MrmDumpPriFileInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510303"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="7dc1e-104">MrmDumpPriFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="7dc1e-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="7dc1e-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7dc1e-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7dc1e-107">Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="7dc1e-108">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="7dc1e-109">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="7dc1e-110">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="7dc1e-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc1e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dc1e-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="7dc1e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dc1e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc1e-113">*indexFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc1e-114">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7dc1e-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="7dc1e-115">Chemin d’accès complet à un fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-115">A full file path to a PRI file.</span></span> <span data-ttu-id="7dc1e-116">Il s’agit du fichier PRI qui sera vidé au format XML.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="7dc1e-117">*schemaPriFile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc1e-118">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7dc1e-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="7dc1e-119">Chemin de fichier complet facultatif d’un fichier de schéma (ou d’un fichier PRI représentant un schéma ; consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="7dc1e-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="7dc1e-120">*dumpType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc1e-121">Type : **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="7dc1e-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="7dc1e-122">Spécifie le degré de détail de la sauvegarde XML, ou si un schéma doit être vidé.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="7dc1e-123">*outputXmlData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc1e-124">Type : **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="7dc1e-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="7dc1e-125">Adresse d’un pointeur vers l’octet.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="7dc1e-126">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="7dc1e-127">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="7dc1e-128">*outputXmlSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc1e-129">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="7dc1e-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="7dc1e-130">Adresse d’un ULONG.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-130">The address of a ULONG.</span></span> <span data-ttu-id="7dc1e-131">Dans _outputXmlSize \*, la fonction retourne la taille de la mémoire allouée appelée par *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc1e-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dc1e-132">Return value</span></span>

<span data-ttu-id="7dc1e-133">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7dc1e-133">Type: **HRESULT**</span></span>

<span data-ttu-id="7dc1e-134">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7dc1e-135">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="7dc1e-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc1e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="7dc1e-136">Remarks</span></span>

<span data-ttu-id="7dc1e-137">Un pack de ressources sans schéma est un pack créé avec l’argument [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passé à [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou avec le commutateur *omitSchemaFromResourcePacks* dans le fichier de configuration PRI).</span><span class="sxs-lookup"><span data-stu-id="7dc1e-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="7dc1e-138">Pour vider un pack de ressources sans schéma, transmettez le chemin d’accès à vos données PRI de package principal en tant qu’argument pour le paramètre *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="7dc1e-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc1e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dc1e-139">Requirements</span></span>



| <span data-ttu-id="7dc1e-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dc1e-140">Requirement</span></span> | <span data-ttu-id="7dc1e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dc1e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc1e-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc1e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc1e-143">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7dc1e-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc1e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc1e-145">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc1e-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7dc1e-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dc1e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc1e-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc1e-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7dc1e-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7dc1e-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="7dc1e-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dc1e-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7dc1e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7dc1e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dc1e-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dc1e-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7dc1e-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dc1e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc1e-153">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="7dc1e-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

