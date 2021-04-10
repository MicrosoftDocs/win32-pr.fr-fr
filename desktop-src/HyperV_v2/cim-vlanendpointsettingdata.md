---
description: Représente des données de configuration pour un point de terminaison de réseau local virtuel.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Classe CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869281"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="3c079-103">\_Classe CIM VLANEndpointSettingData</span><span class="sxs-lookup"><span data-stu-id="3c079-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="3c079-104">Représente des données de configuration pour un point de terminaison de réseau local virtuel.</span><span class="sxs-lookup"><span data-stu-id="3c079-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c079-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c079-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="3c079-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3c079-106">Members</span></span>

<span data-ttu-id="3c079-107">La classe **CIM \_ VLANEndpointSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c079-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3c079-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c079-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c079-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c079-109">Properties</span></span>

<span data-ttu-id="3c079-110">La classe **CIM \_ VLANEndpointSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c079-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c079-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="3c079-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c079-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c079-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c079-113">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c079-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c079-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="3c079-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3c079-115">VLAN d’accès pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3c079-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="3c079-116">**DefaultVLAN**</span><span class="sxs-lookup"><span data-stu-id="3c079-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c079-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c079-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c079-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c079-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c079-119">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="3c079-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3c079-120">Valeur par défaut pour le VLAN natif sur le point de terminaison Trunk.</span><span class="sxs-lookup"><span data-stu-id="3c079-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3c079-121">Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="3c079-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c079-122">**NativeVLAN**</span><span class="sxs-lookup"><span data-stu-id="3c079-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c079-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c079-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c079-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c079-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c079-125">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="3c079-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3c079-126">ID de réseau local virtuel utilisé pour baliser le trafic non marqué reçu sur le point de terminaison Trunk.</span><span class="sxs-lookup"><span data-stu-id="3c079-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3c079-127">Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **SwitchEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="3c079-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c079-128">**PruneEligibleVLANList**</span><span class="sxs-lookup"><span data-stu-id="3c079-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c079-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c079-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c079-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c079-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c079-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="3c079-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3c079-132">Tableau qui contient les ID des réseaux locaux virtuels que le système peut supprimer du point de terminaison Trunk.</span><span class="sxs-lookup"><span data-stu-id="3c079-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3c079-133">Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="3c079-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c079-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="3c079-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c079-135">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c079-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c079-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c079-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3c079-137">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="3c079-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3c079-138">Tableau qui contient les ID des points de terminaison de réseau local virtuel avec le Trunking activé.</span><span class="sxs-lookup"><span data-stu-id="3c079-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="3c079-139">Cette propriété est utilisée uniquement lorsque le point de terminaison VLAN fonctionne en mode Trunking, qui est spécifié dans la propriété **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="3c079-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c079-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c079-140">Requirements</span></span>



| <span data-ttu-id="3c079-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c079-141">Requirement</span></span> | <span data-ttu-id="3c079-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c079-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c079-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c079-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3c079-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3c079-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3c079-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c079-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3c079-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3c079-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3c079-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c079-147">Namespace</span></span><br/>                | <span data-ttu-id="3c079-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c079-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c079-149">MOF</span><span class="sxs-lookup"><span data-stu-id="3c079-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c079-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c079-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c079-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3c079-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c079-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c079-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c079-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c079-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c079-154">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3c079-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

