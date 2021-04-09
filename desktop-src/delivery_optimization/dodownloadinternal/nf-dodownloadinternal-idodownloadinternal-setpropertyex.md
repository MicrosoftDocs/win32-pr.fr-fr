---
title: 'IDODownloadInternal :: SetPropertyEx, méthode'
description: Définit une propriété de téléchargement étendue. La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement.
keywords:
- 'IDODownloadInternal :: SetPropertyEx, méthode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941040"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="df72b-105">IDODownloadInternal :: SetPropertyEx, méthode</span><span class="sxs-lookup"><span data-stu-id="df72b-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df72b-106">L’interface **IDODownloadInternal** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="df72b-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="df72b-107">Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="df72b-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="df72b-108">Définit une propriété de téléchargement étendue.</span><span class="sxs-lookup"><span data-stu-id="df72b-108">Sets an extended download property.</span></span> <span data-ttu-id="df72b-109">La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="df72b-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="df72b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df72b-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="df72b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df72b-111">Parameters</span></span>

`propId`

<span data-ttu-id="df72b-112">ID de propriété requis à définir (de type **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="df72b-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="df72b-113">Valeur de la propriété à définir, stockée dans un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="df72b-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="df72b-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df72b-114">Return Value</span></span>

<span data-ttu-id="df72b-115">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="df72b-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="df72b-116">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="df72b-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="df72b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df72b-117">Return value</span></span>|<span data-ttu-id="df72b-118">Description</span><span class="sxs-lookup"><span data-stu-id="df72b-118">Description</span></span>|
|-|-|
|<span data-ttu-id="df72b-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="df72b-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="df72b-120">*propid* est inconnu.</span><span class="sxs-lookup"><span data-stu-id="df72b-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="df72b-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="df72b-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="df72b-122">Le téléchargement n’est pas actuellement dans un État qui permet de définir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="df72b-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="df72b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df72b-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="df72b-124">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="df72b-124">**Minimum supported client**</span></span> | <span data-ttu-id="df72b-125">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df72b-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="df72b-126">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="df72b-126">**Minimum supported server**</span></span> | <span data-ttu-id="df72b-127">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df72b-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="df72b-128">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="df72b-128">**Header**</span></span> | <span data-ttu-id="df72b-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="df72b-129">DODownloadInternal.h</span></span> |