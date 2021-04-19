---
title: Structure DO_DOWNLOAD_STATUS
description: Permet d’obtenir l’état d’un téléchargement spécifique.
keywords:
- Structure DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106510862"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="d97ff-104">Structure DO_DOWNLOAD_STATUS</span><span class="sxs-lookup"><span data-stu-id="d97ff-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="d97ff-105">La structure **DO_DOWNLOAD_STATUS** permet d’obtenir l’état d’un téléchargement spécifique.</span><span class="sxs-lookup"><span data-stu-id="d97ff-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="d97ff-106">Elle est obtenue en appelant la fonction **IDODownload :: GetStatus** .</span><span class="sxs-lookup"><span data-stu-id="d97ff-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d97ff-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="d97ff-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d97ff-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="d97ff-109">Nombre total d’octets à télécharger.</span><span class="sxs-lookup"><span data-stu-id="d97ff-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="d97ff-110">Nombre d’octets qui ont déjà été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="d97ff-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="d97ff-111">État de téléchargement actuel tel que défini par l’énumération **DODownloadState** .</span><span class="sxs-lookup"><span data-stu-id="d97ff-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="d97ff-112">Informations d’erreur (le cas échéant) associées au téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="d97ff-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="d97ff-113">Informations d’erreur étendues (si elles existent) associées au téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="d97ff-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97ff-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d97ff-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d97ff-115">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d97ff-115">**Minimum supported client**</span></span> | <span data-ttu-id="d97ff-116">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d97ff-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d97ff-117">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d97ff-117">**Minimum supported server**</span></span> | <span data-ttu-id="d97ff-118">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d97ff-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d97ff-119">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="d97ff-119">**Header**</span></span> | <span data-ttu-id="d97ff-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="d97ff-120">Do.h</span></span> |
