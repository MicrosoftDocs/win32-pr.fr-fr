---
title: 'IDOManager :: CreateDownload, méthode'
description: Crée un nouveau téléchargement.
keywords:
- 'IDOManager :: CreateDownload, méthode'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381285"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="a2b19-104">IDOManager :: CreateDownload, méthode</span><span class="sxs-lookup"><span data-stu-id="a2b19-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="a2b19-105">Crée un nouveau téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a2b19-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b19-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b19-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="a2b19-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2b19-107">Parameters</span></span>

`download`

<span data-ttu-id="a2b19-108">Adresse d’un pointeur d’interface **IDODownload** .</span><span class="sxs-lookup"><span data-stu-id="a2b19-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2b19-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a2b19-109">Return Value</span></span>

<span data-ttu-id="a2b19-110">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a2b19-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a2b19-111">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a2b19-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b19-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2b19-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a2b19-113">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a2b19-113">**Minimum supported client**</span></span> | <span data-ttu-id="a2b19-114">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b19-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a2b19-115">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a2b19-115">**Minimum supported server**</span></span> | <span data-ttu-id="a2b19-116">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2b19-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a2b19-117">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="a2b19-117">**Header**</span></span> | <span data-ttu-id="a2b19-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="a2b19-118">Do.h</span></span> |
