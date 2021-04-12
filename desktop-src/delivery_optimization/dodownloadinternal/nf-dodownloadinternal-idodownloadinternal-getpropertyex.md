---
title: 'IDODownloadInternal :: GetPropertyEx, méthode'
description: Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique.
keywords:
- 'IDODownloadInternal :: GetPropertyEx, méthode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382216"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="60a35-104">IDODownloadInternal :: GetPropertyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="60a35-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60a35-105">L’interface **IDODownloadInternal** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="60a35-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="60a35-106">Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="60a35-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="60a35-107">Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="60a35-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60a35-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="60a35-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60a35-109">Parameters</span></span>

`propId`

<span data-ttu-id="60a35-110">ID de propriété requis pour la récupération (de type **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="60a35-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="60a35-111">Valeur de la propriété résultante, stockée dans un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="60a35-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="60a35-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="60a35-112">Return Value</span></span>

<span data-ttu-id="60a35-113">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="60a35-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="60a35-114">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="60a35-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="60a35-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60a35-115">Return value</span></span>|<span data-ttu-id="60a35-116">Description</span><span class="sxs-lookup"><span data-stu-id="60a35-116">Description</span></span>|
|-|-|
|<span data-ttu-id="60a35-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="60a35-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="60a35-118">*propid* est inconnu.</span><span class="sxs-lookup"><span data-stu-id="60a35-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="60a35-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="60a35-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="60a35-120">La propriété est en écriture seule et ne peut pas être lue.</span><span class="sxs-lookup"><span data-stu-id="60a35-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="60a35-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="60a35-121">E_NOT_SET</span></span>|<span data-ttu-id="60a35-122">Aucune propriété de ce type n’a été définie via **SetPropertyEx**.</span><span class="sxs-lookup"><span data-stu-id="60a35-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="60a35-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60a35-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="60a35-124">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="60a35-124">**Minimum supported client**</span></span> | <span data-ttu-id="60a35-125">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60a35-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="60a35-126">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="60a35-126">**Minimum supported server**</span></span> | <span data-ttu-id="60a35-127">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60a35-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="60a35-128">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="60a35-128">**Header**</span></span> | <span data-ttu-id="60a35-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="60a35-129">DODownloadInternal.h</span></span> |