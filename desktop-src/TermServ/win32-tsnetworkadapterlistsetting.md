---
title: Classe Win32_TSNetworkAdapterListSetting
description: Énumère la liste des cartes réseau qui peuvent être configurées pour un terminal Win32 \_ , selon le protocole terminal et la méthode de transport spécifiés.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterListSetting de la classe Services Bureau à distance
- Win32_TSNetworkAdapterListSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510759"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="6f7fc-105">\_Classe TSNetworkAdapterListSetting Win32</span><span class="sxs-lookup"><span data-stu-id="6f7fc-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="6f7fc-106">La classe WMI **\_ TSNetworkAdapterListSetting** WMI énumère la liste des cartes réseau qui peuvent être configurées pour un [**\_ Terminal Win32**](win32-terminal.md), en fonction du protocole terminal et de la méthode de transport spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="6f7fc-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7fc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f7fc-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="6f7fc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6f7fc-109">Members</span></span>

<span data-ttu-id="6f7fc-110">La classe **Win32 \_ TSNetworkAdapterListSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f7fc-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6f7fc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f7fc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f7fc-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f7fc-112">Properties</span></span>

<span data-ttu-id="6f7fc-113">La classe **Win32 \_ TSNetworkAdapterListSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f7fc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6f7fc-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-123">Description of the object.</span></span>

<span data-ttu-id="6f7fc-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="6f7fc-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-129">The date the object was installed.</span></span> <span data-ttu-id="6f7fc-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6f7fc-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-135">The name of the object.</span></span>

<span data-ttu-id="6f7fc-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-140">GUID de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-141">**NetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-144">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-145">Adresse IP de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6f7fc-146">**État**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-149">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-150">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-150">Current status of the object.</span></span> <span data-ttu-id="6f7fc-151">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6f7fc-152">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6f7fc-153">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6f7fc-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6f7fc-154">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6f7fc-155">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6f7fc-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6f7fc-157">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-158">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-159">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-160">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="6f7fc-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-161">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-162">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-163">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6f7fc-164">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="6f7fc-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f7fc-165">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7fc-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7fc-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6f7fc-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7fc-168">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-168">The name of the terminal.</span></span>

<span data-ttu-id="6f7fc-169">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f7fc-170">Notes</span><span class="sxs-lookup"><span data-stu-id="6f7fc-170">Remarks</span></span>

<span data-ttu-id="6f7fc-171">Pour se connecter à l’espace de noms « root \\ cimv2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6f7fc-172">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="6f7fc-173">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="6f7fc-174">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6f7fc-175">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6f7fc-176">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6f7fc-177">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6f7fc-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6f7fc-178">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6f7fc-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7fc-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f7fc-179">Requirements</span></span>



| <span data-ttu-id="6f7fc-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f7fc-180">Requirement</span></span> | <span data-ttu-id="6f7fc-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f7fc-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7fc-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7fc-182">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7fc-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f7fc-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f7fc-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7fc-184">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7fc-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f7fc-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f7fc-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f7fc-186">Namespace</span></span><br/>                | <span data-ttu-id="6f7fc-187">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="6f7fc-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6f7fc-188">MOF</span><span class="sxs-lookup"><span data-stu-id="6f7fc-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f7fc-189"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f7fc-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f7fc-190">DLL</span><span class="sxs-lookup"><span data-stu-id="6f7fc-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f7fc-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f7fc-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f7fc-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f7fc-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7fc-193">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="6f7fc-194">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6f7fc-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

