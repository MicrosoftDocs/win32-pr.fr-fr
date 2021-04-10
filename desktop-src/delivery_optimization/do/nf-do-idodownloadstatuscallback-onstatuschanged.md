---
title: 'IDODownloadStatusCallback :: OnStatusChange, méthode'
description: Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.
keywords:
- 'IDODownloadStatusCallback :: OnStatusChange, méthode'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104030642"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="749dd-104">IDODownloadStatusCallback :: OnStatusChange, méthode</span><span class="sxs-lookup"><span data-stu-id="749dd-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="749dd-105">Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé.</span><span class="sxs-lookup"><span data-stu-id="749dd-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="749dd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="749dd-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="749dd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="749dd-107">Parameters</span></span>

`download`

<span data-ttu-id="749dd-108">Pointeur vers l’interface **IDODownload** dont l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="749dd-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="749dd-109">Pointeur vers une structure **DO_DOWNLOAD_STATUS** contenant l’état du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="749dd-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="749dd-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="749dd-110">Return Value</span></span>

<span data-ttu-id="749dd-111">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="749dd-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="749dd-112">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="749dd-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="749dd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="749dd-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="749dd-114">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="749dd-114">**Minimum supported client**</span></span> | <span data-ttu-id="749dd-115">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="749dd-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="749dd-116">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="749dd-116">**Minimum supported server**</span></span> | <span data-ttu-id="749dd-117">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="749dd-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="749dd-118">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="749dd-118">**Header**</span></span> | <span data-ttu-id="749dd-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="749dd-119">Do.h</span></span> |
