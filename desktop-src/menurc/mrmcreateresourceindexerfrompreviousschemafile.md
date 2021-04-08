---
title: MrmCreateResourceIndexerFromPreviousSchemaFile, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir d’un fichier de schéma créé à l’aide d’un appel précédent à MrmDumpPriFile. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousSchemaFile et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743053"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="60428-105">MrmCreateResourceIndexerFromPreviousSchemaFile fonction)</span><span class="sxs-lookup"><span data-stu-id="60428-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="60428-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="60428-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="60428-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="60428-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="60428-108">Crée un indexeur de ressource à partir d’un fichier de schéma créé à l’aide d’un appel précédent à [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="60428-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="60428-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="60428-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="60428-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60428-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="60428-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60428-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60428-112">*projectRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60428-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60428-113">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="60428-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="60428-114">Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="60428-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="60428-115">En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application.</span><span class="sxs-lookup"><span data-stu-id="60428-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="60428-116">Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="60428-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="60428-117">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60428-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60428-118">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="60428-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="60428-119">Version de la plateforme cible pour l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="60428-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="60428-120">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="60428-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60428-121">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="60428-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="60428-122">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="60428-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="60428-123">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="60428-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="60428-124">*fichierschéma* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60428-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60428-125">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="60428-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="60428-126">Chemin d’accès complet à un fichier de schéma créé par un appel précédent à [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="60428-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="60428-127">*indexeur* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60428-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60428-128">Tapez : \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="60428-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="60428-129">Pointeur vers un handle d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="60428-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60428-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60428-130">Return value</span></span>

<span data-ttu-id="60428-131">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="60428-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="60428-132">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="60428-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="60428-133">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="60428-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="60428-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60428-134">Requirements</span></span>



| <span data-ttu-id="60428-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60428-135">Requirement</span></span> | <span data-ttu-id="60428-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="60428-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60428-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60428-137">Minimum supported client</span></span><br/> | <span data-ttu-id="60428-138">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60428-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="60428-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60428-139">Minimum supported server</span></span><br/> | <span data-ttu-id="60428-140">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60428-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60428-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="60428-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="60428-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="60428-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="60428-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60428-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="60428-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60428-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="60428-145">DLL</span><span class="sxs-lookup"><span data-stu-id="60428-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60428-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60428-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="60428-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60428-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60428-148">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="60428-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

