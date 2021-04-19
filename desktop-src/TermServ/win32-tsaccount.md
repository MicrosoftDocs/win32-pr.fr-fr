---
title: Classe Win32_TSAccount
description: Autorise la suppression d’un compte qui existe sur le \_ Terminal Win32 et la modification des autorisations existantes.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount de la classe Services Bureau à distance
- Win32_TSAccount de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511392"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="bea4d-105">\_Classe TSAccount Win32</span><span class="sxs-lookup"><span data-stu-id="bea4d-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="bea4d-106">La classe WMI **\_ TSAccount** WMI autorise la suppression d’un compte qui existe sur [**le \_ Terminal Win32**](win32-terminal.md) et la modification des autorisations existantes.</span><span class="sxs-lookup"><span data-stu-id="bea4d-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="bea4d-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="bea4d-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="bea4d-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="bea4d-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea4d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bea4d-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="bea4d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="bea4d-110">Members</span></span>

<span data-ttu-id="bea4d-111">La classe **Win32 \_ TSAccount** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bea4d-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="bea4d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bea4d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bea4d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bea4d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bea4d-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bea4d-114">Methods</span></span>

<span data-ttu-id="bea4d-115">La classe **Win32 \_ TSAccount** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bea4d-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="bea4d-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="bea4d-116">Method</span></span>                                                                   | <span data-ttu-id="bea4d-117">Description</span><span class="sxs-lookup"><span data-stu-id="bea4d-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bea4d-118">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="bea4d-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="bea4d-119">Supprime l’utilisateur, le groupe ou le compte d’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="bea4d-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="bea4d-120">**ModifyAuditPermissions**</span><span class="sxs-lookup"><span data-stu-id="bea4d-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="bea4d-121">Modifie la granularité de l’ensemble des autorisations d’audit du compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="bea4d-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="bea4d-122">**ModifyPermissions**</span><span class="sxs-lookup"><span data-stu-id="bea4d-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="bea4d-123">Définit un jeu d’autorisations plus granulaire pour le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="bea4d-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="bea4d-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bea4d-124">Properties</span></span>

<span data-ttu-id="bea4d-125">La classe **Win32 \_ TSAccount** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bea4d-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bea4d-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="bea4d-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bea4d-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-130">Nom actuel du compte.</span><span class="sxs-lookup"><span data-stu-id="bea4d-130">The current name of the account.</span></span> <span data-ttu-id="bea4d-131">Le nom de domaine est inclus.</span><span class="sxs-lookup"><span data-stu-id="bea4d-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-132">**AuditFail**</span><span class="sxs-lookup"><span data-stu-id="bea4d-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bea4d-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-135">Spécifie les [autorisations des services d’hôte de Session Bureau à distance](terminal-services-permissions.md) qui sont auditées pour une condition d’échec.</span><span class="sxs-lookup"><span data-stu-id="bea4d-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="bea4d-136">La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bea4d-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="bea4d-137">**Station \_ de REQUÊTE = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="bea4d-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="bea4d-138">**Station \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="bea4d-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="bea4d-139">**Station \_ de LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="bea4d-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="bea4d-140">**Station \_ de \| Droits standard \_ virtuels \_ requis = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="bea4d-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="bea4d-141">**Station \_ de SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="bea4d-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="bea4d-142">**Station \_ de LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="bea4d-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="bea4d-143">**Station \_ de MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="bea4d-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="bea4d-144">**Station \_ de CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="bea4d-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="bea4d-145">**Station \_ de Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="bea4d-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bea4d-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="bea4d-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bea4d-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-149">Spécifie les autorisations spécifiques au serveur hôte de session Bureau à distance qui sont auditées pour une condition de réussite.</span><span class="sxs-lookup"><span data-stu-id="bea4d-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="bea4d-150">La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bea4d-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="bea4d-151">**Station \_ de REQUÊTE = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="bea4d-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="bea4d-152">**Station \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="bea4d-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="bea4d-153">**Station \_ de LOGOFF = 0x4WINSTATION \_ les \| droits standard virtuels \_ \_ requis = 0xF008** (2)</span><span class="sxs-lookup"><span data-stu-id="bea4d-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="bea4d-154">**Station \_ de SHADOW = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="bea4d-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="bea4d-155">**Station \_ de LOGON = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="bea4d-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="bea4d-156">**Station \_ de MSG = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="bea4d-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="bea4d-157">**Station \_ de CONNECT = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="bea4d-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="bea4d-158">**Station \_ de Disconnect = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="bea4d-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bea4d-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bea4d-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bea4d-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-163">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="bea4d-164">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-165">**Description**</span><span class="sxs-lookup"><span data-stu-id="bea4d-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-168">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-168">Description of the object.</span></span>

<span data-ttu-id="bea4d-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bea4d-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-171">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bea4d-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-173">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="bea4d-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-174">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="bea4d-174">The date the object was installed.</span></span> <span data-ttu-id="bea4d-175">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="bea4d-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bea4d-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-177">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bea4d-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-180">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-180">The name of the object.</span></span>

<span data-ttu-id="bea4d-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-182">**PermissionsAllowed**</span><span class="sxs-lookup"><span data-stu-id="bea4d-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bea4d-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-185">Spécifie les [autorisations de services Bureau à distance](terminal-services-permissions.md) autorisées pour le compte.</span><span class="sxs-lookup"><span data-stu-id="bea4d-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="bea4d-186">La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bea4d-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="bea4d-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**Station \_ de REQUÊTE = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="bea4d-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-188">Autorisation d’interroger les informations relatives à une session.</span><span class="sxs-lookup"><span data-stu-id="bea4d-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="bea4d-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Station \_ de DÉFINIR** (2)</span><span class="sxs-lookup"><span data-stu-id="bea4d-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-190">Autorisation de modifier les paramètres de connexion.</span><span class="sxs-lookup"><span data-stu-id="bea4d-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="bea4d-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Station \_ de Réinitialisation** (64)</span><span class="sxs-lookup"><span data-stu-id="bea4d-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-192">Autorisation de réinitialiser ou de mettre fin à une session ou à une connexion.</span><span class="sxs-lookup"><span data-stu-id="bea4d-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="bea4d-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Station \_ de \| Droits standard \_ virtuels \_ requis** (983048)</span><span class="sxs-lookup"><span data-stu-id="bea4d-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-194">Autorisation d’utiliser des canaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="bea4d-194">Permission to use virtual channels.</span></span> <span data-ttu-id="bea4d-195">Les canaux virtuels fournissent un accès à partir d’un programme serveur sur les périphériques clients.</span><span class="sxs-lookup"><span data-stu-id="bea4d-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="bea4d-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Station \_ de OMBRE** (16)</span><span class="sxs-lookup"><span data-stu-id="bea4d-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-197">Autorisation d’ombrer ou de contrôler à distance la session d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bea4d-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="bea4d-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Station \_ de Ouverture de session** (32)</span><span class="sxs-lookup"><span data-stu-id="bea4d-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-199">Autorisation de se connecter à une session sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="bea4d-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="bea4d-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Station \_ de Fermeture de session** (4)</span><span class="sxs-lookup"><span data-stu-id="bea4d-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-201">Autorisation de fermer la session d’un utilisateur à partir d’une session.</span><span class="sxs-lookup"><span data-stu-id="bea4d-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="bea4d-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Station \_ de MSG** (128)</span><span class="sxs-lookup"><span data-stu-id="bea4d-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-203">Autorisation d’envoyer un message à la session d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bea4d-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="bea4d-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Station \_ de SE connecter** (256)</span><span class="sxs-lookup"><span data-stu-id="bea4d-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-205">Autorisation de se connecter à une autre session.</span><span class="sxs-lookup"><span data-stu-id="bea4d-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="bea4d-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Station \_ de Se déconnecter** (512)</span><span class="sxs-lookup"><span data-stu-id="bea4d-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="bea4d-207">Autorisation de déconnecter une session.</span><span class="sxs-lookup"><span data-stu-id="bea4d-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bea4d-208">**PermissionsDenied**</span><span class="sxs-lookup"><span data-stu-id="bea4d-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-209">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bea4d-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-211">Spécifie les autorisations spécifiques au serveur hôte de session Bureau à distance qui ne sont pas autorisées pour le compte.</span><span class="sxs-lookup"><span data-stu-id="bea4d-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="bea4d-212">La valeur de cette propriété est un masque de masque, qui peut être défini sur une ou plusieurs des valeurs de la propriété **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bea4d-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="bea4d-213">**Station \_ de REQUÊTE = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="bea4d-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="bea4d-214">**Station \_ de SET = 0X2** (1)</span><span class="sxs-lookup"><span data-stu-id="bea4d-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="bea4d-215">**Station \_ de LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="bea4d-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="bea4d-216">**Station \_ de \| Droits standard \_ virtuels \_ requis = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="bea4d-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="bea4d-217">**Station \_ de SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="bea4d-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="bea4d-218">**Station \_ de LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="bea4d-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="bea4d-219">**Station \_ de MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="bea4d-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="bea4d-220">**Station \_ de CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="bea4d-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="bea4d-221">**Station \_ de Disconnect = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="bea4d-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bea4d-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="bea4d-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-225">Spécifie les [identificateurs de sécurité](/windows/desktop/SecAuthZ/security-identifiers) du compte.</span><span class="sxs-lookup"><span data-stu-id="bea4d-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="bea4d-226">**État**</span><span class="sxs-lookup"><span data-stu-id="bea4d-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-229">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="bea4d-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-230">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-230">Current status of the object.</span></span> <span data-ttu-id="bea4d-231">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="bea4d-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bea4d-232">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="bea4d-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bea4d-233">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="bea4d-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bea4d-234">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="bea4d-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bea4d-235">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="bea4d-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bea4d-236">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="bea4d-237">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-238">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-239">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-240">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="bea4d-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-241">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-242">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-243">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bea4d-244">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="bea4d-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bea4d-245">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="bea4d-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea4d-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bea4d-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bea4d-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bea4d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bea4d-248">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="bea4d-248">The name of the terminal.</span></span>

<span data-ttu-id="bea4d-249">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="bea4d-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bea4d-250">Notes</span><span class="sxs-lookup"><span data-stu-id="bea4d-250">Remarks</span></span>

<span data-ttu-id="bea4d-251">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="bea4d-252">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="bea4d-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="bea4d-253">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="bea4d-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="bea4d-254">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="bea4d-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="bea4d-255">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="bea4d-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bea4d-256">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bea4d-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bea4d-257">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="bea4d-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bea4d-258">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bea4d-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bea4d-259">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bea4d-259">Requirements</span></span>



| <span data-ttu-id="bea4d-260">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bea4d-260">Requirement</span></span> | <span data-ttu-id="bea4d-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="bea4d-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bea4d-262">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bea4d-262">Minimum supported client</span></span><br/> | <span data-ttu-id="bea4d-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bea4d-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bea4d-264">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bea4d-264">Minimum supported server</span></span><br/> | <span data-ttu-id="bea4d-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bea4d-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bea4d-266">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bea4d-266">Namespace</span></span><br/>                | <span data-ttu-id="bea4d-267">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="bea4d-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bea4d-268">MOF</span><span class="sxs-lookup"><span data-stu-id="bea4d-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bea4d-269"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bea4d-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bea4d-270">DLL</span><span class="sxs-lookup"><span data-stu-id="bea4d-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bea4d-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bea4d-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea4d-272">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bea4d-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea4d-273">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="bea4d-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

