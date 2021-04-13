---
title: MrmCreateConfigInMemory, fonction (MrmResourceIndexer. h)
description: Crée des informations de configuration PRI initialisées (comme des données en mémoire, et non comme un fichier) qui définissent les valeurs par défaut du qualificateur que vous spécifiez.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menus de fonction MrmCreateConfigInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509186"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="38d96-104">MrmCreateConfigInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="38d96-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="38d96-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="38d96-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="38d96-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="38d96-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="38d96-107">Crée des informations de configuration PRI initialisées (comme des données en mémoire, et non comme un fichier) qui définissent les valeurs par défaut du qualificateur que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="38d96-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="38d96-108">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38d96-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="38d96-109">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="38d96-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="38d96-110">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="38d96-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="38d96-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38d96-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="38d96-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38d96-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d96-113">*platformVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38d96-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38d96-114">Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="38d96-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="38d96-115">Version de la plateforme (*targetOsVersion*) à utiliser pour les informations de configuration générées.</span><span class="sxs-lookup"><span data-stu-id="38d96-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="38d96-116">*defaultQualifiers* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="38d96-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38d96-117">Type : **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="38d96-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="38d96-118">Liste des qualificateurs de ressources par défaut.</span><span class="sxs-lookup"><span data-stu-id="38d96-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="38d96-119">Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »</span><span class="sxs-lookup"><span data-stu-id="38d96-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="38d96-120">*outputXmlData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38d96-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38d96-121">Type : **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="38d96-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="38d96-122">Adresse d’un pointeur vers l’octet.</span><span class="sxs-lookup"><span data-stu-id="38d96-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="38d96-123">La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38d96-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="38d96-124">Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.</span><span class="sxs-lookup"><span data-stu-id="38d96-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="38d96-125">*outputXmlSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38d96-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38d96-126">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="38d96-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="38d96-127">Adresse d’un ULONG.</span><span class="sxs-lookup"><span data-stu-id="38d96-127">The address of a ULONG.</span></span> <span data-ttu-id="38d96-128">Dans _outputXmlSize \*, la fonction retourne la taille de la mémoire allouée appelée par *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="38d96-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d96-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38d96-129">Return value</span></span>

<span data-ttu-id="38d96-130">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="38d96-130">Type: **HRESULT**</span></span>

<span data-ttu-id="38d96-131">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="38d96-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="38d96-132">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="38d96-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d96-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38d96-133">Requirements</span></span>



| <span data-ttu-id="38d96-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38d96-134">Requirement</span></span> | <span data-ttu-id="38d96-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="38d96-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d96-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38d96-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38d96-137">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38d96-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="38d96-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38d96-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38d96-139">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38d96-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38d96-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="38d96-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d96-141"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d96-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="38d96-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38d96-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="38d96-143"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38d96-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="38d96-144">DLL</span><span class="sxs-lookup"><span data-stu-id="38d96-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38d96-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38d96-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="38d96-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38d96-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d96-147">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="38d96-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

