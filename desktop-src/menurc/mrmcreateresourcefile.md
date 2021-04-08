---
title: MrmCreateResourceFile, fonction (MrmResourceIndexer. h)
description: Crée un fichier PRI (nommé \ 0034 ; Resources. pri \ 0034 ;), ou des fichiers, sur le disque dans le dossier spécifié. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menus de fonction MrmCreateResourceFile et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743061"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="21d18-105">MrmCreateResourceFile fonction)</span><span class="sxs-lookup"><span data-stu-id="21d18-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="21d18-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="21d18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="21d18-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="21d18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="21d18-108">Crée un fichier PRI (nommé « Resources. PRI ») ou des fichiers sur le disque dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="21d18-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="21d18-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="21d18-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="21d18-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21d18-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="21d18-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21d18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21d18-112">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21d18-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d18-113">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="21d18-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="21d18-114">Handle identifiant l’indexeur de ressource à partir duquel créer le fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="21d18-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="21d18-115">*packagingMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21d18-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d18-116">Type : **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="21d18-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="21d18-117">Spécifie si le fichier PRI doit être autonome, être fractionné automatiquement par qualificateur de ressource ou être un pack de ressources.</span><span class="sxs-lookup"><span data-stu-id="21d18-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="21d18-118">*packagingOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21d18-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21d18-119">Type : **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="21d18-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="21d18-120">Spécifie des options supplémentaires sur le fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="21d18-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="21d18-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="21d18-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="21d18-122">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="21d18-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="21d18-123">Chemin d’accès à un dossier dans lequel enregistrer le fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="21d18-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21d18-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21d18-124">Return value</span></span>

<span data-ttu-id="21d18-125">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21d18-125">Type: **HRESULT**</span></span>

<span data-ttu-id="21d18-126">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="21d18-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="21d18-127">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="21d18-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d18-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21d18-128">Requirements</span></span>



| <span data-ttu-id="21d18-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21d18-129">Requirement</span></span> | <span data-ttu-id="21d18-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="21d18-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d18-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21d18-131">Minimum supported client</span></span><br/> | <span data-ttu-id="21d18-132">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21d18-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="21d18-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21d18-133">Minimum supported server</span></span><br/> | <span data-ttu-id="21d18-134">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21d18-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21d18-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="21d18-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="21d18-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="21d18-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="21d18-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21d18-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="21d18-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21d18-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="21d18-139">DLL</span><span class="sxs-lookup"><span data-stu-id="21d18-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21d18-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21d18-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="21d18-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21d18-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d18-142">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="21d18-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

