---
description: Décrit les fonctionnalités du ExternalEthernetPort MSVM associé \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Classe Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862945"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="e6302-103">MSVM \_ ExternalEthernetPortCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="e6302-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="e6302-104">Décrit les fonctionnalités du [**\_ ExternalEthernetPort MSVM**](msvm-externalethernetport.md)associé.</span><span class="sxs-lookup"><span data-stu-id="e6302-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="e6302-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e6302-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6302-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6302-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="e6302-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e6302-107">Members</span></span>

<span data-ttu-id="e6302-108">La classe **MSVM \_ ExternalEthernetPortCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6302-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e6302-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6302-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6302-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6302-110">Properties</span></span>

<span data-ttu-id="e6302-111">La classe **MSVM \_ ExternalEthernetPortCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6302-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6302-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e6302-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6302-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6302-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6302-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e6302-115">A short description of the object.</span></span> <span data-ttu-id="e6302-116">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="e6302-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="e6302-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="e6302-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6302-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6302-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6302-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="e6302-120">A description of the object.</span></span> <span data-ttu-id="e6302-121">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « décrit les fonctionnalités du port Ethernet externe Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="e6302-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="e6302-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e6302-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6302-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6302-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6302-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e6302-125">A display name for the object.</span></span> <span data-ttu-id="e6302-126">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités de port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="e6302-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="e6302-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6302-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6302-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6302-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6302-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="e6302-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e6302-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e6302-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e6302-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6302-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6302-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="e6302-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e6302-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6302-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6302-136">Valeur booléenne qui indique si la virtualisation d’e/s (IOV) est prise en charge par la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="e6302-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="e6302-137">Si la valeur est **true**, IOV est pris en charge par la carte réseau et la propriété **iovsupportreasons fourniront** est vide.</span><span class="sxs-lookup"><span data-stu-id="e6302-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="e6302-138">Sinon, la propriété **iovsupportreasons fourniront** aura les raisons pour lesquelles IOV ne peut pas être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6302-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6302-139">**Iovsupportreasons fourniront**</span><span class="sxs-lookup"><span data-stu-id="e6302-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6302-140">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e6302-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6302-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6302-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6302-142">Tableau de chaînes qui indique les raisons possibles pour lesquelles IOV n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6302-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="e6302-143">Si la valeur de **IOVSupport** est **true**, ce tableau sera vide.</span><span class="sxs-lookup"><span data-stu-id="e6302-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6302-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6302-144">Requirements</span></span>



| <span data-ttu-id="e6302-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6302-145">Requirement</span></span> | <span data-ttu-id="e6302-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6302-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6302-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6302-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e6302-148">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6302-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6302-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6302-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e6302-150">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6302-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6302-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6302-151">Namespace</span></span><br/>                | <span data-ttu-id="e6302-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6302-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6302-153">MOF</span><span class="sxs-lookup"><span data-stu-id="e6302-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6302-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6302-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6302-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e6302-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6302-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6302-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

