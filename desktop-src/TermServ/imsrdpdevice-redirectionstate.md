---
title: IMsRdpDevice propriété RedirectionState
description: Indique l’état de redirection de l’appareil.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectionState
- Services Bureau à distance de la propriété RedirectionState, interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, propriété RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465131"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="ea6b0-106">IMsRdpDevice :: RedirectionState, propriété</span><span class="sxs-lookup"><span data-stu-id="ea6b0-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="ea6b0-107">Indique l’état de redirection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea6b0-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="ea6b0-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ea6b0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6b0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea6b0-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="ea6b0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ea6b0-110">Property value</span></span>

<span data-ttu-id="ea6b0-111">Affectez à ce paramètre la valeur **Variant \_ false** pour désactiver la redirection ou la **\_ valeur true** pour activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="ea6b0-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea6b0-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ea6b0-112">Error codes</span></span>

<span data-ttu-id="ea6b0-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="ea6b0-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ea6b0-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="ea6b0-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6b0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea6b0-115">Requirements</span></span>



| <span data-ttu-id="ea6b0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea6b0-116">Requirement</span></span> | <span data-ttu-id="ea6b0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea6b0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6b0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea6b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea6b0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea6b0-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ea6b0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea6b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea6b0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea6b0-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ea6b0-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ea6b0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea6b0-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b0-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea6b0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ea6b0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea6b0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b0-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea6b0-126">IID</span><span class="sxs-lookup"><span data-stu-id="ea6b0-126">IID</span></span><br/>                      | <span data-ttu-id="ea6b0-127">IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="ea6b0-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ea6b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea6b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6b0-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="ea6b0-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





