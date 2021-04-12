---
description: Représente une entrée d’autorisation pour un serveur de récupération.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Classe Msvm_ReplicationAuthorizationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203079"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="a4d18-103">MSVM \_ ReplicationAuthorizationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="a4d18-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="a4d18-104">Représente une entrée d’autorisation pour un serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="a4d18-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="a4d18-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a4d18-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4d18-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="a4d18-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a4d18-107">Members</span></span>

<span data-ttu-id="a4d18-108">La classe **MSVM \_ ReplicationAuthorizationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a4d18-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a4d18-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a4d18-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4d18-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a4d18-110">Properties</span></span>

<span data-ttu-id="a4d18-111">La classe **MSVM \_ ReplicationAuthorizationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a4d18-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4d18-112">**AllowedPrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="a4d18-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a4d18-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-115">Nom de domaine complet ou nom de groupe des serveurs principaux autorisés à répliquer sur ce serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="a4d18-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a4d18-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4d18-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a4d18-119">A short description of the object.</span></span> <span data-ttu-id="a4d18-120">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a4d18-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="a4d18-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4d18-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-124">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="a4d18-124">A description of the object.</span></span> <span data-ttu-id="a4d18-125">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a4d18-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a4d18-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4d18-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-129">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a4d18-129">A display name for the object.</span></span> <span data-ttu-id="a4d18-130">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a4d18-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a4d18-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a4d18-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-134">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="a4d18-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-135">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a4d18-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a4d18-136">Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="a4d18-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-137">**ReplicaStorageLocation**</span><span class="sxs-lookup"><span data-stu-id="a4d18-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a4d18-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-140">Emplacement de stockage des fichiers de réplication du **AllowedPrimaryHostSystem** .</span><span class="sxs-lookup"><span data-stu-id="a4d18-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="a4d18-141">**TrustGroup**</span><span class="sxs-lookup"><span data-stu-id="a4d18-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d18-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a4d18-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d18-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a4d18-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a4d18-144">Nom du groupe de confiance de l’entrée d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="a4d18-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="a4d18-145">Cela identifie les entrées d’autorisation multiples regroupées.</span><span class="sxs-lookup"><span data-stu-id="a4d18-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4d18-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4d18-146">Requirements</span></span>



| <span data-ttu-id="a4d18-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4d18-147">Requirement</span></span> | <span data-ttu-id="a4d18-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4d18-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d18-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4d18-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d18-150">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4d18-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4d18-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4d18-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d18-152">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4d18-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4d18-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4d18-153">Namespace</span></span><br/>                | <span data-ttu-id="a4d18-154">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4d18-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4d18-155">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d18-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d18-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4d18-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d18-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d18-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d18-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4d18-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4d18-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4d18-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d18-160">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a4d18-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="a4d18-161">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a4d18-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a4d18-162">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a4d18-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a4d18-163">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a4d18-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

