---
title: IMsRdpClientAdvancedSettings5 propriété RedirectDevices
description: Définit ou récupère la configuration pour la redirection de périphérique.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDevices
- Services Bureau à distance de la propriété RedirectDevices, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectDevices
- Services Bureau à distance de la propriété RedirectDevices, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectDevices
- Services Bureau à distance de la propriété RedirectDevices, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectDevices
- Services Bureau à distance de la propriété RedirectDevices, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509909"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="bcd39-112">IMsRdpClientAdvancedSettings5 :: RedirectDevices, propriété</span><span class="sxs-lookup"><span data-stu-id="bcd39-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="bcd39-113">Définit ou récupère la configuration pour la redirection de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bcd39-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="bcd39-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bcd39-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd39-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcd39-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="bcd39-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bcd39-116">Property value</span></span>

<span data-ttu-id="bcd39-117">Définit le mode de redirection de périphérique sur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="bcd39-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="bcd39-118">Si la valeur est **true**, le mode de redirection de périphérique est activé.</span><span class="sxs-lookup"><span data-stu-id="bcd39-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd39-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcd39-119">Requirements</span></span>



| <span data-ttu-id="bcd39-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcd39-120">Requirement</span></span> | <span data-ttu-id="bcd39-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcd39-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd39-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcd39-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd39-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcd39-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bcd39-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcd39-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd39-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcd39-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bcd39-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bcd39-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcd39-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd39-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcd39-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd39-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd39-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd39-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcd39-130">IID</span><span class="sxs-lookup"><span data-stu-id="bcd39-130">IID</span></span><br/>                      | <span data-ttu-id="bcd39-131">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="bcd39-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcd39-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcd39-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd39-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bcd39-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bcd39-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bcd39-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bcd39-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bcd39-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bcd39-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bcd39-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





