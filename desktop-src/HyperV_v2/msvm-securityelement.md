---
description: Représente les paramètres de sécurité du runtime d’un \_ ComputerSystem CIM.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Classe Msvm_SecurityElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953257"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="e65f5-103">MSVM \_ SecurityElement, classe</span><span class="sxs-lookup"><span data-stu-id="e65f5-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="e65f5-104">Représente les paramètres de sécurité du runtime d’un [**\_ ComputerSystem CIM**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="e65f5-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="e65f5-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e65f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e65f5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e65f5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="e65f5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e65f5-107">Members</span></span>

<span data-ttu-id="e65f5-108">La classe **MSVM \_ SecurityElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e65f5-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e65f5-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e65f5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e65f5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e65f5-110">Properties</span></span>

<span data-ttu-id="e65f5-111">La classe **MSVM \_ SecurityElement** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e65f5-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e65f5-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e65f5-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e65f5-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e65f5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e65f5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e65f5-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e65f5-116">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e65f5-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="e65f5-117">En cas d’utilisation avec les autres propriétés de clé de cette classe, **CreationClassName** permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e65f5-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="e65f5-118">**EncryptStateAndVmMigrationTrafficEnabled**</span><span class="sxs-lookup"><span data-stu-id="e65f5-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e65f5-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e65f5-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e65f5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e65f5-121">Indique si l’État et le trafic de migration de la machine virtuelle sont actuellement chiffrés.</span><span class="sxs-lookup"><span data-stu-id="e65f5-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="e65f5-122">**Protégé**</span><span class="sxs-lookup"><span data-stu-id="e65f5-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e65f5-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e65f5-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e65f5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e65f5-125">Indique si la machine virtuelle est actuellement protégée.</span><span class="sxs-lookup"><span data-stu-id="e65f5-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="e65f5-126">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e65f5-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e65f5-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e65f5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e65f5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-129">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="e65f5-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="e65f5-130">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e65f5-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="e65f5-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e65f5-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e65f5-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e65f5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e65f5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e65f5-134">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="e65f5-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="e65f5-135">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e65f5-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e65f5-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e65f5-136">Requirements</span></span>



| <span data-ttu-id="e65f5-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e65f5-137">Requirement</span></span> | <span data-ttu-id="e65f5-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="e65f5-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e65f5-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e65f5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e65f5-140">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e65f5-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e65f5-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e65f5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e65f5-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e65f5-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e65f5-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e65f5-143">Namespace</span></span><br/>                | <span data-ttu-id="e65f5-144">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e65f5-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e65f5-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e65f5-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e65f5-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e65f5-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e65f5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e65f5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e65f5-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e65f5-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e65f5-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e65f5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65f5-150">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e65f5-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

