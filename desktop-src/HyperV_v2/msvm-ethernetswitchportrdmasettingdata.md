---
description: Représente les données du paramètre de fonctionnalité RDMA du port.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Classe Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869273"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="90961-103">MSVM \_ EthernetSwitchPortRdmaSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="90961-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="90961-104">Représente les données du paramètre de fonctionnalité RDMA du port.</span><span class="sxs-lookup"><span data-stu-id="90961-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="90961-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="90961-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90961-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90961-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="90961-107">Membres</span><span class="sxs-lookup"><span data-stu-id="90961-107">Members</span></span>

<span data-ttu-id="90961-108">La classe **MSVM \_ EthernetSwitchPortRdmaSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90961-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="90961-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90961-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90961-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90961-110">Properties</span></span>

<span data-ttu-id="90961-111">La classe **MSVM \_ EthernetSwitchPortRdmaSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="90961-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90961-112">**RdmaOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="90961-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90961-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90961-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90961-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="90961-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90961-115">Qualificateurs : **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="90961-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="90961-116">Poids affecté à ce port pour l’invité RDMA.</span><span class="sxs-lookup"><span data-stu-id="90961-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="90961-117">Le poids est l’importance relative lors de l’affectation de ressources RDMA.</span><span class="sxs-lookup"><span data-stu-id="90961-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="90961-118">L’affectation de la valeur 0 à la propriété **RdmaOffloadWeight** désactive RDMA sur le port.</span><span class="sxs-lookup"><span data-stu-id="90961-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="90961-119">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="90961-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90961-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90961-120">Requirements</span></span>



| <span data-ttu-id="90961-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90961-121">Requirement</span></span> | <span data-ttu-id="90961-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="90961-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90961-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90961-123">Minimum supported client</span></span><br/> | <span data-ttu-id="90961-124">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90961-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90961-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90961-125">Minimum supported server</span></span><br/> | <span data-ttu-id="90961-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="90961-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="90961-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90961-127">Namespace</span></span><br/>                | <span data-ttu-id="90961-128">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="90961-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90961-129">MOF</span><span class="sxs-lookup"><span data-stu-id="90961-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90961-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90961-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90961-131">DLL</span><span class="sxs-lookup"><span data-stu-id="90961-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90961-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90961-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90961-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90961-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90961-134">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="90961-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




