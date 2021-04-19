---
title: Interface IDOManager
description: Utilisé pour créer un nouveau téléchargement et énumérer les téléchargements existants.
keywords:
- Interface IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513546"
---
# <a name="idomanager-interface"></a><span data-ttu-id="b38f8-104">Interface IDOManager</span><span class="sxs-lookup"><span data-stu-id="b38f8-104">IDOManager interface</span></span>

<span data-ttu-id="b38f8-105">L’interface **IDOManager** est utilisée pour créer un nouveau téléchargement et énumérer les téléchargements existants.</span><span class="sxs-lookup"><span data-stu-id="b38f8-105">The **IDOManager** interface is used to create a new download, and to enumerate existing downloads.</span></span>

## <a name="methods"></a><span data-ttu-id="b38f8-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b38f8-106">Methods</span></span>

<span data-ttu-id="b38f8-107">L’interface **IDOManager** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b38f8-107">The **IDOManager** interface has these methods.</span></span>

| <span data-ttu-id="b38f8-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="b38f8-108">Method</span></span> | <span data-ttu-id="b38f8-109">Description</span><span class="sxs-lookup"><span data-stu-id="b38f8-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="b38f8-110">IDOManager::CreateDownload</span><span class="sxs-lookup"><span data-stu-id="b38f8-110">IDOManager::CreateDownload</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="b38f8-111">Crée un nouveau téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b38f8-111">Creates a new download.</span></span> |
| [<span data-ttu-id="b38f8-112">IDOManager::EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="b38f8-112">IDOManager::EnumDownloads</span></span>](./nf-do-idomanager-enumdownloads.md) | <span data-ttu-id="b38f8-113">Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants.</span><span class="sxs-lookup"><span data-stu-id="b38f8-113">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span> |

## <a name="requirements"></a><span data-ttu-id="b38f8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b38f8-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b38f8-115">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b38f8-115">**Minimum supported client**</span></span> | <span data-ttu-id="b38f8-116">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b38f8-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b38f8-117">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="b38f8-117">**Minimum supported server**</span></span> | <span data-ttu-id="b38f8-118">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b38f8-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b38f8-119">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="b38f8-119">**Header**</span></span> | <span data-ttu-id="b38f8-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="b38f8-120">Do.h</span></span> |