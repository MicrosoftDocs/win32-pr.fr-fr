---
description: Représente les données de paramètre d’isolation.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Classe Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540872"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="74c93-103">MSVM \_ EthernetSwitchPortIsolationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="74c93-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="74c93-104">Représente les données de paramètre d’isolation.</span><span class="sxs-lookup"><span data-stu-id="74c93-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="74c93-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="74c93-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c93-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74c93-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="74c93-107">Membres</span><span class="sxs-lookup"><span data-stu-id="74c93-107">Members</span></span>

<span data-ttu-id="74c93-108">La classe **MSVM \_ EthernetSwitchPortIsolationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="74c93-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="74c93-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74c93-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74c93-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="74c93-110">Properties</span></span>

<span data-ttu-id="74c93-111">La classe **MSVM \_ EthernetSwitchPortIsolationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="74c93-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74c93-112">**AllowUntaggedTraffic**</span><span class="sxs-lookup"><span data-stu-id="74c93-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74c93-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74c93-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74c93-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="74c93-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74c93-115">Qualificateurs : **WmiDataId** (2), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="74c93-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="74c93-116">Indique si le port est autorisé à envoyer/recevoir du trafic non marqué.</span><span class="sxs-lookup"><span data-stu-id="74c93-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="74c93-117">**DefaultIsolationId**</span><span class="sxs-lookup"><span data-stu-id="74c93-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74c93-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74c93-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74c93-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="74c93-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74c93-120">Qualificateurs : **WmiDataId** (3), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="74c93-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="74c93-121">VirtualSubnetId ou VLAN par défaut qui sera défini sur tout le trafic d’envoi/réception si **AllowedUntaggedTraffic** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="74c93-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="74c93-122">**EnableMultiTenantStack**</span><span class="sxs-lookup"><span data-stu-id="74c93-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74c93-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="74c93-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74c93-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="74c93-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74c93-125">Qualificateurs : **WmiDataId** (4), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="74c93-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="74c93-126">Si la **valeur est true**, la pile réseau de la machine virtuelle peut accéder à la configuration d’isolation.</span><span class="sxs-lookup"><span data-stu-id="74c93-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="74c93-127">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="74c93-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="74c93-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="74c93-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74c93-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74c93-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74c93-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="74c93-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74c93-131">Qualificateurs : **WmiDataId** (1), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="74c93-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="74c93-132">Indique si le port utilise **VLAN** ou **VirtualSubnetId** pour l’isolation.</span><span class="sxs-lookup"><span data-stu-id="74c93-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="74c93-133">**NativeVirtualSubnetId** est utilisé pour les réseaux wnv VirtualSubnetId.</span><span class="sxs-lookup"><span data-stu-id="74c93-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="74c93-134">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="74c93-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="74c93-135">**NativeVirtualSubnetId** (1)</span><span class="sxs-lookup"><span data-stu-id="74c93-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="74c93-136">**ExternalVirtualSubnetId** (2)</span><span class="sxs-lookup"><span data-stu-id="74c93-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="74c93-137">**Réseau local virtuel** (3)</span><span class="sxs-lookup"><span data-stu-id="74c93-137">**VLAN** (3)</span></span>


<span data-ttu-id="74c93-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="74c93-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="74c93-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74c93-139">Requirements</span></span>



| <span data-ttu-id="74c93-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74c93-140">Requirement</span></span> | <span data-ttu-id="74c93-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="74c93-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c93-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c93-142">Minimum supported client</span></span><br/> | <span data-ttu-id="74c93-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="74c93-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="74c93-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c93-144">Minimum supported server</span></span><br/> | <span data-ttu-id="74c93-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="74c93-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="74c93-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="74c93-146">Namespace</span></span><br/>                | <span data-ttu-id="74c93-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="74c93-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74c93-148">MOF</span><span class="sxs-lookup"><span data-stu-id="74c93-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74c93-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74c93-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74c93-150">DLL</span><span class="sxs-lookup"><span data-stu-id="74c93-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c93-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74c93-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74c93-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74c93-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c93-153">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="74c93-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

