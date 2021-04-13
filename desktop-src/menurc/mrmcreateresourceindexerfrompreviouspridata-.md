---
title: MrmCreateResourceIndexerFromPreviousPriData, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir de données PRI créées par un appel précédent à MrmCreateResourceFileInMemory. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousPriData et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317381"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="bc6dc-105">MrmCreateResourceIndexerFromPreviousPriData fonction)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="bc6dc-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc6dc-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc6dc-108">Crée un indexeur de ressource à partir de données PRI créées par un appel précédent à [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="bc6dc-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6dc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc6dc-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="bc6dc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc6dc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6dc-112">*projectRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-113">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bc6dc-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="bc6dc-114">Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="bc6dc-115">En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="bc6dc-116">Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="bc6dc-117">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-118">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="bc6dc-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="bc6dc-119">Version de la plateforme cible pour l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="bc6dc-120">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-121">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bc6dc-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="bc6dc-122">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="bc6dc-123">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="bc6dc-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="bc6dc-124">*priData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-125">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="bc6dc-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="bc6dc-126">Pointeur vers les données PRI créées par un appel précédent à [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="bc6dc-127">Ne libérez pas *priData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="bc6dc-128">Pris en  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-129">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="bc6dc-129">Type: **ULONG**</span></span>

<span data-ttu-id="bc6dc-130">Taille des données vers lesquelles pointe *priData*.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="bc6dc-131">*indexeur* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6dc-132">Tapez : \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="bc6dc-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="bc6dc-133">Pointeur vers un handle d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6dc-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc6dc-134">Return value</span></span>

<span data-ttu-id="bc6dc-135">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="bc6dc-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="bc6dc-136">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="bc6dc-137">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc6dc-138">Notes</span><span class="sxs-lookup"><span data-stu-id="bc6dc-138">Remarks</span></span>

<span data-ttu-id="bc6dc-139">Ne libérez pas *priData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6dc-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc6dc-140">Requirements</span></span>



| <span data-ttu-id="bc6dc-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc6dc-141">Requirement</span></span> | <span data-ttu-id="bc6dc-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc6dc-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc6dc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bc6dc-144">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bc6dc-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc6dc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bc6dc-146">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc6dc-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc6dc-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc6dc-148"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc6dc-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="bc6dc-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc6dc-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc6dc-150"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc6dc-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="bc6dc-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bc6dc-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc6dc-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc6dc-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bc6dc-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc6dc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6dc-154">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="bc6dc-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

