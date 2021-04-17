---
description: Classe d’association entre un composant d’interface de service invité et la ressource de service invité.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Classe Msvm_GuestServiceInterfaceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201602"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="6d9cb-103">MSVM \_ GuestServiceInterfaceSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="6d9cb-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="6d9cb-104">Classe d’association entre un composant d’interface de service invité et la ressource de service invité.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="6d9cb-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9cb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d9cb-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6d9cb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6d9cb-107">Members</span></span>

<span data-ttu-id="6d9cb-108">La classe **MSVM \_ GuestServiceInterfaceSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6d9cb-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="6d9cb-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d9cb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d9cb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6d9cb-110">Properties</span></span>

<span data-ttu-id="6d9cb-111">La classe **MSVM \_ GuestServiceInterfaceSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d9cb-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6d9cb-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9cb-113">Type de données : **MSVM \_ GuestServiceInterfaceComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="6d9cb-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6d9cb-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d9cb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9cb-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**substitution**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6d9cb-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6d9cb-116">Un [**\_ GuestServiceInterfaceComponentSettingData MSVM**](msvm-guestserviceinterfacecomponentsettingdata.md) référençant le composant d’interface de service invité.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="6d9cb-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6d9cb-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9cb-118">Type de données **: \_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="6d9cb-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="6d9cb-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6d9cb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9cb-120">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6d9cb-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6d9cb-121">[**\_ SettingData CIM**](cim-settingdata.md) qui fait référence à la ressource de service invité.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d9cb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d9cb-122">Requirements</span></span>



| <span data-ttu-id="6d9cb-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d9cb-123">Requirement</span></span> | <span data-ttu-id="6d9cb-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d9cb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9cb-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9cb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9cb-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d9cb-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6d9cb-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9cb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9cb-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6d9cb-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6d9cb-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d9cb-129">Namespace</span></span><br/>                | <span data-ttu-id="6d9cb-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6d9cb-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6d9cb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9cb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9cb-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d9cb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d9cb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9cb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9cb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d9cb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6d9cb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d9cb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9cb-136">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="6d9cb-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

