---
title: Méthode FindLicenseServers de la classe Win32_TerminalServiceSetting
description: Énumère tous les serveurs de licences Bureau à distance et la méthode de découverte.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FindLicenseServers
- Services Bureau à distance de la méthode FindLicenseServers, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942725"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="92a34-106">Méthode FindLicenseServers de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="92a34-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="92a34-107">Énumère tous les serveurs de licences Bureau à distance et la méthode de découverte.</span><span class="sxs-lookup"><span data-stu-id="92a34-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a34-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92a34-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="92a34-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92a34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a34-110">*LicenseServersList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92a34-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a34-111">Liste des objets [**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="92a34-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="92a34-112">Chaque objet de la liste de sortie a le nom du serveur de licences Bureau à distance, ainsi que la méthode de découverte.</span><span class="sxs-lookup"><span data-stu-id="92a34-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="92a34-113">*Nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92a34-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a34-114">Nombre total de serveurs de licences Bureau à distance détectés dans la liste de sortie.</span><span class="sxs-lookup"><span data-stu-id="92a34-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92a34-115">Notes</span><span class="sxs-lookup"><span data-stu-id="92a34-115">Remarks</span></span>

<span data-ttu-id="92a34-116">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="92a34-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="92a34-117">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="92a34-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="92a34-118">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="92a34-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="92a34-119">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="92a34-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="92a34-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="92a34-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="92a34-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="92a34-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="92a34-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="92a34-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="92a34-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="92a34-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="92a34-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92a34-124">Requirements</span></span>



| <span data-ttu-id="92a34-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92a34-125">Requirement</span></span> | <span data-ttu-id="92a34-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="92a34-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92a34-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a34-127">Minimum supported client</span></span><br/> | <span data-ttu-id="92a34-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92a34-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92a34-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92a34-129">Minimum supported server</span></span><br/> | <span data-ttu-id="92a34-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92a34-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92a34-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92a34-131">Namespace</span></span><br/>                | <span data-ttu-id="92a34-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="92a34-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="92a34-133">MOF</span><span class="sxs-lookup"><span data-stu-id="92a34-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92a34-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92a34-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="92a34-135">DLL</span><span class="sxs-lookup"><span data-stu-id="92a34-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a34-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a34-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a34-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a34-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a34-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="92a34-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

