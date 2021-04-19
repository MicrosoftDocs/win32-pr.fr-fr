---
title: 'IDODownload :: Abort, méthode'
description: Abandonne le téléchargement.
keywords:
- 'IDODownload :: Abort, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106509826"
---
# <a name="idodownloadabort-method"></a><span data-ttu-id="aa5dd-104">IDODownload :: Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="aa5dd-104">IDODownload::Abort method</span></span>

<span data-ttu-id="aa5dd-105">Abandonne le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="aa5dd-105">Aborts the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5dd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa5dd-106">Syntax</span></span>

```cpp
HRESULT Abort();
```

## <a name="return-value"></a><span data-ttu-id="aa5dd-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="aa5dd-107">Return Value</span></span>

<span data-ttu-id="aa5dd-108">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="aa5dd-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="aa5dd-109">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="aa5dd-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5dd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa5dd-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa5dd-111">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="aa5dd-111">**Minimum supported client**</span></span> | <span data-ttu-id="aa5dd-112">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa5dd-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="aa5dd-113">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="aa5dd-113">**Minimum supported server**</span></span> | <span data-ttu-id="aa5dd-114">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa5dd-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="aa5dd-115">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="aa5dd-115">**Header**</span></span> | <span data-ttu-id="aa5dd-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="aa5dd-116">Do.h</span></span> |
