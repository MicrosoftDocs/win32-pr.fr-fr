---
title: 'IDODownload :: GetProperty, méthode'
description: Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique.
keywords:
- 'IDODownload :: GetProperty, méthode'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841733"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="81d02-104">IDODownload :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="81d02-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="81d02-105">Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique.</span><span class="sxs-lookup"><span data-stu-id="81d02-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d02-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81d02-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="81d02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81d02-107">Parameters</span></span>

`propId`

<span data-ttu-id="81d02-108">ID de propriété requis pour la récupération (de type **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="81d02-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="81d02-109">Valeur de la propriété résultante, stockée dans un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="81d02-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="81d02-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81d02-110">Return Value</span></span>

<span data-ttu-id="81d02-111">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="81d02-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="81d02-112">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="81d02-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="81d02-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81d02-113">Return value</span></span>|<span data-ttu-id="81d02-114">Description</span><span class="sxs-lookup"><span data-stu-id="81d02-114">Description</span></span>|
|-|-|
|<span data-ttu-id="81d02-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="81d02-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="81d02-116">*propid* est inconnu.</span><span class="sxs-lookup"><span data-stu-id="81d02-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="81d02-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="81d02-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="81d02-118">La propriété est en écriture seule et ne peut pas être lue.</span><span class="sxs-lookup"><span data-stu-id="81d02-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="81d02-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="81d02-119">E_NOT_SET</span></span>|<span data-ttu-id="81d02-120">Aucune propriété de ce type n’a été définie via **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="81d02-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="81d02-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d02-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="81d02-122">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="81d02-122">**Minimum supported client**</span></span> | <span data-ttu-id="81d02-123">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81d02-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="81d02-124">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="81d02-124">**Minimum supported server**</span></span> | <span data-ttu-id="81d02-125">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81d02-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="81d02-126">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="81d02-126">**Header**</span></span> | <span data-ttu-id="81d02-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="81d02-127">Do.h</span></span> |
