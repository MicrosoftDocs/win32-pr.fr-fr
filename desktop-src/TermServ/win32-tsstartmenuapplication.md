---
title: Classe Win32_TSStartMenuApplication
description: Décrit les applications qui se trouvent dans le menu Démarrer d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Win32_TSStartMenuApplication de la classe Services Bureau à distance
- Win32_TSStartMenuApplication de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743596"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="6133f-105">\_Classe TSStartMenuApplication Win32</span><span class="sxs-lookup"><span data-stu-id="6133f-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="6133f-106">Décrit les applications qui se trouvent dans le menu Démarrer d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="6133f-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6133f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6133f-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="6133f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6133f-108">Members</span></span>

<span data-ttu-id="6133f-109">La classe **Win32 \_ TSStartMenuApplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6133f-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="6133f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6133f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6133f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6133f-111">Properties</span></span>

<span data-ttu-id="6133f-112">La classe **Win32 \_ TSStartMenuApplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6133f-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6133f-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6133f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6133f-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6133f-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6133f-117">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6133f-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6133f-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6133f-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6133f-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="6133f-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-122">Arguments de ligne de commande à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6133f-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="6133f-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="6133f-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-126">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6133f-126">Description of the object.</span></span>

<span data-ttu-id="6133f-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6133f-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6133f-128">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="6133f-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6133f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-131">Index ou ID de l’icône.</span><span class="sxs-lookup"><span data-stu-id="6133f-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="6133f-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="6133f-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-135">Chemin d’accès de l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="6133f-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="6133f-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6133f-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-137">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6133f-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6133f-139">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="6133f-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6133f-140">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6133f-140">The date the object was installed.</span></span> <span data-ttu-id="6133f-141">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6133f-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6133f-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6133f-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6133f-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6133f-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-146">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="6133f-146">The name of the object.</span></span>

<span data-ttu-id="6133f-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6133f-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6133f-148">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="6133f-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6133f-151">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="6133f-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6133f-152">Chemin d'accès de l'application.</span><span class="sxs-lookup"><span data-stu-id="6133f-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="6133f-153">**État**</span><span class="sxs-lookup"><span data-stu-id="6133f-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6133f-156">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6133f-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6133f-157">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6133f-157">Current status of the object.</span></span> <span data-ttu-id="6133f-158">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="6133f-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6133f-159">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="6133f-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6133f-160">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6133f-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6133f-161">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6133f-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6133f-162">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6133f-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6133f-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6133f-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6133f-164">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="6133f-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-165">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="6133f-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-166">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6133f-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-167">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="6133f-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-168">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6133f-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-169">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6133f-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-170">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6133f-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6133f-171">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="6133f-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6133f-172">**VPath**</span><span class="sxs-lookup"><span data-stu-id="6133f-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6133f-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6133f-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6133f-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6133f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6133f-175">Chemin d’accès virtuel de l’application.</span><span class="sxs-lookup"><span data-stu-id="6133f-175">The virtual path of the application.</span></span> <span data-ttu-id="6133f-176">Cela comprend les variables d’environnement système, telles que% windir%.</span><span class="sxs-lookup"><span data-stu-id="6133f-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6133f-177">Notes</span><span class="sxs-lookup"><span data-stu-id="6133f-177">Remarks</span></span>

<span data-ttu-id="6133f-178">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="6133f-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="6133f-179">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="6133f-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6133f-180">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="6133f-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="6133f-181">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="6133f-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="6133f-182">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="6133f-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6133f-183">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6133f-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6133f-184">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6133f-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6133f-185">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6133f-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6133f-186">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6133f-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6133f-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6133f-187">Requirements</span></span>



| <span data-ttu-id="6133f-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6133f-188">Requirement</span></span> | <span data-ttu-id="6133f-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="6133f-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6133f-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6133f-190">Minimum supported client</span></span><br/> | <span data-ttu-id="6133f-191">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6133f-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6133f-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6133f-192">Minimum supported server</span></span><br/> | <span data-ttu-id="6133f-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6133f-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6133f-194">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6133f-194">Namespace</span></span><br/>                | <span data-ttu-id="6133f-195">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="6133f-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6133f-196">MOF</span><span class="sxs-lookup"><span data-stu-id="6133f-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6133f-197"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6133f-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6133f-198">DLL</span><span class="sxs-lookup"><span data-stu-id="6133f-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6133f-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6133f-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

