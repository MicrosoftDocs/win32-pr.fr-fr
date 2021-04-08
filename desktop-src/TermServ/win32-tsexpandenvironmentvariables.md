---
title: Classe Win32_TSExpandEnvironmentVariables
description: Développe les variables d’environnement définies par le système. | Classe Win32_TSExpandEnvironmentVariables
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Win32_TSExpandEnvironmentVariables de la classe Services Bureau à distance
- Win32_TSExpandEnvironmentVariables de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869906"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="c919f-106">\_Classe TSExpandEnvironmentVariables Win32</span><span class="sxs-lookup"><span data-stu-id="c919f-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="c919f-107">Développe les variables d’environnement définies par le système.</span><span class="sxs-lookup"><span data-stu-id="c919f-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="c919f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c919f-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="c919f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c919f-109">Members</span></span>

<span data-ttu-id="c919f-110">La classe **Win32 \_ TSExpandEnvironmentVariables** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c919f-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="c919f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c919f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c919f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c919f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c919f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c919f-113">Methods</span></span>

<span data-ttu-id="c919f-114">La classe **Win32 \_ TSExpandEnvironmentVariables** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c919f-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="c919f-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c919f-115">Method</span></span>                                                                                  | <span data-ttu-id="c919f-116">Description</span><span class="sxs-lookup"><span data-stu-id="c919f-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="c919f-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="c919f-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="c919f-118">Développe les variables d’environnement définies par le système.</span><span class="sxs-lookup"><span data-stu-id="c919f-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c919f-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c919f-119">Properties</span></span>

<span data-ttu-id="c919f-120">La classe **Win32 \_ TSExpandEnvironmentVariables** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c919f-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c919f-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c919f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919f-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c919f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c919f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c919f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c919f-124">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c919f-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c919f-125">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c919f-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c919f-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c919f-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c919f-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="c919f-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919f-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c919f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c919f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c919f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c919f-130">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c919f-130">Description of the object.</span></span>

<span data-ttu-id="c919f-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c919f-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c919f-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c919f-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919f-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c919f-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c919f-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c919f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c919f-135">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c919f-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c919f-136">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="c919f-136">The date the object was installed.</span></span> <span data-ttu-id="c919f-137">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="c919f-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c919f-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c919f-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c919f-139">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c919f-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919f-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c919f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c919f-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c919f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c919f-142">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="c919f-142">The name of the object.</span></span>

<span data-ttu-id="c919f-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c919f-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c919f-144">**État**</span><span class="sxs-lookup"><span data-stu-id="c919f-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919f-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c919f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c919f-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c919f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c919f-147">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c919f-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c919f-148">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c919f-148">Current status of the object.</span></span> <span data-ttu-id="c919f-149">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="c919f-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c919f-150">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="c919f-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c919f-151">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="c919f-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c919f-152">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="c919f-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c919f-153">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="c919f-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c919f-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c919f-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c919f-155">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="c919f-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-156">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="c919f-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-157">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="c919f-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-158">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="c919f-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-159">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="c919f-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-160">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="c919f-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-161">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="c919f-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c919f-162">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="c919f-162">("Service")</span></span>


<span data-ttu-id="c919f-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c919f-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c919f-164">Notes</span><span class="sxs-lookup"><span data-stu-id="c919f-164">Remarks</span></span>

<span data-ttu-id="c919f-165">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="c919f-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c919f-166">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="c919f-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="c919f-167">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="c919f-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c919f-168">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="c919f-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c919f-169">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c919f-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c919f-170">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c919f-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c919f-171">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c919f-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c919f-172">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c919f-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c919f-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c919f-173">Requirements</span></span>



| <span data-ttu-id="c919f-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c919f-174">Requirement</span></span> | <span data-ttu-id="c919f-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="c919f-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c919f-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c919f-176">Minimum supported client</span></span><br/> | <span data-ttu-id="c919f-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c919f-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c919f-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c919f-178">Minimum supported server</span></span><br/> | <span data-ttu-id="c919f-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c919f-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c919f-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c919f-180">Namespace</span></span><br/>                | <span data-ttu-id="c919f-181">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c919f-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c919f-182">MOF</span><span class="sxs-lookup"><span data-stu-id="c919f-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c919f-183"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c919f-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c919f-184">DLL</span><span class="sxs-lookup"><span data-stu-id="c919f-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c919f-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c919f-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

