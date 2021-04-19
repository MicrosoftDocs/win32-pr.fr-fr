---
description: Représente les données de paramètre de la fonctionnalité de mappage de l’équipe des ports.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Classe Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538406"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="cb0d5-103">MSVM \_ EthernetSwitchPortTeamMappingSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="cb0d5-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="cb0d5-104">Représente les données de paramètre de la fonctionnalité de mappage de l’équipe des ports.</span><span class="sxs-lookup"><span data-stu-id="cb0d5-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="cb0d5-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb0d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb0d5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb0d5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="cb0d5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cb0d5-107">Members</span></span>

<span data-ttu-id="cb0d5-108">La classe **MSVM \_ EthernetSwitchPortTeamMappingSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb0d5-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cb0d5-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb0d5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb0d5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb0d5-110">Properties</span></span>

<span data-ttu-id="cb0d5-111">La classe **MSVM \_ EthernetSwitchPortTeamMappingSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb0d5-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb0d5-112">**NetAdapterDeviceId**</span><span class="sxs-lookup"><span data-stu-id="cb0d5-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb0d5-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb0d5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb0d5-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb0d5-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cb0d5-115">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cb0d5-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cb0d5-116">ID d’appareil de la carte physique mappée préférée.</span><span class="sxs-lookup"><span data-stu-id="cb0d5-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="cb0d5-117">**NetAdapterName**</span><span class="sxs-lookup"><span data-stu-id="cb0d5-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb0d5-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb0d5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb0d5-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb0d5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cb0d5-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="cb0d5-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="cb0d5-121">Nom de la carte physique mappée préférée.</span><span class="sxs-lookup"><span data-stu-id="cb0d5-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb0d5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb0d5-122">Requirements</span></span>



| <span data-ttu-id="cb0d5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb0d5-123">Requirement</span></span> | <span data-ttu-id="cb0d5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb0d5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0d5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb0d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cb0d5-126">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb0d5-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb0d5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb0d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cb0d5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb0d5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cb0d5-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb0d5-129">Namespace</span></span><br/>                | <span data-ttu-id="cb0d5-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb0d5-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb0d5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cb0d5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb0d5-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb0d5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb0d5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cb0d5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb0d5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb0d5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb0d5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb0d5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0d5-136">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="cb0d5-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

