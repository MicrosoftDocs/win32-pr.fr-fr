---
title: IMsRdpClientNonScriptable7 Clipboard, propriété
description: Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés du presse-papiers
- Propriété Clipboard Services Bureau à distance, interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, propriété Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103949937"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="c3312-106">IMsRdpClientNonScriptable7 :: Clipboard, propriété</span><span class="sxs-lookup"><span data-stu-id="c3312-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="c3312-107">Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.</span><span class="sxs-lookup"><span data-stu-id="c3312-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="c3312-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c3312-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3312-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3312-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="c3312-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c3312-110">Property value</span></span>

<span data-ttu-id="c3312-111">[IMsRdpClipboard](imsrdpclipboard.md) qui représente le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée (autrement dit, la valeur de la propriété [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) est définie sur **true**).</span><span class="sxs-lookup"><span data-stu-id="c3312-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3312-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3312-112">Requirements</span></span>

| <span data-ttu-id="c3312-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3312-113">Requirement</span></span> | <span data-ttu-id="c3312-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3312-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c3312-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3312-115">Minimum supported client</span></span>| <span data-ttu-id="c3312-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="c3312-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="c3312-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c3312-117">Type library</span></span>            | <span data-ttu-id="c3312-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c3312-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c3312-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c3312-119">DLL</span></span>                  | <span data-ttu-id="c3312-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c3312-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c3312-121">IID</span><span class="sxs-lookup"><span data-stu-id="c3312-121">IID</span></span>                      | <span data-ttu-id="c3312-122">IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="c3312-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="c3312-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3312-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3312-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="c3312-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>