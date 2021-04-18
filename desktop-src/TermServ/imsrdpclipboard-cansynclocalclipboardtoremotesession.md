---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession, méthode
description: Indique si le presse-papiers local peut être synchronisé avec la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanSyncLocalClipboardToRemoteSession
- Méthode CanSyncLocalClipboardToRemoteSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106533581"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="06876-106">IMsRdpClipboard :: CanSyncLocalClipboardToRemoteSession, méthode</span><span class="sxs-lookup"><span data-stu-id="06876-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="06876-107">Indique si le presse-papiers local peut être synchronisé avec la session à distance.</span><span class="sxs-lookup"><span data-stu-id="06876-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="06876-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06876-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="06876-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06876-109">Parameters</span></span>

<span data-ttu-id="06876-110">**True** si le presse-papiers local peut être synchronisé avec la session à distance ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="06876-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="06876-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06876-111">Return value</span></span>

<span data-ttu-id="06876-112">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="06876-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="06876-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06876-113">Requirements</span></span>

| <span data-ttu-id="06876-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06876-114">Requirement</span></span> | <span data-ttu-id="06876-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="06876-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="06876-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06876-116">Minimum supported client</span></span>| <span data-ttu-id="06876-117">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="06876-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="06876-118">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="06876-118">Type library</span></span>            | <span data-ttu-id="06876-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="06876-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="06876-120">DLL</span><span class="sxs-lookup"><span data-stu-id="06876-120">DLL</span></span>                  | <span data-ttu-id="06876-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="06876-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="06876-122">IID</span><span class="sxs-lookup"><span data-stu-id="06876-122">IID</span></span>                      | <span data-ttu-id="06876-123">IID \_ IMsRdpClipboard est défini en tant que 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="06876-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="06876-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06876-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06876-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="06876-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>