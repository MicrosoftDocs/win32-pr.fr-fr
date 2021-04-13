---
title: IMsRdpClientNonScriptable3 propriété DriveCollection
description: Récupère la collection d’objets Drive à rediriger.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété DriveCollection
- Services Bureau à distance de la propriété DriveCollection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété DriveCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464686"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="0c5b8-120">IMsRdpClientNonScriptable3 ::D propriété riveCollection</span><span class="sxs-lookup"><span data-stu-id="0c5b8-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="0c5b8-121">Récupère la collection d’objets Drive à rediriger.</span><span class="sxs-lookup"><span data-stu-id="0c5b8-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="0c5b8-122">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0c5b8-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5b8-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c5b8-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="0c5b8-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0c5b8-124">Property value</span></span>

<span data-ttu-id="0c5b8-125">Récupère la collection d’objets Drive de type [**IMSRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="0c5b8-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c5b8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c5b8-126">Requirements</span></span>



| <span data-ttu-id="0c5b8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c5b8-127">Requirement</span></span> | <span data-ttu-id="0c5b8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c5b8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5b8-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c5b8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5b8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c5b8-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0c5b8-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c5b8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5b8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c5b8-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0c5b8-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0c5b8-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c5b8-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c5b8-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0c5b8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0c5b8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c5b8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c5b8-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0c5b8-137">IID</span><span class="sxs-lookup"><span data-stu-id="0c5b8-137">IID</span></span><br/>                      | <span data-ttu-id="0c5b8-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="0c5b8-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c5b8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c5b8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5b8-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0c5b8-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="0c5b8-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0c5b8-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="0c5b8-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="0c5b8-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





