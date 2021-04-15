---
title: Méthode SetDisableForcibleLogoff de la classe Win32_TerminalServiceSetting
description: Cette méthode n'est pas prise en charge.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDisableForcibleLogoff
- Services Bureau à distance de la méthode SetDisableForcibleLogoff, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465099"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c7570-106">Méthode SetDisableForcibleLogoff de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="c7570-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c7570-107">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c7570-107">This method is not supported.</span></span>

<span data-ttu-id="c7570-108">**Windows Vista et Windows Server 2008 :** Active ou désactive si un administrateur connecté à la console peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c7570-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7570-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7570-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="c7570-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7570-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7570-111">*DisableForcibleLogoff* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7570-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7570-112">Indicateur de désactivation ou d’activation de la propriété **DisableForcibleLogoff** , qui détermine si un administrateur connecté à la console peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c7570-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c7570-113"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="c7570-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c7570-114">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="c7570-114">Disable the property.</span></span> <span data-ttu-id="c7570-115">L’administrateur connecté peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c7570-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c7570-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c7570-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c7570-117">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="c7570-117">Enable the property.</span></span> <span data-ttu-id="c7570-118">L’administrateur connecté ne peut pas être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="c7570-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7570-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7570-119">Return value</span></span>

<span data-ttu-id="c7570-120">Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="c7570-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="c7570-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c7570-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7570-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7570-122">Requirements</span></span>



| <span data-ttu-id="c7570-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7570-123">Requirement</span></span> | <span data-ttu-id="c7570-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7570-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7570-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7570-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c7570-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7570-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7570-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7570-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c7570-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7570-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7570-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c7570-129">End of client support</span></span><br/>    | <span data-ttu-id="c7570-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7570-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7570-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c7570-131">End of server support</span></span><br/>    | <span data-ttu-id="c7570-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7570-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7570-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7570-133">Namespace</span></span><br/>                | <span data-ttu-id="c7570-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c7570-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c7570-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c7570-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7570-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7570-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7570-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7570-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7570-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7570-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7570-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7570-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7570-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c7570-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





