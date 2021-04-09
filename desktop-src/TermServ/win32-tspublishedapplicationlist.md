---
title: Classe Win32_TSPublishedApplicationList
description: Représente la liste des programmes qui se trouvent dans la liste programmes RemoteApp sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList de la classe Services Bureau à distance
- Win32_TSPublishedApplicationList de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032727"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="70363-105">\_Classe TSPublishedApplicationList Win32</span><span class="sxs-lookup"><span data-stu-id="70363-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="70363-106">Représente la liste des programmes qui se trouvent dans la liste programmes RemoteApp sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="70363-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="70363-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70363-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="70363-108">Membres</span><span class="sxs-lookup"><span data-stu-id="70363-108">Members</span></span>

<span data-ttu-id="70363-109">La classe **Win32 \_ TSPublishedApplicationList** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70363-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="70363-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70363-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70363-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70363-111">Properties</span></span>

<span data-ttu-id="70363-112">La classe **Win32 \_ TSPublishedApplicationList** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70363-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70363-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="70363-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70363-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70363-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70363-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="70363-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="70363-117">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70363-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="70363-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70363-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70363-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="70363-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70363-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70363-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70363-122">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70363-122">Description of the object.</span></span>

<span data-ttu-id="70363-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70363-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70363-124">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="70363-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-125">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70363-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70363-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70363-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="70363-127">Indique si le serveur hôte de session Bureau à distance restreint les programmes qu’un utilisateur peut démarrer lors de la connexion initiale aux programmes figurant dans la liste des programmes RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70363-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="70363-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="70363-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-129">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70363-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70363-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70363-131">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="70363-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="70363-132">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="70363-132">The date the object was installed.</span></span> <span data-ttu-id="70363-133">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="70363-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="70363-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70363-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70363-135">**Nom**</span><span class="sxs-lookup"><span data-stu-id="70363-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70363-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70363-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70363-138">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="70363-138">The name of the object.</span></span>

<span data-ttu-id="70363-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70363-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="70363-140">**PolicySourceDisabled**</span><span class="sxs-lookup"><span data-stu-id="70363-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70363-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70363-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70363-143">Indique l’emplacement où la propriété **Disabled** est configurée.</span><span class="sxs-lookup"><span data-stu-id="70363-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="70363-144">Les valeurs possibles incluent :</span><span class="sxs-lookup"><span data-stu-id="70363-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="70363-145">0</span><span class="sxs-lookup"><span data-stu-id="70363-145">0</span></span>
</dt> <dd>

<span data-ttu-id="70363-146">Le paramètre est configuré sur le serveur via Gestionnaire RemoteApp ou le fournisseur WMI RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70363-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="70363-147">1</span><span class="sxs-lookup"><span data-stu-id="70363-147">1</span></span>
</dt> <dd>

<span data-ttu-id="70363-148">Le paramètre est configuré via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="70363-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="70363-149">2</span><span class="sxs-lookup"><span data-stu-id="70363-149">2</span></span>
</dt> <dd>

<span data-ttu-id="70363-150">Le paramètre n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="70363-150">The setting is not configured.</span></span> <span data-ttu-id="70363-151">La valeur par défaut **false** est utilisée pour la propriété **Disabled** .</span><span class="sxs-lookup"><span data-stu-id="70363-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="70363-152">**État**</span><span class="sxs-lookup"><span data-stu-id="70363-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70363-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70363-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70363-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70363-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70363-155">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="70363-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="70363-156">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70363-156">Current status of the object.</span></span> <span data-ttu-id="70363-157">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="70363-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="70363-158">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="70363-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="70363-159">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="70363-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="70363-160">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="70363-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="70363-161">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="70363-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="70363-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="70363-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="70363-163">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="70363-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-164">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="70363-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-165">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="70363-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-166">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="70363-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-167">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="70363-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-168">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="70363-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-169">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="70363-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="70363-170">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="70363-170">("Service")</span></span>


<span data-ttu-id="70363-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="70363-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="70363-172">Notes</span><span class="sxs-lookup"><span data-stu-id="70363-172">Remarks</span></span>

<span data-ttu-id="70363-173">Vous devez être membre du groupe administrateurs pour définir des propriétés à l’aide de cette classe.</span><span class="sxs-lookup"><span data-stu-id="70363-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="70363-174">La propriété **Disabled** n’empêche pas les utilisateurs de démarrer des programmes non listés à distance après qu’ils se sont connectés au serveur hôte de session Bureau à distance à l’aide d’un programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="70363-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="70363-175">La propriété **Disabled** est définie sur la valeur 2 uniquement si l’entrée de Registre suivante est manquante :</span><span class="sxs-lookup"><span data-stu-id="70363-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="70363-176">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **TerminalServer** \\ **TSAppAllowList** \\ **fDisabledAllowList**</span><span class="sxs-lookup"><span data-stu-id="70363-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="70363-177">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="70363-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="70363-178">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="70363-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="70363-179">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="70363-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="70363-180">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="70363-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="70363-181">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="70363-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="70363-182">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="70363-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="70363-183">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="70363-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="70363-184">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="70363-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="70363-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70363-185">Requirements</span></span>



| <span data-ttu-id="70363-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70363-186">Requirement</span></span> | <span data-ttu-id="70363-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="70363-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70363-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70363-188">Minimum supported client</span></span><br/> | <span data-ttu-id="70363-189">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70363-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="70363-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70363-190">Minimum supported server</span></span><br/> | <span data-ttu-id="70363-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70363-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70363-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70363-192">Namespace</span></span><br/>                | <span data-ttu-id="70363-193">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="70363-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="70363-194">MOF</span><span class="sxs-lookup"><span data-stu-id="70363-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70363-195"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70363-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="70363-196">DLL</span><span class="sxs-lookup"><span data-stu-id="70363-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70363-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70363-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

