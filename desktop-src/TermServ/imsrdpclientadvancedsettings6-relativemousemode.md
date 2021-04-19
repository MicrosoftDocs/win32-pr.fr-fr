---
title: IMsRdpClientAdvancedSettings6 propriété RelativeMouseMode
description: Spécifie si la souris doit utiliser le mode relatif.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511372"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a><span data-ttu-id="ab50b-110">IMsRdpClientAdvancedSettings6 :: RelativeMouseMode, propriété</span><span class="sxs-lookup"><span data-stu-id="ab50b-110">IMsRdpClientAdvancedSettings6::RelativeMouseMode property</span></span>

<span data-ttu-id="ab50b-111">Spécifie si la souris doit utiliser le mode relatif.</span><span class="sxs-lookup"><span data-stu-id="ab50b-111">Specifies whether the mouse should use relative mode.</span></span> <span data-ttu-id="ab50b-112">Contient **la \_ valeur variant true** si la souris est en mode relatif ou **\_ false** si la souris est en mode absolu.</span><span class="sxs-lookup"><span data-stu-id="ab50b-112">Contains **VARIANT\_TRUE** if the mouse is in relative mode or **VARIANT\_FALSE** if the mouse is in absolute mode.</span></span>

<span data-ttu-id="ab50b-113">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ab50b-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab50b-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab50b-114">Syntax</span></span>


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a><span data-ttu-id="ab50b-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ab50b-115">Property value</span></span>

<span data-ttu-id="ab50b-116">Contient la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ab50b-116">Contains the new property value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab50b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ab50b-117">Remarks</span></span>

<span data-ttu-id="ab50b-118">Le mode de la souris indique comment le contrôle ActiveX calcule les coordonnées de la souris qu’il envoie au serveur Bureau à distance hôte de session (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="ab50b-118">The mouse mode indicates how the ActiveX control calculates the mouse coordinates that it sends to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="ab50b-119">Lorsque la souris est en mode relatif, le contrôle ActiveX calcule les coordonnées de la souris par rapport à la dernière position de la souris.</span><span class="sxs-lookup"><span data-stu-id="ab50b-119">When the mouse is in relative mode, the ActiveX control calculates mouse coordinates relative to the mouse's last position.</span></span> <span data-ttu-id="ab50b-120">Lorsque la souris est en mode absolu, le contrôle ActiveX calcule les coordonnées de la souris par rapport au Bureau du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ab50b-120">When the mouse is in absolute mode, the ActiveX control calculates mouse coordinates relative to the desktop of the RD Session Host server.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab50b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab50b-121">Requirements</span></span>



| <span data-ttu-id="ab50b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab50b-122">Requirement</span></span> | <span data-ttu-id="ab50b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab50b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab50b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab50b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab50b-125">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="ab50b-125">Windows Vista with SP1</span></span><br/>                                                                |
| <span data-ttu-id="ab50b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab50b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab50b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab50b-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ab50b-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ab50b-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab50b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab50b-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ab50b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ab50b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab50b-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab50b-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ab50b-132">IID</span><span class="sxs-lookup"><span data-stu-id="ab50b-132">IID</span></span><br/>                      | <span data-ttu-id="ab50b-133">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="ab50b-133">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab50b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab50b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab50b-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ab50b-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ab50b-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ab50b-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ab50b-137">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ab50b-137">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





