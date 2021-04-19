---
title: Méthode GetWinstationDriverNames de la classe Win32_TerminalServiceSetting
description: Récupère une liste de noms de pilote de station de noms.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetWinstationDriverNames
- Services Bureau à distance de la méthode GetWinstationDriverNames, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510311"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="60b07-106">Méthode GetWinstationDriverNames de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="60b07-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="60b07-107">Récupère une liste de noms de pilote de station de noms.</span><span class="sxs-lookup"><span data-stu-id="60b07-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b07-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60b07-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="60b07-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60b07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b07-110">*WinstaDriverNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60b07-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b07-111">Liste des noms de pilote de station de noms.</span><span class="sxs-lookup"><span data-stu-id="60b07-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b07-112">Notes</span><span class="sxs-lookup"><span data-stu-id="60b07-112">Remarks</span></span>

<span data-ttu-id="60b07-113">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="60b07-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="60b07-114">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="60b07-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="60b07-115">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="60b07-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="60b07-116">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="60b07-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="60b07-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="60b07-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60b07-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60b07-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60b07-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="60b07-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60b07-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60b07-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60b07-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60b07-121">Requirements</span></span>



| <span data-ttu-id="60b07-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b07-122">Requirement</span></span> | <span data-ttu-id="60b07-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b07-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b07-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b07-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60b07-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60b07-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60b07-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b07-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60b07-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60b07-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60b07-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60b07-128">Namespace</span></span><br/>                | <span data-ttu-id="60b07-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="60b07-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="60b07-130">MOF</span><span class="sxs-lookup"><span data-stu-id="60b07-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b07-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b07-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b07-132">DLL</span><span class="sxs-lookup"><span data-stu-id="60b07-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b07-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b07-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b07-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b07-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b07-135">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="60b07-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

