---
title: MrmIndexFile, fonction (MrmResourceIndexer. h)
description: Indexe un fichier de ressources appartenant à une application UWP. Prend une liste explicite (mais facultative) des qualificateurs de ressources. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menus de fonction MrmIndexFile et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466594"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="26e20-106">MrmIndexFile fonction)</span><span class="sxs-lookup"><span data-stu-id="26e20-106">MrmIndexFile function</span></span>

<span data-ttu-id="26e20-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="26e20-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26e20-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="26e20-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26e20-109">Indexe un fichier de ressources appartenant à une application UWP.</span><span class="sxs-lookup"><span data-stu-id="26e20-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="26e20-110">Prend une liste explicite (mais facultative) des qualificateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="26e20-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="26e20-111">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="26e20-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="26e20-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26e20-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="26e20-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26e20-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e20-114">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e20-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e20-115">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="26e20-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="26e20-116">Handle identifiant l’indexeur de ressource qui indexe le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="26e20-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="26e20-117">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e20-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e20-118">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="26e20-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="26e20-119">URI de ressource à assigner à la ressource.</span><span class="sxs-lookup"><span data-stu-id="26e20-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="26e20-120">Le chemin d’accès sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="26e20-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="26e20-121">*filePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26e20-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e20-122">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="26e20-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="26e20-123">Chemin d’accès relatif à un fichier contenant une ressource que vous souhaitez indexer.</span><span class="sxs-lookup"><span data-stu-id="26e20-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="26e20-124">Ce chemin d’accès est relatif à la racine du projet de l’application UWP pour laquelle vous générez des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="26e20-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="26e20-125">La racine du projet est la valeur de *projectRoot* que vous avez passée à [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="26e20-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="26e20-126">*qualificateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26e20-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26e20-127">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="26e20-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="26e20-128">Liste facultative de qualificateurs de ressources, par exemple L « language-en-US \_ Scale-100 \_ Contrast-standard ».</span><span class="sxs-lookup"><span data-stu-id="26e20-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="26e20-129">Une chaîne vide ou **nullptr** indique une ressource neutre.</span><span class="sxs-lookup"><span data-stu-id="26e20-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="26e20-130">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri* ou de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="26e20-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e20-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26e20-131">Return value</span></span>

<span data-ttu-id="26e20-132">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26e20-132">Type: **HRESULT**</span></span>

<span data-ttu-id="26e20-133">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="26e20-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="26e20-134">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="26e20-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e20-135">Notes</span><span class="sxs-lookup"><span data-stu-id="26e20-135">Remarks</span></span>

<span data-ttu-id="26e20-136">Si vous souhaitez spécifier des qualificateurs de ressources, transmettez-les dans le paramètre *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="26e20-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="26e20-137">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri* ni de *filePath*.</span><span class="sxs-lookup"><span data-stu-id="26e20-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="26e20-138">Le segment de nom de fichier de *resourceuri* (non *filePath*) est utilisé comme nom de ressource.</span><span class="sxs-lookup"><span data-stu-id="26e20-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e20-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26e20-139">Requirements</span></span>



| <span data-ttu-id="26e20-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26e20-140">Requirement</span></span> | <span data-ttu-id="26e20-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="26e20-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e20-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e20-142">Minimum supported client</span></span><br/> | <span data-ttu-id="26e20-143">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e20-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="26e20-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26e20-144">Minimum supported server</span></span><br/> | <span data-ttu-id="26e20-145">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26e20-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26e20-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="26e20-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e20-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e20-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="26e20-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26e20-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="26e20-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26e20-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="26e20-150">DLL</span><span class="sxs-lookup"><span data-stu-id="26e20-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26e20-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e20-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="26e20-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26e20-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e20-153">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="26e20-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

