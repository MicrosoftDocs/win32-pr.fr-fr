---
title: 'IDODownload :: GetStatus, méthode'
description: Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement.
keywords:
- 'IDODownload :: GetStatus, méthode'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381287"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="3aaa7-104">IDODownload :: GetStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="3aaa7-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="3aaa7-105">Récupère un pointeur vers une structure **DO_DOWNLOAD_STATUS** qui reflète l’état actuel du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aaa7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aaa7-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="3aaa7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aaa7-107">Parameters</span></span>

`status`

<span data-ttu-id="3aaa7-108">Pointeur vers une structure **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="3aaa7-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aaa7-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3aaa7-109">Return Value</span></span>

<span data-ttu-id="3aaa7-110">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3aaa7-111">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3aaa7-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aaa7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aaa7-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3aaa7-113">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="3aaa7-113">**Minimum supported client**</span></span> | <span data-ttu-id="3aaa7-114">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aaa7-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3aaa7-115">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="3aaa7-115">**Minimum supported server**</span></span> | <span data-ttu-id="3aaa7-116">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aaa7-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3aaa7-117">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="3aaa7-117">**Header**</span></span> | <span data-ttu-id="3aaa7-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="3aaa7-118">Do.h</span></span> |
