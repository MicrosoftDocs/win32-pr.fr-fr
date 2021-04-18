---
title: Méthode ConnectionSettings de la classe Win32_TSClientSetting
description: La méthode ConnectionSettings définit les paramètres de session qui s’appliquent au processus de connexion et d’ouverture de session.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ConnectionSettings
- Services Bureau à distance de la méthode ConnectionSettings, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508506"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="30bb0-106">Méthode ConnectionSettings de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="30bb0-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="30bb0-107">La méthode **ConnectionSettings** définit les paramètres de session qui s’appliquent au processus de connexion et d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="30bb0-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bb0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30bb0-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="30bb0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30bb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bb0-110">*ConnectClientDrivesAtLogon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30bb0-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bb0-111">Indicateur d’activation ou de désactivation de la propriété **ConnectClientDrivesAtLogon** qui spécifie si les lecteurs du client sont connectés automatiquement au cours de la procédure d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="30bb0-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="30bb0-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="30bb0-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-113">Les lecteurs du client ne sont pas automatiquement connectés.</span><span class="sxs-lookup"><span data-stu-id="30bb0-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="30bb0-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="30bb0-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-115">Les lecteurs du client sont automatiquement connectés.</span><span class="sxs-lookup"><span data-stu-id="30bb0-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="30bb0-116">*ConnectPrinterAtLogon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30bb0-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bb0-117">Indicateur d’activation ou de désactivation de la propriété **ConnectPrinterAtLogon** , qui spécifie si toutes les imprimantes clientes locales mappées sont automatiquement connectées lors de la procédure d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="30bb0-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="30bb0-118"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="30bb0-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-119">Toutes les imprimantes locales mappées ne sont pas automatiquement connectées.</span><span class="sxs-lookup"><span data-stu-id="30bb0-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="30bb0-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="30bb0-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-121">Toutes les imprimantes locales mappées sont automatiquement connectées.</span><span class="sxs-lookup"><span data-stu-id="30bb0-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="30bb0-122">*DefaultToClientPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30bb0-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bb0-123">Indicateur d’activation ou de désactivation de la propriété **DefaultToClientPrinter** qui spécifie si les travaux d’impression sont envoyés automatiquement à l’imprimante locale du client.</span><span class="sxs-lookup"><span data-stu-id="30bb0-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="30bb0-124"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="30bb0-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-125">Les travaux d’impression ne sont pas envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="30bb0-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="30bb0-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="30bb0-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="30bb0-127">Les travaux d’impression sont envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="30bb0-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bb0-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30bb0-128">Return value</span></span>

<span data-ttu-id="30bb0-129">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="30bb0-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="30bb0-130">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="30bb0-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="30bb0-131">La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="30bb0-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bb0-132">Notes</span><span class="sxs-lookup"><span data-stu-id="30bb0-132">Remarks</span></span>

<span data-ttu-id="30bb0-133">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="30bb0-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30bb0-134">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="30bb0-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30bb0-135">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="30bb0-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30bb0-136">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30bb0-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30bb0-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30bb0-137">Requirements</span></span>



| <span data-ttu-id="30bb0-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30bb0-138">Requirement</span></span> | <span data-ttu-id="30bb0-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bb0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30bb0-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bb0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="30bb0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30bb0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30bb0-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bb0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="30bb0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30bb0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30bb0-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30bb0-144">Namespace</span></span><br/>                | <span data-ttu-id="30bb0-145">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="30bb0-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="30bb0-146">MOF</span><span class="sxs-lookup"><span data-stu-id="30bb0-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30bb0-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30bb0-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="30bb0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="30bb0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30bb0-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30bb0-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bb0-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30bb0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bb0-151">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="30bb0-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

