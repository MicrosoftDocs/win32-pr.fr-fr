---
title: Méthode SetAllowTSConnections de la classe Win32_TerminalServiceSetting
description: La méthode SetAllowTSConnections autorise ou refuse les nouvelles connexions Bureau à distance. Cette méthode modifie la propriété AllowTSConnections de la classe en conséquence.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAllowTSConnections
- Services Bureau à distance de la méthode SetAllowTSConnections, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466719"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="602c1-107">Méthode SetAllowTSConnections de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="602c1-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="602c1-108">La méthode **SetAllowTSConnections** autorise ou refuse les nouvelles connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="602c1-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="602c1-109">Cette méthode modifie la propriété **AllowTSConnections** de la classe en conséquence.</span><span class="sxs-lookup"><span data-stu-id="602c1-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="602c1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="602c1-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="602c1-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="602c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="602c1-112">*AllowTSConnections* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="602c1-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602c1-113">Spécifie si les nouvelles connexions Bureau à distance sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="602c1-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="602c1-114">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="602c1-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="602c1-115"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="602c1-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="602c1-116">Les nouvelles connexions ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="602c1-116">New connections are not allowed.</span></span> <span data-ttu-id="602c1-117">Si le paramètre *ModifyFirewallException* est 1, l’exception de pare-feu Bureau à distance est désactivée.</span><span class="sxs-lookup"><span data-stu-id="602c1-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="602c1-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="602c1-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="602c1-119">Les nouvelles connexions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="602c1-119">New connections are allowed.</span></span> <span data-ttu-id="602c1-120">Si le paramètre *ModifyFirewallException* est 1, l’exception de pare-feu Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="602c1-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="602c1-121">*ModifyFirewallException* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="602c1-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="602c1-122">Spécifie si le paramètre d’exception de pare-feu pour Bureau à distance sera modifié à l’état spécifié par le paramètre *AllowTSConnections* .</span><span class="sxs-lookup"><span data-stu-id="602c1-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="602c1-123">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="602c1-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="602c1-124"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="602c1-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="602c1-125">Ne modifiez pas le paramètre d’exception de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="602c1-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="602c1-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="602c1-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="602c1-127">Modifiez le paramètre d’exception de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="602c1-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="602c1-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="602c1-128">Return value</span></span>

<span data-ttu-id="602c1-129">Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="602c1-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="602c1-130">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="602c1-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="602c1-131">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="602c1-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="602c1-132">Notes</span><span class="sxs-lookup"><span data-stu-id="602c1-132">Remarks</span></span>

<span data-ttu-id="602c1-133">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="602c1-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="602c1-134">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="602c1-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="602c1-135">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="602c1-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="602c1-136">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="602c1-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="602c1-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="602c1-137">Requirements</span></span>



| <span data-ttu-id="602c1-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="602c1-138">Requirement</span></span> | <span data-ttu-id="602c1-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="602c1-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="602c1-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="602c1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="602c1-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="602c1-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="602c1-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="602c1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="602c1-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="602c1-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="602c1-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="602c1-144">Namespace</span></span><br/>                | <span data-ttu-id="602c1-145">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="602c1-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="602c1-146">MOF</span><span class="sxs-lookup"><span data-stu-id="602c1-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="602c1-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="602c1-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="602c1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="602c1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="602c1-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="602c1-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="602c1-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="602c1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602c1-151">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="602c1-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

