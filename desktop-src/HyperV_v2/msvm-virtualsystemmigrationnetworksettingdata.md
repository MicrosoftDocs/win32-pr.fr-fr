---
description: Représente le réseau sur lequel le service de migration de système virtuel écoute la migration du système virtuel entrant.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Classe Msvm_VirtualSystemMigrationNetworkSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862058"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="3319a-103">MSVM \_ VirtualSystemMigrationNetworkSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="3319a-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="3319a-104">Représente le réseau sur lequel le service de migration de système virtuel écoute la migration du système virtuel entrant.</span><span class="sxs-lookup"><span data-stu-id="3319a-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="3319a-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3319a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3319a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3319a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="3319a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3319a-107">Members</span></span>

<span data-ttu-id="3319a-108">La classe **MSVM \_ VirtualSystemMigrationNetworkSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3319a-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3319a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3319a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3319a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3319a-110">Properties</span></span>

<span data-ttu-id="3319a-111">La classe **MSVM \_ VirtualSystemMigrationNetworkSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3319a-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3319a-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3319a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3319a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3319a-115">A short description of the object.</span></span> <span data-ttu-id="3319a-116">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="3319a-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="3319a-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="3319a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3319a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="3319a-120">A description of the object.</span></span> <span data-ttu-id="3319a-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3319a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3319a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3319a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3319a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3319a-125">A display name for the object.</span></span> <span data-ttu-id="3319a-126">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3319a-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3319a-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3319a-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3319a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3319a-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3319a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3319a-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3319a-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3319a-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3319a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3319a-133">**Mesure**</span><span class="sxs-lookup"><span data-stu-id="3319a-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3319a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-136">Mesure de priorité de ce réseau pour la migration.</span><span class="sxs-lookup"><span data-stu-id="3319a-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="3319a-137">Les valeurs les plus basses sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="3319a-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="3319a-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="3319a-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-139">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3319a-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-141">Longueur du préfixe du sous-réseau de la migration.</span><span class="sxs-lookup"><span data-stu-id="3319a-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="3319a-142">**SubnetNumber**</span><span class="sxs-lookup"><span data-stu-id="3319a-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3319a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3319a-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-145">Numéro de sous-réseau de la migration.</span><span class="sxs-lookup"><span data-stu-id="3319a-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="3319a-146">**Balises**</span><span class="sxs-lookup"><span data-stu-id="3319a-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3319a-147">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3319a-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3319a-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3319a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3319a-149">Tableau de balises permettant de représenter le système de gestion qui a défini ce réseau pour le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="3319a-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3319a-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3319a-150">Requirements</span></span>



| <span data-ttu-id="3319a-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3319a-151">Requirement</span></span> | <span data-ttu-id="3319a-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="3319a-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3319a-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3319a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3319a-154">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3319a-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3319a-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3319a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3319a-156">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3319a-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3319a-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3319a-157">Namespace</span></span><br/>                | <span data-ttu-id="3319a-158">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3319a-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3319a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="3319a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3319a-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3319a-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3319a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="3319a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3319a-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3319a-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3319a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3319a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3319a-164">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3319a-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="3319a-165">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="3319a-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

