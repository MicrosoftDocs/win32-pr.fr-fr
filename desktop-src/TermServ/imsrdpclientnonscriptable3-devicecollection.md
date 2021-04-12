---
title: IMsRdpClientNonScriptable3 propriété DeviceCollection
description: Récupère la collection d’objets d’appareil Plug-and-Play (PnP) à rediriger.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété DeviceCollection
- Services Bureau à distance de la propriété DeviceCollection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété DeviceCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384179"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="c0ea3-120">IMsRdpClientNonScriptable3 ::D propriété eviceCollection</span><span class="sxs-lookup"><span data-stu-id="c0ea3-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="c0ea3-121">Récupère la collection d’objets d’appareil Plug-and-Play (PnP) à rediriger.</span><span class="sxs-lookup"><span data-stu-id="c0ea3-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="c0ea3-122">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0ea3-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ea3-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0ea3-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c0ea3-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0ea3-124">Property value</span></span>

<span data-ttu-id="c0ea3-125">Récupère la collection d’objets périphériques PnP de type [**IMSRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c0ea3-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ea3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0ea3-126">Requirements</span></span>



| <span data-ttu-id="c0ea3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0ea3-127">Requirement</span></span> | <span data-ttu-id="c0ea3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0ea3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ea3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0ea3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ea3-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0ea3-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c0ea3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0ea3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ea3-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0ea3-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c0ea3-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c0ea3-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0ea3-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea3-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c0ea3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ea3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ea3-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea3-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c0ea3-137">IID</span><span class="sxs-lookup"><span data-stu-id="c0ea3-137">IID</span></span><br/>                      | <span data-ttu-id="c0ea3-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="c0ea3-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0ea3-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0ea3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ea3-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c0ea3-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c0ea3-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c0ea3-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c0ea3-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c0ea3-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





