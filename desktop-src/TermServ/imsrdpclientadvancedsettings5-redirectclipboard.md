---
title: IMsRdpClientAdvancedSettings5 propriété RedirectClipboard
description: Définit ou récupère la configuration de la redirection du presse-papiers.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectClipboard
- Services Bureau à distance de la propriété RedirectClipboard, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectClipboard
- Services Bureau à distance de la propriété RedirectClipboard, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectClipboard
- Services Bureau à distance de la propriété RedirectClipboard, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectClipboard
- Services Bureau à distance de la propriété RedirectClipboard, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aba9950b8d602ca239d66364279a5876a432d04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941879"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a><span data-ttu-id="df194-112">IMsRdpClientAdvancedSettings5 :: RedirectClipboard, propriété</span><span class="sxs-lookup"><span data-stu-id="df194-112">IMsRdpClientAdvancedSettings5::RedirectClipboard property</span></span>

<span data-ttu-id="df194-113">Définit ou récupère la configuration de la redirection du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="df194-113">Sets or retrieves the configuration for clipboard redirection.</span></span>

<span data-ttu-id="df194-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="df194-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df194-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df194-115">Syntax</span></span>


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a><span data-ttu-id="df194-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="df194-116">Property value</span></span>

<span data-ttu-id="df194-117">Définit le mode de redirection du presse-papiers sur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="df194-117">Sets the clipboard redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="df194-118">Si la valeur est **true**, le mode de redirection du presse-papiers est activé.</span><span class="sxs-lookup"><span data-stu-id="df194-118">If set to **TRUE**, clipboard redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="df194-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df194-119">Requirements</span></span>



| <span data-ttu-id="df194-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df194-120">Requirement</span></span> | <span data-ttu-id="df194-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="df194-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df194-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df194-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df194-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df194-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="df194-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df194-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df194-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df194-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="df194-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="df194-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="df194-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df194-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="df194-128">DLL</span><span class="sxs-lookup"><span data-stu-id="df194-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df194-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df194-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="df194-130">IID</span><span class="sxs-lookup"><span data-stu-id="df194-130">IID</span></span><br/>                      | <span data-ttu-id="df194-131">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="df194-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df194-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df194-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df194-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="df194-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="df194-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="df194-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="df194-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="df194-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="df194-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="df194-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





