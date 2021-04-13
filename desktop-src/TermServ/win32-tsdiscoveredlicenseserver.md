---
title: Classe Win32_TSDiscoveredLicenseServer
description: Fournit des détails sur le serveur de licences Bureau à distance détecté.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer de la classe Services Bureau à distance
- Win32_TSDiscoveredLicenseServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466714"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="18b23-105">\_Classe TSDiscoveredLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="18b23-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="18b23-106">Fournit des détails sur le serveur de licences Bureau à distance détecté.</span><span class="sxs-lookup"><span data-stu-id="18b23-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b23-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18b23-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="18b23-108">Membres</span><span class="sxs-lookup"><span data-stu-id="18b23-108">Members</span></span>

<span data-ttu-id="18b23-109">La classe **Win32 \_ TSDiscoveredLicenseServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18b23-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="18b23-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18b23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18b23-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18b23-111">Properties</span></span>

<span data-ttu-id="18b23-112">La classe **Win32 \_ TSDiscoveredLicenseServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="18b23-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18b23-113">**HowDiscovered**</span><span class="sxs-lookup"><span data-stu-id="18b23-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b23-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18b23-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18b23-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18b23-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b23-116">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="18b23-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="18b23-117">Cette propriété n'est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18b23-117">This property is no longer supported.</span></span>

<span data-ttu-id="18b23-118">**Windows Server 2008 :** Méthode de découverte du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18b23-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="18b23-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span><span class="sxs-lookup"><span data-stu-id="18b23-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-120">Le serveur de licences a été découvert à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="18b23-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="18b23-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span><span class="sxs-lookup"><span data-stu-id="18b23-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-122">Le serveur de licences a été découvert à l’aide d’un paramètre du Registre.</span><span class="sxs-lookup"><span data-stu-id="18b23-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="18b23-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span><span class="sxs-lookup"><span data-stu-id="18b23-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-124">Le serveur de licences a été découvert à l’aide de l’étendue de la découverte du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="18b23-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="18b23-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span><span class="sxs-lookup"><span data-stu-id="18b23-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-126">Le serveur de licences a été découvert à l’aide de l’étendue de découverte du domaine.</span><span class="sxs-lookup"><span data-stu-id="18b23-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="18b23-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span><span class="sxs-lookup"><span data-stu-id="18b23-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-128">Le serveur de licences a été découvert à l’aide de l’étendue de la découverte de forêt.</span><span class="sxs-lookup"><span data-stu-id="18b23-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18b23-129">**IsAdminOnLS**</span><span class="sxs-lookup"><span data-stu-id="18b23-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b23-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18b23-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18b23-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18b23-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b23-132">Indique si le compte utilisé pour exécuter le script ou le fichier. exe qui utilise la classe **Win32 \_ TSDiscoveredLicenseServer** dispose d’un accès administrateur au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="18b23-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="18b23-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**Non** (0)</span><span class="sxs-lookup"><span data-stu-id="18b23-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-134">Le compte utilisé ne dispose pas d’un accès administrateur au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="18b23-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="18b23-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Oui** (1)</span><span class="sxs-lookup"><span data-stu-id="18b23-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-136">Le compte utilisé dispose d’un accès administrateur au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="18b23-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="18b23-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Je ne **sais** pas (2)</span><span class="sxs-lookup"><span data-stu-id="18b23-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-138">Il n’est pas possible de déterminer si le compte utilisé dispose d’un accès administrateur au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="18b23-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18b23-139">**IsLSAvailable**</span><span class="sxs-lookup"><span data-stu-id="18b23-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b23-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18b23-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18b23-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18b23-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b23-142">Indique si le serveur de licences est disponible (qu’une connexion RPC d’appel de procédure distante \[ \] puisse être établie au serveur).</span><span class="sxs-lookup"><span data-stu-id="18b23-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="18b23-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="18b23-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-144">Le serveur de licences n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="18b23-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="18b23-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="18b23-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-146">Le serveur de licences est disponible.</span><span class="sxs-lookup"><span data-stu-id="18b23-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18b23-147">**IssuingCALs**</span><span class="sxs-lookup"><span data-stu-id="18b23-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b23-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18b23-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18b23-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18b23-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b23-150">Indique si le serveur de licences est autorisé à émettre des licences d’accès client (CAL) Services Bureau à distance au serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18b23-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="18b23-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non autorisé** (0)</span><span class="sxs-lookup"><span data-stu-id="18b23-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-152">Le serveur de licences n’est pas autorisé à émettre des licences d’accès client aux services Bureau à distance au serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18b23-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="18b23-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Autorisé** (1)</span><span class="sxs-lookup"><span data-stu-id="18b23-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-154">Le serveur de licences est autorisé à émettre des licences d’accès client aux services Bureau à distance au serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18b23-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="18b23-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Je ne **sais** pas (2)</span><span class="sxs-lookup"><span data-stu-id="18b23-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18b23-156">Il n’est pas possible de déterminer si le serveur de licences est autorisé à émettre des licences d’accès client aux services Bureau à distance au serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18b23-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18b23-157">**LicenseServer**</span><span class="sxs-lookup"><span data-stu-id="18b23-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b23-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18b23-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b23-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18b23-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b23-160">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18b23-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18b23-161">Nom du serveur de licences Bureau à distance détecté.</span><span class="sxs-lookup"><span data-stu-id="18b23-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18b23-162">Notes</span><span class="sxs-lookup"><span data-stu-id="18b23-162">Remarks</span></span>

<span data-ttu-id="18b23-163">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="18b23-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="18b23-164">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="18b23-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="18b23-165">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="18b23-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="18b23-166">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="18b23-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="18b23-167">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="18b23-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18b23-168">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18b23-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18b23-169">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="18b23-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18b23-170">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18b23-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18b23-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18b23-171">Requirements</span></span>



| <span data-ttu-id="18b23-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18b23-172">Requirement</span></span> | <span data-ttu-id="18b23-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="18b23-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b23-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18b23-174">Minimum supported client</span></span><br/> | <span data-ttu-id="18b23-175">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18b23-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="18b23-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18b23-176">Minimum supported server</span></span><br/> | <span data-ttu-id="18b23-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18b23-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18b23-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18b23-178">Namespace</span></span><br/>                | <span data-ttu-id="18b23-179">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="18b23-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="18b23-180">MOF</span><span class="sxs-lookup"><span data-stu-id="18b23-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18b23-181"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18b23-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="18b23-182">DLL</span><span class="sxs-lookup"><span data-stu-id="18b23-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b23-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b23-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

