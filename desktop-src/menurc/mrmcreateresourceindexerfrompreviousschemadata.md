---
title: MrmCreateResourceIndexerFromPreviousSchemaData, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir de données de schéma en mémoire créées à l’aide d’un appel précédent à MrmDumpPriFileInMemory ou MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousSchemaData et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465599"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="69367-104">MrmCreateResourceIndexerFromPreviousSchemaData fonction)</span><span class="sxs-lookup"><span data-stu-id="69367-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="69367-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="69367-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="69367-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="69367-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="69367-107">Crée un indexeur de ressource à partir de données de schéma en mémoire créées à l’aide d’un appel précédent à [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="69367-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="69367-108">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="69367-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="69367-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69367-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="69367-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69367-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69367-111">*projectRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69367-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-112">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="69367-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="69367-113">Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="69367-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="69367-114">En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application.</span><span class="sxs-lookup"><span data-stu-id="69367-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="69367-115">Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="69367-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="69367-116">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69367-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-117">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="69367-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="69367-118">Version de la plateforme cible pour l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="69367-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="69367-119">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69367-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-120">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="69367-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="69367-121">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="69367-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="69367-122">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="69367-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="69367-123">*schemaXmlData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69367-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-124">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="69367-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="69367-125">Pointeur vers les données de schéma créées par un appel précédent à [_ *MrmDumpPriFileInMemory* \*](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="69367-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="69367-126">Ne libérez pas *schemaXmlData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="69367-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="69367-127">*schemaXmlSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69367-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-128">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="69367-128">Type: **ULONG**</span></span>

<span data-ttu-id="69367-129">Taille des données vers lesquelles pointe *schemaXmlData*.</span><span class="sxs-lookup"><span data-stu-id="69367-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="69367-130">*indexeur* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69367-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69367-131">Tapez : \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="69367-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="69367-132">Pointeur vers un handle d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="69367-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69367-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69367-133">Return value</span></span>

<span data-ttu-id="69367-134">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="69367-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="69367-135">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="69367-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="69367-136">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="69367-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="69367-137">Notes</span><span class="sxs-lookup"><span data-stu-id="69367-137">Remarks</span></span>

<span data-ttu-id="69367-138">Ne libérez pas *schemaXmlData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="69367-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="69367-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69367-139">Requirements</span></span>



| <span data-ttu-id="69367-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69367-140">Requirement</span></span> | <span data-ttu-id="69367-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="69367-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69367-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69367-142">Minimum supported client</span></span><br/> | <span data-ttu-id="69367-143">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69367-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="69367-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69367-144">Minimum supported server</span></span><br/> | <span data-ttu-id="69367-145">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69367-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69367-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="69367-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="69367-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="69367-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="69367-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69367-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="69367-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69367-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="69367-150">DLL</span><span class="sxs-lookup"><span data-stu-id="69367-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69367-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69367-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="69367-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69367-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69367-153">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="69367-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

