---
title: IMsRdpClientAdvancedSettings5 propriété ConnectionBarShowPinButton
description: Définit ou récupère la configuration du bouton épingler dans la barre de connexion.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512561"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="09644-112">IMsRdpClientAdvancedSettings5 :: ConnectionBarShowPinButton, propriété</span><span class="sxs-lookup"><span data-stu-id="09644-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="09644-113">Définit ou récupère la configuration du bouton épingler dans la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="09644-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="09644-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="09644-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="09644-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09644-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="09644-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="09644-116">Property value</span></span>

<span data-ttu-id="09644-117">Valeur booléenne **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="09644-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="09644-118">La valeur **true** affiche le bouton épingler dans la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="09644-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="09644-119">La valeur **false** masque le bouton épingler dans la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="09644-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="09644-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09644-120">Requirements</span></span>



| <span data-ttu-id="09644-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09644-121">Requirement</span></span> | <span data-ttu-id="09644-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="09644-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09644-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09644-123">Minimum supported client</span></span><br/> | <span data-ttu-id="09644-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09644-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="09644-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09644-125">Minimum supported server</span></span><br/> | <span data-ttu-id="09644-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09644-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="09644-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="09644-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="09644-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09644-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="09644-129">DLL</span><span class="sxs-lookup"><span data-stu-id="09644-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09644-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09644-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="09644-131">IID</span><span class="sxs-lookup"><span data-stu-id="09644-131">IID</span></span><br/>                      | <span data-ttu-id="09644-132">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="09644-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09644-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09644-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09644-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="09644-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="09644-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="09644-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="09644-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="09644-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="09644-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="09644-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





