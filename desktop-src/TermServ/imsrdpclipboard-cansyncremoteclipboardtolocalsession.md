---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession, méthode
description: Indique si le presse-papiers distant peut être synchronisé avec la session locale.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanSyncRemoteClipboardToLocalSession
- Méthode CanSyncRemoteClipboardToLocalSession Services Bureau à distance, interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, méthode CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106514901"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="e9846-106">IMsRdpClipboard :: CanSyncRemoteClipboardToLocalSession, méthode</span><span class="sxs-lookup"><span data-stu-id="e9846-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="e9846-107">Indique si le presse-papiers distant peut être synchronisé avec la session locale.</span><span class="sxs-lookup"><span data-stu-id="e9846-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9846-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9846-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="e9846-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9846-109">Parameters</span></span>

<span data-ttu-id="e9846-110">**True** si le presse-papiers distant peut être synchronisé avec la session locale ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e9846-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9846-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9846-111">Return value</span></span>

<span data-ttu-id="e9846-112">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e9846-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9846-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9846-113">Requirements</span></span>

| <span data-ttu-id="e9846-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9846-114">Requirement</span></span> | <span data-ttu-id="e9846-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9846-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e9846-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9846-116">Minimum supported client</span></span>| <span data-ttu-id="e9846-117">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="e9846-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e9846-118">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e9846-118">Type library</span></span>            | <span data-ttu-id="e9846-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e9846-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e9846-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e9846-120">DLL</span></span>                  | <span data-ttu-id="e9846-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e9846-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e9846-122">IID</span><span class="sxs-lookup"><span data-stu-id="e9846-122">IID</span></span>                      | <span data-ttu-id="e9846-123">IID \_ IMsRdpClipboard est défini en tant que 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="e9846-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="e9846-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9846-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9846-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="e9846-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>