---
title: MrmIndexEmbeddedData, fonction (MrmResourceIndexer. h)
description: Indexe une ressource données incorporée unique appartenant à une application UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menus de fonction MrmIndexEmbeddedData et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513762"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="5f5ce-104">MrmIndexEmbeddedData fonction)</span><span class="sxs-lookup"><span data-stu-id="5f5ce-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="5f5ce-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f5ce-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f5ce-107">Indexe une ressource **données incorporée** unique appartenant à une application UWP.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="5f5ce-108">Prend une liste explicite (mais facultative) des qualificateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="5f5ce-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5f5ce-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5ce-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f5ce-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="5f5ce-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f5ce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f5ce-112">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5ce-113">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="5f5ce-114">Handle identifiant l’indexeur de ressource qui indexe le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ce-115">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5ce-116">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="5f5ce-117">URI de ressource à assigner à la ressource.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="5f5ce-118">Le chemin d’accès sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ce-119">*données incorporée* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5ce-120">Type : \**const Byte \** _</span><span class="sxs-lookup"><span data-stu-id="5f5ce-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="5f5ce-121">Pointeur vers les données de la ressource que vous souhaitez indexer.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ce-122">_embeddedDataSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5ce-123">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-123">Type: **ULONG**</span></span>

<span data-ttu-id="5f5ce-124">Taille des données vers lesquelles pointe *données incorporée*.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="5f5ce-125">*qualificateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5ce-126">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="5f5ce-127">Liste facultative de qualificateurs de ressources, par exemple L « language-en-US \_ Scale-100 \_ Contrast-standard ».</span><span class="sxs-lookup"><span data-stu-id="5f5ce-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="5f5ce-128">Une chaîne vide ou **nullptr** indique une ressource neutre.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="5f5ce-129">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f5ce-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f5ce-130">Return value</span></span>

<span data-ttu-id="5f5ce-131">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-131">Type: **HRESULT**</span></span>

<span data-ttu-id="5f5ce-132">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="5f5ce-133">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f5ce-134">Notes</span><span class="sxs-lookup"><span data-stu-id="5f5ce-134">Remarks</span></span>

<span data-ttu-id="5f5ce-135">Si vous souhaitez spécifier des qualificateurs de ressources, transmettez-les dans le paramètre *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="5f5ce-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="5f5ce-136">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="5f5ce-137">Le segment de nom de fichier de *resourceuri* est utilisé comme nom de ressource.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5ce-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f5ce-138">Requirements</span></span>



| <span data-ttu-id="5f5ce-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f5ce-139">Requirement</span></span> | <span data-ttu-id="5f5ce-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f5ce-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5ce-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5ce-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5ce-142">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5f5ce-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f5ce-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5ce-144">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f5ce-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f5ce-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5ce-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5ce-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="5f5ce-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f5ce-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f5ce-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f5ce-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="5f5ce-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5f5ce-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f5ce-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5ce-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5f5ce-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f5ce-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5ce-152">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="5f5ce-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

