---
title: MrmCreateResourceIndexer, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource, utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menus de fonction MrmCreateResourceIndexer et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385123"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="709b7-105">MrmCreateResourceIndexer fonction)</span><span class="sxs-lookup"><span data-stu-id="709b7-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="709b7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="709b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="709b7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="709b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="709b7-108">Crée un indexeur de ressource, utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP.</span><span class="sxs-lookup"><span data-stu-id="709b7-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="709b7-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="709b7-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="709b7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="709b7-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="709b7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="709b7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="709b7-112">*packageFamilyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="709b7-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709b7-113">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="709b7-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="709b7-114">Nom de la famille de packages de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="709b7-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="709b7-115">Cette valeur sera utilisée comme nom de mappage de ressources lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="709b7-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="709b7-116">*projectRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="709b7-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709b7-117">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="709b7-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="709b7-118">Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI.</span><span class="sxs-lookup"><span data-stu-id="709b7-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="709b7-119">En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application.</span><span class="sxs-lookup"><span data-stu-id="709b7-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="709b7-120">Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="709b7-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="709b7-121">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="709b7-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709b7-122">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="709b7-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="709b7-123">Version de la plateforme cible pour l’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="709b7-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="709b7-124">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="709b7-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="709b7-125">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="709b7-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="709b7-126">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="709b7-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="709b7-127">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="709b7-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="709b7-128">*indexeur* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="709b7-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="709b7-129">Tapez : \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="709b7-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="709b7-130">Pointeur vers un handle d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="709b7-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="709b7-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="709b7-131">Return value</span></span>

<span data-ttu-id="709b7-132">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="709b7-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="709b7-133">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="709b7-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="709b7-134">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="709b7-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="709b7-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="709b7-135">Requirements</span></span>



| <span data-ttu-id="709b7-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="709b7-136">Requirement</span></span> | <span data-ttu-id="709b7-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="709b7-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709b7-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="709b7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="709b7-139">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="709b7-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="709b7-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="709b7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="709b7-141">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="709b7-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="709b7-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="709b7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="709b7-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="709b7-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="709b7-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="709b7-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="709b7-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="709b7-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="709b7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="709b7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="709b7-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709b7-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="709b7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="709b7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709b7-149">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="709b7-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

