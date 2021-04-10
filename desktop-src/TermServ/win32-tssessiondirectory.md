---
title: Classe Win32_TSSessionDirectory
description: Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la \_ classe Win32 TSSessionDirectorySetting.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory de la classe Services Bureau à distance
- Win32_TSSessionDirectory de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941980"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="ecf63-105">\_Classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="ecf63-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="ecf63-106">Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf63-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="ecf63-107">Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="ecf63-108">Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="ecf63-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="ecf63-109">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="ecf63-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="ecf63-110">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ecf63-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf63-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecf63-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="ecf63-112">Membres</span><span class="sxs-lookup"><span data-stu-id="ecf63-112">Members</span></span>

<span data-ttu-id="ecf63-113">La classe **Win32 \_ TSSessionDirectory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ecf63-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="ecf63-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ecf63-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ecf63-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecf63-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ecf63-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ecf63-116">Methods</span></span>

<span data-ttu-id="ecf63-117">La classe **Win32 \_ TSSessionDirectory** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ecf63-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="ecf63-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="ecf63-118">Method</span></span>                                                                                                  | <span data-ttu-id="ecf63-119">Description</span><span class="sxs-lookup"><span data-stu-id="ecf63-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf63-120">**CreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="ecf63-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="ecf63-121">Crée un modèle de disque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecf63-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="ecf63-122">**DisableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="ecf63-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="ecf63-123">Désactive un disque dur virtuel de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecf63-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="ecf63-124">**EnableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="ecf63-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="ecf63-125">Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.</span><span class="sxs-lookup"><span data-stu-id="ecf63-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="ecf63-126">**GetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="ecf63-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="ecf63-127">Obtient la liste configurée actuellement des adresses DNS éligibles et le type de redirection.</span><span class="sxs-lookup"><span data-stu-id="ecf63-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="ecf63-128">**GetRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="ecf63-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="ecf63-129">Obtient la liste complète des adresses DNS éligibles.</span><span class="sxs-lookup"><span data-stu-id="ecf63-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="ecf63-130">**PingSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="ecf63-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="ecf63-131">Vérifie si le serveur du Service Broker pour les connexions Bureau à distance est disponible.</span><span class="sxs-lookup"><span data-stu-id="ecf63-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="ecf63-132">**SetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="ecf63-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="ecf63-133">Définit la liste configurée des adresses DNS éligibles et le type de redirection.</span><span class="sxs-lookup"><span data-stu-id="ecf63-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="ecf63-134">**SetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="ecf63-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="ecf63-135">Définit la valeur pour indiquer si le serveur doit participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="ecf63-136">**SetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="ecf63-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="ecf63-137">Définit la valeur du poids du serveur pour l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="ecf63-138">**SetSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="ecf63-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="ecf63-139">Désactive et active le Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="ecf63-140">**SetSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="ecf63-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="ecf63-141">Définit la propriété **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="ecf63-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="ecf63-142">**SetSessionDirectoryProperty**</span><span class="sxs-lookup"><span data-stu-id="ecf63-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="ecf63-143">Définit la propriété **SessionDirectoryLocation** ou la propriété **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="ecf63-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="ecf63-144">**SetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="ecf63-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="ecf63-145">Cette méthode n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ecf63-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="ecf63-146">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecf63-146">Properties</span></span>

<span data-ttu-id="ecf63-147">La classe **Win32 \_ TSSessionDirectory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ecf63-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ecf63-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ecf63-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ecf63-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-152">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ecf63-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="ecf63-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-157">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-157">Description of the object.</span></span>

<span data-ttu-id="ecf63-158">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-159">**GetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="ecf63-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-162">Indique si le serveur est configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="ecf63-163">0</span><span class="sxs-lookup"><span data-stu-id="ecf63-163">0</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-164">Le serveur n’est pas configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-165">1</span><span class="sxs-lookup"><span data-stu-id="ecf63-165">1</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-166">Le serveur est configuré pour participer à l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-167">**GetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="ecf63-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-168">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-170">Récupère la valeur de poids du serveur qui est utilisée dans l’équilibrage de charge du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-171">**GetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="ecf63-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-174">Indique si le serveur est configuré pour agir en tant que redirecteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="ecf63-175">0</span><span class="sxs-lookup"><span data-stu-id="ecf63-175">0</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-176">Le serveur est configuré pour agir en tant que redirecteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-177">1</span><span class="sxs-lookup"><span data-stu-id="ecf63-177">1</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-178">Le serveur n’est pas configuré pour agir en tant que redirecteur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="ecf63-179">**Windows Server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ecf63-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ecf63-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-181">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ecf63-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-183">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ecf63-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-184">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="ecf63-184">The date the object was installed.</span></span> <span data-ttu-id="ecf63-185">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ecf63-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ecf63-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-187">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ecf63-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-190">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-190">The name of the object.</span></span>

<span data-ttu-id="ecf63-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-192">**PolicySourceLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="ecf63-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-195">Indique si la propriété **GetLoadBalancingState** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-196">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-197">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-199">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-200">**PolicySourceSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="ecf63-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-203">Indique si la propriété **SessionDirectoryActive** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-204">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-205">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-207">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-208">**PolicySourceSessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="ecf63-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-209">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-211">Indique si la propriété **SessionDirectoryClusterName** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-212">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-213">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-215">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-216">**PolicySourceSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="ecf63-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-217">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-219">Indique si la propriété **SessionDirectoryExposeServerIP** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-220">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-221">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-223">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-224">**PolicySourceSessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="ecf63-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-227">Indique si la propriété **SessionDirectoryLocation** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-228">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-229">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-231">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-232">**PolicySourceTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="ecf63-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-233">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-235">Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ecf63-235">This property is not available.</span></span>

<span data-ttu-id="ecf63-236">**Windows Server 2008 R2 :** Indique si la propriété **GetTSRedirectorMode** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ecf63-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ecf63-237">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-238">Serveur</span><span class="sxs-lookup"><span data-stu-id="ecf63-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ecf63-240">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ecf63-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-241">**SessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="ecf63-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-242">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-244">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecf63-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-245">Spécifie si Services Bureau à distance fait partie du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ecf63-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ecf63-247">Services Bureau à distance la participation au service Broker pour les connexions Bureau à distance est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ecf63-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ecf63-248"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ecf63-249">Services Bureau à distance la participation au service Broker pour les connexions Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="ecf63-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-250">**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="ecf63-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-253">Adresse IP virtuelle du cluster auquel appartient le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ecf63-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-254">**SessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="ecf63-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-255">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-257">Spécifie si la récupération de l’adresse IP du Service Broker pour les connexions Bureau à distance est autorisée.</span><span class="sxs-lookup"><span data-stu-id="ecf63-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ecf63-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ecf63-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ecf63-259">La récupération est refusée.</span><span class="sxs-lookup"><span data-stu-id="ecf63-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ecf63-260"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ecf63-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ecf63-261">La récupération est autorisée.</span><span class="sxs-lookup"><span data-stu-id="ecf63-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ecf63-262">**SessionDirectoryIPAddress**</span><span class="sxs-lookup"><span data-stu-id="ecf63-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-264">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecf63-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-265">Adresse IP de la carte réseau utilisée par l’annuaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="ecf63-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-266">**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="ecf63-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-269">Nom DNS réseau ou adresse IP du serveur sur lequel le service du Service Broker pour les connexions Bureau à distance est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ecf63-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-270">**État**</span><span class="sxs-lookup"><span data-stu-id="ecf63-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecf63-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecf63-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecf63-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecf63-273">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ecf63-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ecf63-274">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-274">Current status of the object.</span></span> <span data-ttu-id="ecf63-275">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ecf63-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ecf63-276">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="ecf63-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ecf63-277">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ecf63-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ecf63-278">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ecf63-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ecf63-279">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ecf63-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ecf63-280">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ecf63-281">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-282">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-283">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-284">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="ecf63-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-285">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-286">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-287">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ecf63-288">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="ecf63-288">("Service")</span></span>


<span data-ttu-id="ecf63-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ecf63-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ecf63-290">Notes</span><span class="sxs-lookup"><span data-stu-id="ecf63-290">Remarks</span></span>

<span data-ttu-id="ecf63-291">Pour se connecter à l' \\ \\ \\ espace de \\ noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ecf63-292">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="ecf63-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ecf63-293">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de six.</span><span class="sxs-lookup"><span data-stu-id="ecf63-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="ecf63-294">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="ecf63-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ecf63-295">Dans Windows Server 2008, le nom de la fonctionnalité annuaire de sessions des services Terminal Server a été remplacé par session Broker des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="ecf63-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="ecf63-296">Dans Windows Server 2008 R2, le nom de la fonctionnalité session Broker des services Terminal Server a été remplacé par Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="ecf63-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="ecf63-297">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ecf63-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ecf63-298">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ecf63-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ecf63-299">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ecf63-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ecf63-300">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ecf63-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf63-301">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecf63-301">Requirements</span></span>



| <span data-ttu-id="ecf63-302">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecf63-302">Requirement</span></span> | <span data-ttu-id="ecf63-303">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecf63-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf63-304">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecf63-304">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf63-305">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecf63-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ecf63-306">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecf63-306">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf63-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecf63-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecf63-308">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ecf63-308">Namespace</span></span><br/>                | <span data-ttu-id="ecf63-309">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ecf63-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ecf63-310">MOF</span><span class="sxs-lookup"><span data-stu-id="ecf63-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecf63-311"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecf63-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecf63-312">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf63-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf63-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf63-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf63-314">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecf63-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf63-315">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="ecf63-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="ecf63-316">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ecf63-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

