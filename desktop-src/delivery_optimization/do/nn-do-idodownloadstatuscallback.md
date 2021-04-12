---
title: Interface IDODownloadStatusCallback
description: Utilisé pour recevoir des notifications relatives à un téléchargement.
keywords:
- Interface IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382009"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="451e6-104">Interface IDODownloadStatusCallback</span><span class="sxs-lookup"><span data-stu-id="451e6-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="451e6-105">L’interface **IDODownloadStatusCallback** est utilisée pour recevoir des notifications relatives à un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="451e6-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="451e6-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="451e6-106">Methods</span></span>

<span data-ttu-id="451e6-107">L’interface **IDODownloadStatusCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="451e6-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="451e6-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="451e6-108">Method</span></span> | <span data-ttu-id="451e6-109">Description</span><span class="sxs-lookup"><span data-stu-id="451e6-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="451e6-110">IDODownloadStatusCallback::OnStatusChanged</span><span class="sxs-lookup"><span data-stu-id="451e6-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="451e6-111">Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.</span><span class="sxs-lookup"><span data-stu-id="451e6-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="451e6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="451e6-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="451e6-113">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="451e6-113">**Minimum supported client**</span></span> | <span data-ttu-id="451e6-114">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="451e6-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="451e6-115">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="451e6-115">**Minimum supported server**</span></span> | <span data-ttu-id="451e6-116">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="451e6-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="451e6-117">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="451e6-117">**Header**</span></span> | <span data-ttu-id="451e6-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="451e6-118">Do.h</span></span> |