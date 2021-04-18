---
title: 'IDODownload :: Finalize, méthode'
description: Finalise le téléchargement.
keywords:
- 'IDODownload :: Finalize, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106509234"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="a2fd2-104">IDODownload :: Finalize, méthode</span><span class="sxs-lookup"><span data-stu-id="a2fd2-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="a2fd2-105">Finalise le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a2fd2-105">Finalizes the download.</span></span> <span data-ttu-id="a2fd2-106">Une fois finalisé, un téléchargement ne peut pas être repris en appelant **Start**.</span><span class="sxs-lookup"><span data-stu-id="a2fd2-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fd2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2fd2-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="a2fd2-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2fd2-108">Return Value</span></span>

<span data-ttu-id="a2fd2-109">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a2fd2-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a2fd2-110">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a2fd2-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fd2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2fd2-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a2fd2-112">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a2fd2-112">**Minimum supported client**</span></span> | <span data-ttu-id="a2fd2-113">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2fd2-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a2fd2-114">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a2fd2-114">**Minimum supported server**</span></span> | <span data-ttu-id="a2fd2-115">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2fd2-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a2fd2-116">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="a2fd2-116">**Header**</span></span> | <span data-ttu-id="a2fd2-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="a2fd2-117">Do.h</span></span> |
