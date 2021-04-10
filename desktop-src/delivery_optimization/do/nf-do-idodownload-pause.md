---
title: IDODownload ::P méthode ause
description: Interrompt le téléchargement.
keywords:
- IDODownload ::P méthode ause
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101133"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="e2162-104">IDODownload ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="e2162-104">IDODownload::Pause method</span></span>

<span data-ttu-id="e2162-105">Interrompt le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e2162-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2162-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2162-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="e2162-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e2162-107">Return Value</span></span>

<span data-ttu-id="e2162-108">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e2162-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e2162-109">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e2162-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2162-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2162-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e2162-111">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="e2162-111">**Minimum supported client**</span></span> | <span data-ttu-id="e2162-112">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2162-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e2162-113">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="e2162-113">**Minimum supported server**</span></span> | <span data-ttu-id="e2162-114">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2162-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e2162-115">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="e2162-115">**Header**</span></span> | <span data-ttu-id="e2162-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="e2162-116">Do.h</span></span> |
