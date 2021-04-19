---
title: MrmCreateConfig, fonction (MrmResourceIndexer. h)
description: Crée un nouveau fichier de configuration PRI initialisé définissant les valeurs par défaut du qualificateur que vous spécifiez. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Menus de fonction MrmCreateConfig et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515078"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="aab43-105">MrmCreateConfig fonction)</span><span class="sxs-lookup"><span data-stu-id="aab43-105">MrmCreateConfig function</span></span>

<span data-ttu-id="aab43-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="aab43-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aab43-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="aab43-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aab43-108">Crée un nouveau fichier de configuration PRI initialisé définissant les valeurs par défaut du qualificateur que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="aab43-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="aab43-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="aab43-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="aab43-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aab43-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="aab43-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aab43-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab43-112">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aab43-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab43-113">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="aab43-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="aab43-114">Version de la plateforme (*targetOsVersion*) à utiliser pour le fichier de configuration généré.</span><span class="sxs-lookup"><span data-stu-id="aab43-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="aab43-115">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="aab43-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aab43-116">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="aab43-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="aab43-117">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="aab43-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="aab43-118">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="aab43-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="aab43-119">*outputXmlFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aab43-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab43-120">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="aab43-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="aab43-121">Chemin d’accès du fichier de configuration à créer.</span><span class="sxs-lookup"><span data-stu-id="aab43-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab43-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aab43-122">Return value</span></span>

<span data-ttu-id="aab43-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aab43-123">Type: **HRESULT**</span></span>

<span data-ttu-id="aab43-124">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="aab43-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="aab43-125">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="aab43-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab43-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aab43-126">Requirements</span></span>



| <span data-ttu-id="aab43-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aab43-127">Requirement</span></span> | <span data-ttu-id="aab43-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="aab43-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab43-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab43-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aab43-130">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aab43-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aab43-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aab43-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aab43-132">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aab43-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aab43-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="aab43-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab43-134"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab43-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="aab43-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aab43-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="aab43-136"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aab43-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="aab43-137">DLL</span><span class="sxs-lookup"><span data-stu-id="aab43-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab43-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab43-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="aab43-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aab43-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab43-140">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="aab43-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

