---
title: MrmIndexResourceContainerAutoQualifiers, fonction (MrmResourceIndexer. h)
description: Indexe les ressources de type chaîne contenues dans un fichier de ressources (. resw/. resjson), ou. priinfo ou. prifile, appartenant à une application UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menus de fonction MrmIndexResourceContainerAutoQualifiers et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106545756"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="78954-104">MrmIndexResourceContainerAutoQualifiers fonction)</span><span class="sxs-lookup"><span data-stu-id="78954-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="78954-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="78954-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="78954-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="78954-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="78954-107">Indexe les ressources de type chaîne contenues dans un fichier de ressources (. resw/. resjson), ou. priinfo ou. prifile, appartenant à une application UWP.</span><span class="sxs-lookup"><span data-stu-id="78954-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="78954-108">Déduit une liste de qualificateurs de ressources à partir du paramètre *containerPath* .</span><span class="sxs-lookup"><span data-stu-id="78954-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="78954-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="78954-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="78954-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78954-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="78954-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78954-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78954-112">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78954-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78954-113">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="78954-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="78954-114">Handle identifiant l’indexeur de ressource qui indexera les ressources de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="78954-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="78954-115">*containerPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78954-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78954-116">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="78954-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="78954-117">Chemin d’accès relatif à un. resw,. resjson,. priinfo ou. prifile contenant les ressources de type chaîne que vous souhaitez indexer.</span><span class="sxs-lookup"><span data-stu-id="78954-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="78954-118">Ce chemin d’accès est relatif à la racine du projet de l’application UWP pour laquelle vous générez des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="78954-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="78954-119">La racine du projet est la valeur de *projectRoot* que vous avez passée à [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="78954-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78954-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78954-120">Return value</span></span>

<span data-ttu-id="78954-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78954-121">Type: **HRESULT**</span></span>

<span data-ttu-id="78954-122">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="78954-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="78954-123">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="78954-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="78954-124">Notes</span><span class="sxs-lookup"><span data-stu-id="78954-124">Remarks</span></span>

<span data-ttu-id="78954-125">Les qualificateurs de ressources sont déduits à partir de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="78954-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="78954-126">Par exemple, la valeur L "en-US \\ \\ Resources. resw" ajoute des ressources de type chaîne avec le qualificateur "language-fr-US".</span><span class="sxs-lookup"><span data-stu-id="78954-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="78954-127">Le nom du fichier de ressources sera utilisé comme nom de sous-arborescence de mappage des ressources pour ces ressources lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="78954-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="78954-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78954-128">Requirements</span></span>



| <span data-ttu-id="78954-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78954-129">Requirement</span></span> | <span data-ttu-id="78954-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="78954-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78954-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78954-131">Minimum supported client</span></span><br/> | <span data-ttu-id="78954-132">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78954-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="78954-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78954-133">Minimum supported server</span></span><br/> | <span data-ttu-id="78954-134">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78954-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78954-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="78954-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="78954-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="78954-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="78954-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78954-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="78954-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78954-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="78954-139">DLL</span><span class="sxs-lookup"><span data-stu-id="78954-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78954-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78954-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="78954-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78954-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78954-142">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="78954-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

