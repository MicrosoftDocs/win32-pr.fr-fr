---
title: IMsRdpClientAdvancedSettings6 propriété HotKeyFocusReleaseLeft
description: Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + gauche.
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyFocusReleaseLeft
- Services Bureau à distance de la propriété HotKeyFocusReleaseLeft, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyFocusReleaseLeft
- Services Bureau à distance de la propriété HotKeyFocusReleaseLeft, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyFocusReleaseLeft
- Services Bureau à distance de la propriété HotKeyFocusReleaseLeft, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyFocusReleaseLeft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740005"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a><span data-ttu-id="2fa04-110">IMsRdpClientAdvancedSettings6 :: HotKeyFocusReleaseLeft, propriété</span><span class="sxs-lookup"><span data-stu-id="2fa04-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseLeft property</span></span>

<span data-ttu-id="2fa04-111">Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + gauche.</span><span class="sxs-lookup"><span data-stu-id="2fa04-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Left Arrow.</span></span>

<span data-ttu-id="2fa04-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2fa04-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa04-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fa04-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a><span data-ttu-id="2fa04-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2fa04-114">Property value</span></span>

<span data-ttu-id="2fa04-115">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2fa04-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa04-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2fa04-116">Remarks</span></span>

<span data-ttu-id="2fa04-117">Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.</span><span class="sxs-lookup"><span data-stu-id="2fa04-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa04-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fa04-118">Requirements</span></span>



| <span data-ttu-id="2fa04-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fa04-119">Requirement</span></span> | <span data-ttu-id="2fa04-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fa04-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa04-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fa04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa04-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fa04-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="2fa04-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fa04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa04-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fa04-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="2fa04-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2fa04-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2fa04-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fa04-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2fa04-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2fa04-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fa04-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fa04-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="2fa04-129">IID</span><span class="sxs-lookup"><span data-stu-id="2fa04-129">IID</span></span><br/>                      | <span data-ttu-id="2fa04-130">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="2fa04-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2fa04-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa04-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa04-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2fa04-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2fa04-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2fa04-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2fa04-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2fa04-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





