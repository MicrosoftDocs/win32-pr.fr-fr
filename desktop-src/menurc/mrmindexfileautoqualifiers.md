---
title: MrmIndexFileAutoQualifiers, fonction (MrmResourceIndexer. h)
description: Indexe un fichier de ressources appartenant à une application UWP. Déduit une liste de qualificateurs de ressources à partir du paramètre filePath. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menus de fonction MrmIndexFileAutoQualifiers et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102992"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="5b7cd-106">MrmIndexFileAutoQualifiers fonction)</span><span class="sxs-lookup"><span data-stu-id="5b7cd-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="5b7cd-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5b7cd-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5b7cd-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5b7cd-109">Indexe un fichier de ressources appartenant à une application UWP.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="5b7cd-110">Déduit une liste de qualificateurs de ressources à partir du paramètre *filePath* .</span><span class="sxs-lookup"><span data-stu-id="5b7cd-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="5b7cd-111">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5b7cd-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7cd-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b7cd-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="5b7cd-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b7cd-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b7cd-114">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b7cd-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b7cd-115">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="5b7cd-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="5b7cd-116">Handle identifiant l’indexeur de ressource qui indexe le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="5b7cd-117">*filePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b7cd-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b7cd-118">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="5b7cd-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="5b7cd-119">Chemin d’accès relatif à un fichier contenant une ressource que vous souhaitez indexer.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="5b7cd-120">Ce chemin d’accès est relatif à la racine du projet de l’application UWP pour laquelle vous générez des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="5b7cd-121">La racine du projet est la valeur de *projectRoot* que vous avez passée à [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="5b7cd-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b7cd-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b7cd-122">Return value</span></span>

<span data-ttu-id="5b7cd-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b7cd-123">Type: **HRESULT**</span></span>

<span data-ttu-id="5b7cd-124">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="5b7cd-125">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b7cd-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5b7cd-126">Remarks</span></span>

<span data-ttu-id="5b7cd-127">Le segment de nom de fichier de *filePath* est utilisé comme nom de ressource ; les qualificateurs de ressources et sont dérivés de son chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="5b7cd-128">Par exemple, si vous transmettez L "images \\ de-- \\ scale-100 \\background.png" vers *filePath* , l’indexeur de ressource ajoute une ressource nommée "background.png" avec des qualificateurs de ressources "Language-out" et "Scale-100".</span><span class="sxs-lookup"><span data-stu-id="5b7cd-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="5b7cd-129">L "fichiers" sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="5b7cd-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7cd-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b7cd-130">Requirements</span></span>



| <span data-ttu-id="5b7cd-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b7cd-131">Requirement</span></span> | <span data-ttu-id="5b7cd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b7cd-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7cd-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b7cd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5b7cd-134">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b7cd-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b7cd-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b7cd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5b7cd-136">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b7cd-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b7cd-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b7cd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b7cd-138"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b7cd-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="5b7cd-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b7cd-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b7cd-140"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b7cd-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="5b7cd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b7cd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b7cd-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b7cd-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5b7cd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b7cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7cd-144">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="5b7cd-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

