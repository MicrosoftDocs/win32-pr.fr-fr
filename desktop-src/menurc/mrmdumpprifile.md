---
title: MrmDumpPriFile, fonction (MrmResourceIndexer. h)
description: Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (sous forme de fichier sur le disque), afin de le rendre plus facile à lire.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menus de fonction MrmDumpPriFile et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741828"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="154fa-104">MrmDumpPriFile fonction)</span><span class="sxs-lookup"><span data-stu-id="154fa-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="154fa-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="154fa-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="154fa-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="154fa-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="154fa-107">Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (sous forme de fichier sur le disque), afin de le rendre plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="154fa-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="154fa-108">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="154fa-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="154fa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="154fa-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="154fa-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="154fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="154fa-111">*indexFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="154fa-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="154fa-112">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="154fa-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="154fa-113">Chemin d’accès complet à un fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="154fa-113">A full file path to a PRI file.</span></span> <span data-ttu-id="154fa-114">Il s’agit du fichier PRI qui sera vidé au format XML.</span><span class="sxs-lookup"><span data-stu-id="154fa-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="154fa-115">*schemaPriFile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="154fa-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="154fa-116">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="154fa-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="154fa-117">Chemin de fichier complet facultatif d’un fichier de schéma (ou d’un fichier PRI représentant un schéma ; consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="154fa-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="154fa-118">*dumpType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="154fa-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="154fa-119">Type : **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="154fa-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="154fa-120">Spécifie le degré de détail de la sauvegarde XML, ou si un schéma doit être vidé.</span><span class="sxs-lookup"><span data-stu-id="154fa-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="154fa-121">*outputXmlFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="154fa-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="154fa-122">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="154fa-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="154fa-123">Chemin d’accès d’un fichier XML à créer.</span><span class="sxs-lookup"><span data-stu-id="154fa-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="154fa-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="154fa-124">Return value</span></span>

<span data-ttu-id="154fa-125">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="154fa-125">Type: **HRESULT**</span></span>

<span data-ttu-id="154fa-126">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="154fa-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="154fa-127">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="154fa-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="154fa-128">Notes</span><span class="sxs-lookup"><span data-stu-id="154fa-128">Remarks</span></span>

<span data-ttu-id="154fa-129">Un pack de ressources sans schéma est un pack créé avec l’argument [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passé à [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou avec le commutateur *omitSchemaFromResourcePacks* dans le fichier de configuration PRI).</span><span class="sxs-lookup"><span data-stu-id="154fa-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="154fa-130">Pour vider un pack de ressources sans schéma, transmettez le chemin d’accès à vos données PRI de package principal en tant qu’argument pour le paramètre *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="154fa-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="154fa-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="154fa-131">Requirements</span></span>



| <span data-ttu-id="154fa-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="154fa-132">Requirement</span></span> | <span data-ttu-id="154fa-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="154fa-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="154fa-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="154fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="154fa-135">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="154fa-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="154fa-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="154fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="154fa-137">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="154fa-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="154fa-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="154fa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="154fa-139"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="154fa-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="154fa-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="154fa-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="154fa-141"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="154fa-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="154fa-142">DLL</span><span class="sxs-lookup"><span data-stu-id="154fa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="154fa-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="154fa-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="154fa-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="154fa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154fa-145">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="154fa-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

