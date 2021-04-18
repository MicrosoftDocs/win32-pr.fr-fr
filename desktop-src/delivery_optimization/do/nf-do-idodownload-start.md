---
title: 'IDODownload :: Start, méthode'
description: Démarre ou reprend un téléchargement.
keywords:
- 'IDODownload :: Start, méthode'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106522908"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="e012f-104">IDODownload :: Start, méthode</span><span class="sxs-lookup"><span data-stu-id="e012f-104">IDODownload::Start method</span></span>

<span data-ttu-id="e012f-105">Démarre ou reprend un téléchargement, en passant des plages facultatives en tant que pointeur vers [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span><span class="sxs-lookup"><span data-stu-id="e012f-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e012f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e012f-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="e012f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e012f-107">Parameters</span></span>

`ranges`

<span data-ttu-id="e012f-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e012f-108">Optional.</span></span> <span data-ttu-id="e012f-109">Pointeur vers une structure [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (pour télécharger uniquement des plages spécifiques du fichier).</span><span class="sxs-lookup"><span data-stu-id="e012f-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="e012f-110">Pass `nullptr` pour télécharger l’intégralité du fichier.</span><span class="sxs-lookup"><span data-stu-id="e012f-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="e012f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e012f-111">Return Value</span></span>

<span data-ttu-id="e012f-112">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e012f-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e012f-113">Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e012f-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e012f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e012f-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e012f-115">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="e012f-115">**Minimum supported client**</span></span> | <span data-ttu-id="e012f-116">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e012f-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e012f-117">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="e012f-117">**Minimum supported server**</span></span> | <span data-ttu-id="e012f-118">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e012f-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e012f-119">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="e012f-119">**Header**</span></span> | <span data-ttu-id="e012f-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="e012f-120">Do.h</span></span> |
