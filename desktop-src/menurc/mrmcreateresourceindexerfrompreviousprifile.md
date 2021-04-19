---
title: MrmCreateResourceIndexerFromPreviousPriFile, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir d’un fichier PRI créé à l’aide d’un appel précédent à MrmCreateResourceFile. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousPriFile et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510329"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a><span data-ttu-id="9bebb-105">MrmCreateResourceIndexerFromPreviousPriFile fonction)</span><span class="sxs-lookup"><span data-stu-id="9bebb-105">MrmCreateResourceIndexerFromPreviousPriFile function</span></span>

<span data-ttu-id="9bebb-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="9bebb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bebb-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bebb-108">Crée un indexeur de ressource à partir d’un fichier PRI créé à l’aide d’un appel précédent à [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span><span class="sxs-lookup"><span data-stu-id="9bebb-108">Creates a resource indexer from a PRI file created with a previous call to [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span></span> <span data-ttu-id="9bebb-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="9bebb-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bebb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bebb-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="9bebb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bebb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bebb-112">*projectRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bebb-113">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9bebb-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="9bebb-114">Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="9bebb-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="9bebb-115">En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application.</span><span class="sxs-lookup"><span data-stu-id="9bebb-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="9bebb-116">Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="9bebb-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="9bebb-117">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bebb-118">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="9bebb-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="9bebb-119">Version de la plateforme cible pour l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="9bebb-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="9bebb-120">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9bebb-121">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9bebb-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="9bebb-122">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="9bebb-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="9bebb-123">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="9bebb-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="9bebb-124">*priFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-124">*priFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bebb-125">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9bebb-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="9bebb-126">Chemin d’accès complet à un fichier PRI.</span><span class="sxs-lookup"><span data-stu-id="9bebb-126">A full file path to a PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="9bebb-127">*indexeur* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bebb-128">Tapez : \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="9bebb-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="9bebb-129">Pointeur vers un handle d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="9bebb-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bebb-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9bebb-130">Return value</span></span>

<span data-ttu-id="9bebb-131">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9bebb-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9bebb-132">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="9bebb-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="9bebb-133">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="9bebb-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bebb-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bebb-134">Requirements</span></span>



| <span data-ttu-id="9bebb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bebb-135">Requirement</span></span> | <span data-ttu-id="9bebb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bebb-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bebb-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bebb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9bebb-138">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9bebb-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bebb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9bebb-140">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bebb-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9bebb-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bebb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bebb-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bebb-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="9bebb-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9bebb-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bebb-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bebb-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="9bebb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9bebb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bebb-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bebb-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="9bebb-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bebb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bebb-148">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="9bebb-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

