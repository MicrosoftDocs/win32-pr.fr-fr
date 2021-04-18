---
description: Décrit les données de paramètres d’un commutateur Ethernet virtuel.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519846"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="65e3d-103">\_Classe CIM VirtualEthernetSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="65e3d-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="65e3d-104">Décrit les données de paramètres d’un commutateur Ethernet virtuel.</span><span class="sxs-lookup"><span data-stu-id="65e3d-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e3d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65e3d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="65e3d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="65e3d-106">Members</span></span>

<span data-ttu-id="65e3d-107">La classe **CIM \_ VirtualEthernetSwitchSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65e3d-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="65e3d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65e3d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65e3d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65e3d-109">Properties</span></span>

<span data-ttu-id="65e3d-110">La classe **CIM \_ VirtualEthernetSwitchSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="65e3d-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65e3d-111">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="65e3d-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65e3d-112">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="65e3d-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65e3d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65e3d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65e3d-114">Tableau qui contient les pools de ressources hôtes actuellement associés, ou à associer au commutateur Ethernet, afin d’allouer des connexions Ethernet entre le commutateur Ethernet et un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="65e3d-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="65e3d-115">Chaque valeur non null de cette propriété doit être conforme à **l' \_ URI WBEM \_ UntypedInstancePath** tel que défini dans la spécification « DSP0207 » DMTF.</span><span class="sxs-lookup"><span data-stu-id="65e3d-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="65e3d-116">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="65e3d-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65e3d-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65e3d-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65e3d-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65e3d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65e3d-119">Nombre d’adresses MAC uniques que le commutateur peut apprendre pour l’apprentissage des adresses MAC, tel que défini dans la norme IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="65e3d-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="65e3d-120">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="65e3d-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65e3d-121">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="65e3d-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65e3d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="65e3d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65e3d-123">Tableau qui contient les ID de réseau local virtuel auxquels le commutateur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="65e3d-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65e3d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65e3d-124">Requirements</span></span>



| <span data-ttu-id="65e3d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65e3d-125">Requirement</span></span> | <span data-ttu-id="65e3d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="65e3d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e3d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65e3d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65e3d-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65e3d-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="65e3d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65e3d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65e3d-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65e3d-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="65e3d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65e3d-131">Namespace</span></span><br/>                | <span data-ttu-id="65e3d-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="65e3d-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="65e3d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="65e3d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65e3d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65e3d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65e3d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="65e3d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65e3d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65e3d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="65e3d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65e3d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e3d-138">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="65e3d-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




