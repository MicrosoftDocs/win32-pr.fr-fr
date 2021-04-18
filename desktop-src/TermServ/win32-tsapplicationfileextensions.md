---
title: Classe Win32_TSApplicationFileExtensions
description: Les extensions de nom de fichier gérées par une application sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509556"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="981ec-105">\_Classe TSApplicationFileExtensions Win32</span><span class="sxs-lookup"><span data-stu-id="981ec-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="981ec-106">Décrit les extensions de nom de fichier qui sont gérées par une application sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="981ec-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="981ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="981ec-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="981ec-108">Membres</span><span class="sxs-lookup"><span data-stu-id="981ec-108">Members</span></span>

<span data-ttu-id="981ec-109">La classe **Win32 \_ TSApplicationFileExtensions** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="981ec-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="981ec-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="981ec-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="981ec-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="981ec-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="981ec-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="981ec-112">Methods</span></span>

<span data-ttu-id="981ec-113">La classe **Win32 \_ TSApplicationFileExtensions** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="981ec-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="981ec-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="981ec-114">Method</span></span>                                                                         | <span data-ttu-id="981ec-115">Description</span><span class="sxs-lookup"><span data-stu-id="981ec-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="981ec-116">**FileAssociations**</span><span class="sxs-lookup"><span data-stu-id="981ec-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="981ec-117">Analyse le registre pour obtenir les associations de fichiers actuelles pour une application.</span><span class="sxs-lookup"><span data-stu-id="981ec-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="981ec-118">**FileExtensions**</span><span class="sxs-lookup"><span data-stu-id="981ec-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="981ec-119">Fournit une liste des extensions de nom de fichier qui sont gérées par une application.</span><span class="sxs-lookup"><span data-stu-id="981ec-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="981ec-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="981ec-120">Properties</span></span>

<span data-ttu-id="981ec-121">La classe **Win32 \_ TSApplicationFileExtensions** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="981ec-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="981ec-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="981ec-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ec-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="981ec-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ec-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="981ec-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="981ec-125">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="981ec-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="981ec-126">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="981ec-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="981ec-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="981ec-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="981ec-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="981ec-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ec-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="981ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ec-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="981ec-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="981ec-131">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="981ec-131">Description of the object.</span></span>

<span data-ttu-id="981ec-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="981ec-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="981ec-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="981ec-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ec-134">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="981ec-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="981ec-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="981ec-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="981ec-136">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="981ec-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="981ec-137">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="981ec-137">The date the object was installed.</span></span> <span data-ttu-id="981ec-138">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="981ec-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="981ec-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="981ec-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="981ec-140">**Nom**</span><span class="sxs-lookup"><span data-stu-id="981ec-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ec-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="981ec-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ec-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="981ec-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="981ec-143">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="981ec-143">The name of the object.</span></span>

<span data-ttu-id="981ec-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="981ec-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="981ec-145">**État**</span><span class="sxs-lookup"><span data-stu-id="981ec-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ec-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="981ec-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ec-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="981ec-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="981ec-148">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="981ec-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="981ec-149">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="981ec-149">Current status of the object.</span></span> <span data-ttu-id="981ec-150">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="981ec-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="981ec-151">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="981ec-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="981ec-152">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="981ec-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="981ec-153">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="981ec-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="981ec-154">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="981ec-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="981ec-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="981ec-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="981ec-156">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="981ec-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-157">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="981ec-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-158">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="981ec-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-159">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="981ec-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-160">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="981ec-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-161">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="981ec-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-162">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="981ec-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="981ec-163">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="981ec-163">("Service")</span></span>


<span data-ttu-id="981ec-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="981ec-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="981ec-165">Notes</span><span class="sxs-lookup"><span data-stu-id="981ec-165">Remarks</span></span>

<span data-ttu-id="981ec-166">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="981ec-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="981ec-167">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="981ec-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="981ec-168">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="981ec-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="981ec-169">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="981ec-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="981ec-170">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="981ec-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="981ec-171">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="981ec-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="981ec-172">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="981ec-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="981ec-173">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="981ec-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="981ec-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="981ec-174">Requirements</span></span>



| <span data-ttu-id="981ec-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="981ec-175">Requirement</span></span> | <span data-ttu-id="981ec-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="981ec-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="981ec-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="981ec-177">Minimum supported client</span></span><br/> | <span data-ttu-id="981ec-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="981ec-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="981ec-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="981ec-179">Minimum supported server</span></span><br/> | <span data-ttu-id="981ec-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="981ec-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="981ec-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="981ec-181">Namespace</span></span><br/>                | <span data-ttu-id="981ec-182">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="981ec-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="981ec-183">MOF</span><span class="sxs-lookup"><span data-stu-id="981ec-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="981ec-184"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="981ec-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="981ec-185">DLL</span><span class="sxs-lookup"><span data-stu-id="981ec-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="981ec-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="981ec-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

