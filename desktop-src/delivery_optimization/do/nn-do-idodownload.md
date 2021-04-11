---
title: Interface IDODownload
description: Utilisé pour démarrer et gérer un téléchargement.
keywords:
- Interface IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315263"
---
# <a name="idodownload-interface"></a><span data-ttu-id="92bd9-104">Interface IDODownload</span><span class="sxs-lookup"><span data-stu-id="92bd9-104">IDODownload interface</span></span>

<span data-ttu-id="92bd9-105">L’interface **IDODownload** est utilisée pour démarrer et gérer un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="92bd9-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92bd9-106">Methods</span></span>

<span data-ttu-id="92bd9-107">L’interface **IDODownload** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="92bd9-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="92bd9-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="92bd9-108">Method</span></span> | <span data-ttu-id="92bd9-109">Description</span><span class="sxs-lookup"><span data-stu-id="92bd9-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="92bd9-110">IDODownload :: Abort</span><span class="sxs-lookup"><span data-stu-id="92bd9-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="92bd9-111">Abandonne le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-111">Aborts the download.</span></span> |
| [<span data-ttu-id="92bd9-112">IDODownload :: Finalize</span><span class="sxs-lookup"><span data-stu-id="92bd9-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="92bd9-113">Finalise le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="92bd9-114">IDODownload :: GetProperty</span><span class="sxs-lookup"><span data-stu-id="92bd9-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="92bd9-115">Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique.</span><span class="sxs-lookup"><span data-stu-id="92bd9-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="92bd9-116">IDODownload :: GetStatus</span><span class="sxs-lookup"><span data-stu-id="92bd9-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="92bd9-117">Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="92bd9-118">IDODownload ::P ause</span><span class="sxs-lookup"><span data-stu-id="92bd9-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="92bd9-119">Interrompt le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-119">Pauses the download.</span></span> |
| [<span data-ttu-id="92bd9-120">IDODownload :: SetProperty</span><span class="sxs-lookup"><span data-stu-id="92bd9-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="92bd9-121">Définit une propriété de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-121">Sets a download property.</span></span> |
| [<span data-ttu-id="92bd9-122">IDODownload :: Start</span><span class="sxs-lookup"><span data-stu-id="92bd9-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="92bd9-123">Démarre ou reprend un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="92bd9-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="92bd9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92bd9-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="92bd9-125">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="92bd9-125">**Minimum supported client**</span></span> | <span data-ttu-id="92bd9-126">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92bd9-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="92bd9-127">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="92bd9-127">**Minimum supported server**</span></span> | <span data-ttu-id="92bd9-128">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92bd9-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="92bd9-129">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="92bd9-129">**Header**</span></span> | <span data-ttu-id="92bd9-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="92bd9-130">Do.h</span></span> |