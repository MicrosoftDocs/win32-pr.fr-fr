---
title: Méthode SetDisableForcibleLogoff de la classe Win32_TerminalServiceSetting
description: Méthode SetDisableForcibleLogoff de la classe Win32_TerminalServiceSetting-cette méthode n’est pas prise en charge.
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
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103707"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="23445-106">Méthode SetDisableForcibleLogoff de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="23445-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="23445-107">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23445-107">This method is not supported.</span></span>

<span data-ttu-id="23445-108">**Windows Vista et Windows Server 2008 :** Active ou désactive si un administrateur connecté à la console peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="23445-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="23445-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23445-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="23445-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23445-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23445-111">*DisableForcibleLogoff* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23445-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23445-112">Indicateur de désactivation ou d’activation de la propriété **DisableForcibleLogoff** , qui détermine si un administrateur connecté à la console peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="23445-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="23445-113"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="23445-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="23445-114">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="23445-114">Disable the property.</span></span> <span data-ttu-id="23445-115">L’administrateur connecté peut être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="23445-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="23445-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="23445-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="23445-117">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="23445-117">Enable the property.</span></span> <span data-ttu-id="23445-118">L’administrateur connecté ne peut pas être déconnecté de force.</span><span class="sxs-lookup"><span data-stu-id="23445-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23445-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23445-119">Return value</span></span>

<span data-ttu-id="23445-120">Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="23445-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="23445-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="23445-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="23445-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23445-122">Requirements</span></span>



| <span data-ttu-id="23445-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23445-123">Requirement</span></span> | <span data-ttu-id="23445-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="23445-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23445-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23445-125">Minimum supported client</span></span><br/> | <span data-ttu-id="23445-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23445-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23445-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23445-127">Minimum supported server</span></span><br/> | <span data-ttu-id="23445-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23445-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23445-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="23445-129">End of client support</span></span><br/>    | <span data-ttu-id="23445-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23445-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23445-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="23445-131">End of server support</span></span><br/>    | <span data-ttu-id="23445-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23445-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23445-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23445-133">Namespace</span></span><br/>                | <span data-ttu-id="23445-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="23445-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="23445-135">MOF</span><span class="sxs-lookup"><span data-stu-id="23445-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23445-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23445-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="23445-137">DLL</span><span class="sxs-lookup"><span data-stu-id="23445-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23445-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23445-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23445-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23445-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23445-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="23445-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





