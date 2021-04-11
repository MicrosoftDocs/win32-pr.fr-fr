---
title: IMsRdpClientAdvancedSettings5 propriété RedirectPOSDevices
description: Définit ou récupère la configuration pour la redirection de périphérique de point de service.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectPOSDevices
- Services Bureau à distance de la propriété RedirectPOSDevices, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectPOSDevices
- Services Bureau à distance de la propriété RedirectPOSDevices, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectPOSDevices
- Services Bureau à distance de la propriété RedirectPOSDevices, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectPOSDevices
- Services Bureau à distance de la propriété RedirectPOSDevices, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectPOSDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104626"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="1e683-112">IMsRdpClientAdvancedSettings5 :: RedirectPOSDevices, propriété</span><span class="sxs-lookup"><span data-stu-id="1e683-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="1e683-113">Définit ou récupère la configuration pour la redirection de périphérique de point de service.</span><span class="sxs-lookup"><span data-stu-id="1e683-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="1e683-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1e683-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e683-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e683-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="1e683-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1e683-116">Property value</span></span>

<span data-ttu-id="1e683-117">Définit le mode de redirection du périphérique de point de service sur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="1e683-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="1e683-118">Si la valeur est **true**, le mode de redirection du périphérique de point de service est activé.</span><span class="sxs-lookup"><span data-stu-id="1e683-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e683-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e683-119">Requirements</span></span>



| <span data-ttu-id="1e683-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e683-120">Requirement</span></span> | <span data-ttu-id="1e683-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e683-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e683-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e683-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e683-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e683-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1e683-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e683-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e683-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e683-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1e683-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1e683-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e683-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e683-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1e683-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1e683-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e683-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e683-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1e683-130">IID</span><span class="sxs-lookup"><span data-stu-id="1e683-130">IID</span></span><br/>                      | <span data-ttu-id="1e683-131">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1e683-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e683-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e683-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e683-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1e683-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1e683-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1e683-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1e683-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1e683-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1e683-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1e683-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





