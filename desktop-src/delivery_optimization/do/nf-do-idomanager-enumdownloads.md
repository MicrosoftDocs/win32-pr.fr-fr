---
title: 'IDOManager :: EnumDownloads, méthode'
description: Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants.
keywords:
- 'IDOManager :: EnumDownloads, méthode'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512291"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="71961-104">IDOManager :: EnumDownloads, méthode</span><span class="sxs-lookup"><span data-stu-id="71961-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="71961-105">Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants.</span><span class="sxs-lookup"><span data-stu-id="71961-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="71961-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71961-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="71961-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71961-107">Parameters</span></span>

`category`

<span data-ttu-id="71961-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="71961-108">Optional.</span></span> <span data-ttu-id="71961-109">Nom de la propriété à utiliser comme catégorie à énumérer.</span><span class="sxs-lookup"><span data-stu-id="71961-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="71961-110">La réussite `nullptr` permet de récupérer tous les téléchargements existants.</span><span class="sxs-lookup"><span data-stu-id="71961-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="71961-111">Les propriétés suivantes sont prises en charge en tant que catégorie.</span><span class="sxs-lookup"><span data-stu-id="71961-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="71961-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="71961-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="71961-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="71961-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="71961-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="71961-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="71961-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="71961-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="71961-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="71961-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="71961-117">Adresse d’un pointeur d’interface vers **IEnumUnknown**, qui est utilisé pour énumérer les téléchargements existants.</span><span class="sxs-lookup"><span data-stu-id="71961-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="71961-118">Le contenu de l’énumérateur dépend de la valeur de *Category*.</span><span class="sxs-lookup"><span data-stu-id="71961-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="71961-119">Les téléchargements inclus dans l’interface d’énumération sont ceux qui ont été précédemment créés par le même appelant à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="71961-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="71961-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71961-120">Return Value</span></span>

<span data-ttu-id="71961-121">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="71961-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="71961-122">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="71961-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="71961-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71961-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="71961-124">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="71961-124">**Minimum supported client**</span></span> | <span data-ttu-id="71961-125">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71961-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="71961-126">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="71961-126">**Minimum supported server**</span></span> | <span data-ttu-id="71961-127">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71961-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="71961-128">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="71961-128">**Header**</span></span> | <span data-ttu-id="71961-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="71961-129">Do.h</span></span> |
