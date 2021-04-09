---
title: MrmDestroyIndexerAndMessages, fonction (MrmResourceIndexer. h)
description: Libère les ressources de l’ordinateur associées à un indexeur de ressource.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menus de fonction MrmDestroyIndexerAndMessages et autres ressources
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033233"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="8abbe-104">MrmDestroyIndexerAndMessages fonction)</span><span class="sxs-lookup"><span data-stu-id="8abbe-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="8abbe-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8abbe-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8abbe-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8abbe-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8abbe-107">Libère les ressources de l’ordinateur associées à un indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="8abbe-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="8abbe-108">Détruit le handle, libère l’indexeur et supprime tous les messages.</span><span class="sxs-lookup"><span data-stu-id="8abbe-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="8abbe-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8abbe-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8abbe-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8abbe-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="8abbe-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8abbe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8abbe-112">*indexeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8abbe-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8abbe-113">Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="8abbe-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="8abbe-114">Handle identifiant l’indexeur de ressource à détruire.</span><span class="sxs-lookup"><span data-stu-id="8abbe-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8abbe-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8abbe-115">Return value</span></span>

<span data-ttu-id="8abbe-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8abbe-116">Type: **HRESULT**</span></span>

<span data-ttu-id="8abbe-117">\_OK si la fonction a réussi, sinon une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="8abbe-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="8abbe-118">Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="8abbe-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8abbe-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8abbe-119">Requirements</span></span>



| <span data-ttu-id="8abbe-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8abbe-120">Requirement</span></span> | <span data-ttu-id="8abbe-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8abbe-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abbe-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8abbe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8abbe-123">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8abbe-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8abbe-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8abbe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8abbe-125">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8abbe-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8abbe-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8abbe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8abbe-127"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8abbe-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="8abbe-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8abbe-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8abbe-129"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8abbe-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="8abbe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8abbe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8abbe-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8abbe-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8abbe-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8abbe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8abbe-133">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="8abbe-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

