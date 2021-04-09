---
title: Interface IDODownloadInternal
description: Utilisé pour récupérer ou définir les propriétés de téléchargement étendues.
keywords:
- Interface IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102016"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="68408-104">Interface IDODownloadInternal</span><span class="sxs-lookup"><span data-stu-id="68408-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68408-105">L’interface **IDODownloadInternal** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="68408-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="68408-106">Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="68408-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="68408-107">L’interface **IDODownloadInternal** est utilisée pour récupérer ou définir des propriétés de téléchargement étendues.</span><span class="sxs-lookup"><span data-stu-id="68408-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="68408-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68408-108">Methods</span></span>

<span data-ttu-id="68408-109">L’interface **IDODownloadInternal** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="68408-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="68408-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="68408-110">Method</span></span> | <span data-ttu-id="68408-111">Description</span><span class="sxs-lookup"><span data-stu-id="68408-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="68408-112">IDODownloadInternal::GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="68408-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="68408-113">Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="68408-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="68408-114">IDODownloadInternal::SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="68408-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="68408-115">Définit une propriété de téléchargement étendue.</span><span class="sxs-lookup"><span data-stu-id="68408-115">Sets an extended download property.</span></span> <span data-ttu-id="68408-116">La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="68408-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="68408-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68408-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="68408-118">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="68408-118">**Minimum supported client**</span></span> | <span data-ttu-id="68408-119">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68408-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="68408-120">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="68408-120">**Minimum supported server**</span></span> | <span data-ttu-id="68408-121">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68408-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="68408-122">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="68408-122">**Header**</span></span> | <span data-ttu-id="68408-123">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="68408-123">DODownloadInternal.h</span></span> |