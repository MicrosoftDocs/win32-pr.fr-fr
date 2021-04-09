---
description: Représente les paramètres du service de communication invité.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Classe Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113635"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="37bc1-103">MSVM \_ GuestCommunicationServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="37bc1-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="37bc1-104">Représente les paramètres du service de communication invité.</span><span class="sxs-lookup"><span data-stu-id="37bc1-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="37bc1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37bc1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bc1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37bc1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="37bc1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="37bc1-107">Members</span></span>

<span data-ttu-id="37bc1-108">La classe **MSVM \_ GuestCommunicationServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37bc1-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="37bc1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37bc1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37bc1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37bc1-110">Properties</span></span>

<span data-ttu-id="37bc1-111">La classe **MSVM \_ GuestCommunicationServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="37bc1-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37bc1-112">**EnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="37bc1-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bc1-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37bc1-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37bc1-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37bc1-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="37bc1-115">EnabledStatePolicy est une énumération entière qui indique l’état activé, désactivé ou par défaut **du \_ GuestCommunicationServiceSettingData MSVM**.</span><span class="sxs-lookup"><span data-stu-id="37bc1-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37bc1-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="37bc1-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="37bc1-117">Le service de communication est défini sur l’état activé.</span><span class="sxs-lookup"><span data-stu-id="37bc1-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37bc1-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="37bc1-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37bc1-119">Le service de communication est défini sur l’état désactivé.</span><span class="sxs-lookup"><span data-stu-id="37bc1-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="37bc1-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Différé** (8)</span><span class="sxs-lookup"><span data-stu-id="37bc1-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="37bc1-121">L’état du service de communication dépend de **DefaultEnabledStatePolicy** dans **MSVM \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="37bc1-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="37bc1-122">**Nom**</span><span class="sxs-lookup"><span data-stu-id="37bc1-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bc1-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37bc1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bc1-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37bc1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37bc1-125">GUID du service.</span><span class="sxs-lookup"><span data-stu-id="37bc1-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37bc1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37bc1-126">Requirements</span></span>



| <span data-ttu-id="37bc1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37bc1-127">Requirement</span></span> | <span data-ttu-id="37bc1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="37bc1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bc1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bc1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="37bc1-130">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37bc1-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="37bc1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bc1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="37bc1-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37bc1-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37bc1-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37bc1-133">Namespace</span></span><br/>                | <span data-ttu-id="37bc1-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37bc1-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37bc1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="37bc1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37bc1-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37bc1-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37bc1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="37bc1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37bc1-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37bc1-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37bc1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37bc1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bc1-140">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="37bc1-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




