---
title: IMsRdpClipboard, interface
description: Représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClipboard
- Services Bureau à distance de l’interface IMsRdpClipboard, Description
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108367"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="f8684-105">IMsRdpClipboard, interface</span><span class="sxs-lookup"><span data-stu-id="f8684-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="f8684-106">Représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée (autrement dit, la valeur de la propriété [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) est définie sur **true**).</span><span class="sxs-lookup"><span data-stu-id="f8684-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="f8684-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f8684-107">Members</span></span>

<span data-ttu-id="f8684-108">L’interface **IMsRdpClipboard** hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="f8684-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="f8684-109">**IMsRdpClipboard** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8684-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="f8684-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8684-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f8684-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8684-111">Methods</span></span>

<span data-ttu-id="f8684-112">L’interface **IMsRdpClipboard** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f8684-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="f8684-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f8684-113">Method</span></span>        | <span data-ttu-id="f8684-114">Description</span><span class="sxs-lookup"><span data-stu-id="f8684-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="f8684-115">**CanSyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="f8684-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="f8684-116">Indique si le presse-papiers local peut être synchronisé avec la session à distance.</span><span class="sxs-lookup"><span data-stu-id="f8684-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="f8684-117">**CanSyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="f8684-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="f8684-118">Indique si le presse-papiers distant peut être synchronisé avec la session locale.</span><span class="sxs-lookup"><span data-stu-id="f8684-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="f8684-119">**SyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="f8684-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="f8684-120">Synchronise le presse-papiers local avec la session à distance.</span><span class="sxs-lookup"><span data-stu-id="f8684-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="f8684-121">**SyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="f8684-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="f8684-122">Synchronise le presse-papiers distant avec la session locale.</span><span class="sxs-lookup"><span data-stu-id="f8684-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="f8684-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8684-123">Requirements</span></span>

| <span data-ttu-id="f8684-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8684-124">Requirement</span></span> | <span data-ttu-id="f8684-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8684-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f8684-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8684-126">Minimum supported client</span></span>| <span data-ttu-id="f8684-127">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="f8684-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f8684-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f8684-128">Type library</span></span>            | <span data-ttu-id="f8684-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f8684-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f8684-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f8684-130">DLL</span></span>                  | <span data-ttu-id="f8684-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f8684-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f8684-132">IID</span><span class="sxs-lookup"><span data-stu-id="f8684-132">IID</span></span>                      | <span data-ttu-id="f8684-133">IID \_ IMsRdpClipboard est défini en tant que 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="f8684-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="f8684-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8684-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8684-135">**IMsRdpClientNonScriptable7 :: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="f8684-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
