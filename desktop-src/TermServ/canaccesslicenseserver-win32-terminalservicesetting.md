---
title: Méthode CanAccessLicenseServer de la classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer n’est plus disponible.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanAccessLicenseServer
- Services Bureau à distance de la méthode CanAccessLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103173"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="1166e-106">Méthode CanAccessLicenseServer de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="1166e-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="1166e-107">\[**CanAccessLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="1166e-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="1166e-108">\* \* Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="1166e-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="1166e-109">Détermine si le Bureau à distance serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander Services Bureau à distance des licences d’accès client (CAL RDS) à partir d’un serveur de licences Bureau à distance en fonction des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1166e-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="1166e-110">Paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1166e-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="1166e-111">Appartenance au groupe local ordinateurs Terminal Server sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1166e-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1166e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1166e-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="1166e-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1166e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1166e-114">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1166e-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1166e-115">Nom du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1166e-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="1166e-116">*AccessAllowed* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1166e-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1166e-117">Si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client aux services Bureau à distance à partir du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1166e-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="1166e-118">0</span><span class="sxs-lookup"><span data-stu-id="1166e-118">0</span></span>
</dt> <dd>

<span data-ttu-id="1166e-119">La demande est autorisée.</span><span class="sxs-lookup"><span data-stu-id="1166e-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="1166e-120">1</span><span class="sxs-lookup"><span data-stu-id="1166e-120">1</span></span>
</dt> <dd>

<span data-ttu-id="1166e-121">La demande n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="1166e-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1166e-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1166e-122">Return value</span></span>

<span data-ttu-id="1166e-123">Retourne la valeur **\_ OK** si le serveur hôte de session Bureau à distance a accès au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1166e-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="1166e-124">Retourne **la \_ valeur S false** si le serveur hôte de session Bureau à distance n’a pas accès au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1166e-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="1166e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1166e-125">Remarks</span></span>

<span data-ttu-id="1166e-126">Le paramètre de stratégie « Groupe de sécurité du serveur de licences » vous permet de spécifier les serveurs hôtes de session Bureau à distance qui sont autorisés à contacter le serveur de licences pour obtenir des licences d’accès client aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1166e-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="1166e-127">Si le paramètre de stratégie est activé sur le serveur de licences, le serveur de licences répond uniquement aux demandes de licences d’accès client aux services Bureau à distance des serveurs hôtes de session Bureau à distance dont les comptes d’ordinateur sont membres du groupe local ordinateurs Terminal Server sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1166e-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="1166e-128">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="1166e-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="1166e-129">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="1166e-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="1166e-130">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="1166e-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="1166e-131">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="1166e-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="1166e-132">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1166e-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1166e-133">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1166e-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1166e-134">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1166e-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1166e-135">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1166e-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1166e-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1166e-136">Requirements</span></span>



| <span data-ttu-id="1166e-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1166e-137">Requirement</span></span> | <span data-ttu-id="1166e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="1166e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1166e-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1166e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1166e-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1166e-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1166e-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1166e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1166e-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1166e-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1166e-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1166e-143">End of client support</span></span><br/>    | <span data-ttu-id="1166e-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1166e-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1166e-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1166e-145">End of server support</span></span><br/>    | <span data-ttu-id="1166e-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1166e-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1166e-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1166e-147">Namespace</span></span><br/>                | <span data-ttu-id="1166e-148">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1166e-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1166e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="1166e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1166e-150"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1166e-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1166e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1166e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1166e-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1166e-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1166e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1166e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1166e-154">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1166e-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

