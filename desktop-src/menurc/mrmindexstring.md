---
title: MrmIndexString, fonction (MrmResourceIndexer. h)
description: Indexe une ressource de type chaîne unique appartenant à une application UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menus de fonction MrmIndexString et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102989"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="30052-104">MrmIndexString fonction)</span><span class="sxs-lookup"><span data-stu-id="30052-104">MrmIndexString function</span></span>

<span data-ttu-id="30052-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="30052-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="30052-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="30052-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="30052-107">Indexe une ressource de type chaîne unique appartenant à une application UWP.</span><span class="sxs-lookup"><span data-stu-id="30052-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="30052-108">Prend une liste explicite (mais facultative) des qualificateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="30052-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="30052-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="30052-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="30052-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30052-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="30052-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30052-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30052-112">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30052-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30052-113">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="30052-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="30052-114">Handle identifiant l’indexeur de ressource qui indexera les ressources de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="30052-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="30052-115">*resourceuri* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30052-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30052-116">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="30052-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="30052-117">URI de ressource à assigner à la ressource.</span><span class="sxs-lookup"><span data-stu-id="30052-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="30052-118">Le chemin d’accès sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="30052-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="30052-119">*resourceString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30052-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30052-120">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="30052-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="30052-121">Valeur de la ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="30052-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="30052-122">*qualificateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="30052-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="30052-123">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="30052-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="30052-124">Liste facultative de qualificateurs de ressources, par exemple L « language-en-US \_ Scale-100 \_ Contrast-standard ».</span><span class="sxs-lookup"><span data-stu-id="30052-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="30052-125">Une chaîne vide ou **nullptr** indique une ressource neutre.</span><span class="sxs-lookup"><span data-stu-id="30052-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="30052-126">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.</span><span class="sxs-lookup"><span data-stu-id="30052-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30052-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30052-127">Return value</span></span>

<span data-ttu-id="30052-128">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30052-128">Type: **HRESULT**</span></span>

<span data-ttu-id="30052-129">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="30052-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="30052-130">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="30052-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="30052-131">Notes</span><span class="sxs-lookup"><span data-stu-id="30052-131">Remarks</span></span>

<span data-ttu-id="30052-132">Si vous souhaitez spécifier des qualificateurs de ressources, transmettez-les dans le paramètre *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="30052-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="30052-133">Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.</span><span class="sxs-lookup"><span data-stu-id="30052-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="30052-134">Le segment de nom de fichier de *resourceuri* est utilisé comme nom de ressource.</span><span class="sxs-lookup"><span data-stu-id="30052-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="30052-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30052-135">Requirements</span></span>



| <span data-ttu-id="30052-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30052-136">Requirement</span></span> | <span data-ttu-id="30052-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="30052-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30052-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30052-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30052-139">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30052-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30052-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30052-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30052-141">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30052-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30052-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="30052-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="30052-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="30052-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="30052-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30052-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="30052-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30052-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="30052-146">DLL</span><span class="sxs-lookup"><span data-stu-id="30052-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30052-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30052-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="30052-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30052-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30052-149">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="30052-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

