---
title: 'IDODownload :: SetProperty, méthode'
description: Définit une propriété de téléchargement.
keywords:
- 'IDODownload :: SetProperty, méthode'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679242"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="a0492-104">IDODownload :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="a0492-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="a0492-105">Définit une propriété de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a0492-105">Sets a download property.</span></span> <span data-ttu-id="a0492-106">La méthode accepte un pointeur vers un **Variant** qui contient une propriété spécifique à appliquer au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a0492-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0492-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0492-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="a0492-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0492-108">Parameters</span></span>

`propId`

<span data-ttu-id="a0492-109">ID de propriété requis à définir (de type **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="a0492-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="a0492-110">Valeur de la propriété à définir, stockée dans un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="a0492-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0492-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a0492-111">Return Value</span></span>

<span data-ttu-id="a0492-112">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a0492-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a0492-113">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a0492-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="a0492-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0492-114">Return value</span></span>|<span data-ttu-id="a0492-115">Description</span><span class="sxs-lookup"><span data-stu-id="a0492-115">Description</span></span>|
|-|-|
|<span data-ttu-id="a0492-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="a0492-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="a0492-117">*propid* est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a0492-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="a0492-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="a0492-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="a0492-119">Le téléchargement n’est pas actuellement dans un État qui permet de définir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="a0492-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="a0492-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0492-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a0492-121">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a0492-121">**Minimum supported client**</span></span> | <span data-ttu-id="a0492-122">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0492-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a0492-123">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a0492-123">**Minimum supported server**</span></span> | <span data-ttu-id="a0492-124">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0492-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a0492-125">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="a0492-125">**Header**</span></span> | <span data-ttu-id="a0492-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="a0492-126">Do.h</span></span> |
