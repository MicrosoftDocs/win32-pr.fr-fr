---
title: IMsRdpClientAdvancedSettings6 propriété HotKeyFocusReleaseRight
description: Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour Ctrl + Alt + droite.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513036"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a><span data-ttu-id="fd007-110">IMsRdpClientAdvancedSettings6 :: HotKeyFocusReleaseRight, propriété</span><span class="sxs-lookup"><span data-stu-id="fd007-110">IMsRdpClientAdvancedSettings6::HotKeyFocusReleaseRight property</span></span>

<span data-ttu-id="fd007-111">Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour Ctrl + Alt + droite.</span><span class="sxs-lookup"><span data-stu-id="fd007-111">Specifies the virtual-key code to add to Ctrl+Alt to determine the hotkey replacement for Ctrl+Alt+Right Arrow.</span></span>

<span data-ttu-id="fd007-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fd007-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd007-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd007-113">Syntax</span></span>


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a><span data-ttu-id="fd007-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fd007-114">Property value</span></span>

<span data-ttu-id="fd007-115">Nouveau code de la clé virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fd007-115">The new virtual-key code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd007-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fd007-116">Remarks</span></span>

<span data-ttu-id="fd007-117">Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.</span><span class="sxs-lookup"><span data-stu-id="fd007-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd007-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd007-118">Requirements</span></span>



| <span data-ttu-id="fd007-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd007-119">Requirement</span></span> | <span data-ttu-id="fd007-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd007-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd007-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd007-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd007-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd007-122">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="fd007-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd007-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd007-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd007-124">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="fd007-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fd007-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd007-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd007-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fd007-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fd007-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd007-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd007-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fd007-129">IID</span><span class="sxs-lookup"><span data-stu-id="fd007-129">IID</span></span><br/>                      | <span data-ttu-id="fd007-130">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="fd007-130">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd007-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd007-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd007-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fd007-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fd007-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fd007-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fd007-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fd007-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





