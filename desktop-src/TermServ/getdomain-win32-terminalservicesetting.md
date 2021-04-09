---
title: Méthode GetDomain de la classe Win32_TerminalServiceSetting
description: Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre.
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetDomain
- Services Bureau à distance de la méthode GetDomain, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetDomain
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941756"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="3ca5e-106">Méthode GetDomain de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="3ca5e-106">GetDomain method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="3ca5e-107">Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-107">Retrieves the name of the domain that the Remote Desktop Session Host (RD Session Host) server is a member of.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca5e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ca5e-108">Syntax</span></span>


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="3ca5e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ca5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca5e-110">*Domaine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ca5e-110">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca5e-111">Nom de domaine du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-111">The domain name of the RD Session Host server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ca5e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca5e-112">Remarks</span></span>

<span data-ttu-id="3ca5e-113">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="3ca5e-114">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="3ca5e-115">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="3ca5e-116">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="3ca5e-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3ca5e-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3ca5e-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3ca5e-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3ca5e-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3ca5e-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca5e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ca5e-121">Requirements</span></span>



| <span data-ttu-id="3ca5e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ca5e-122">Requirement</span></span> | <span data-ttu-id="3ca5e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ca5e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca5e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ca5e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca5e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ca5e-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ca5e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ca5e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca5e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ca5e-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ca5e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ca5e-128">Namespace</span></span><br/>                | <span data-ttu-id="3ca5e-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3ca5e-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3ca5e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3ca5e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ca5e-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5e-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ca5e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca5e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca5e-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5e-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca5e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ca5e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca5e-135">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3ca5e-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

