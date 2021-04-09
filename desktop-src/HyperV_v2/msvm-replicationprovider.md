---
description: Représente les fournisseurs disponibles pour la réplication.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Classe Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865521"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="d1667-103">MSVM \_ ReplicationProvider, classe</span><span class="sxs-lookup"><span data-stu-id="d1667-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="d1667-104">Représente les fournisseurs disponibles pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="d1667-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="d1667-105">La syntaxe suivante est simplifiée à partir du code MOF et comprend les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d1667-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1667-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1667-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="d1667-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d1667-107">Members</span></span>

<span data-ttu-id="d1667-108">La classe **MSVM \_ ReplicationProvider** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1667-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="d1667-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1667-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1667-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1667-110">Properties</span></span>

<span data-ttu-id="d1667-111">La classe **MSVM \_ ReplicationProvider** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1667-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1667-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1667-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1667-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1667-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1667-115">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="d1667-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1667-116">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1667-116">A short description of the object.</span></span> <span data-ttu-id="d1667-117">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1667-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d1667-118">Pour cet objet, la valeur est :</span><span class="sxs-lookup"><span data-stu-id="d1667-118">For this object, the value is:</span></span>

<span data-ttu-id="d1667-119">« Fournisseur de réplication »</span><span class="sxs-lookup"><span data-stu-id="d1667-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="d1667-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="d1667-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1667-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1667-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1667-123">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d1667-123">A description of the object.</span></span> <span data-ttu-id="d1667-124">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1667-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d1667-125">Pour les fournisseurs externes, la valeur est fournie par ces derniers.</span><span class="sxs-lookup"><span data-stu-id="d1667-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="d1667-126">Pour que l’hôte héberge le fournisseur intégré, la valeur est :</span><span class="sxs-lookup"><span data-stu-id="d1667-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="d1667-127">« Fournisseur de réplication d’ordinateur virtuel sur l’hôte Hyper-V »</span><span class="sxs-lookup"><span data-stu-id="d1667-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="d1667-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d1667-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1667-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1667-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1667-131">Nom complet du fournisseur de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d1667-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="d1667-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1667-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="d1667-133">Pour Host pour héberger le fournisseur incorporé, cette propriété a toujours la valeur :</span><span class="sxs-lookup"><span data-stu-id="d1667-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="d1667-134">« Fournisseur de réplication d’ordinateur virtuel sur l’hôte Hyper-V »</span><span class="sxs-lookup"><span data-stu-id="d1667-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="d1667-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1667-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1667-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1667-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1667-138">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="d1667-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1667-139">L’ID d’instance WMI, qui identifie le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d1667-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="d1667-140">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d1667-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="d1667-141">Le format de cette propriété est « Microsoft : <Host-machine-name>\\ ReplicationProvider \\<Provider-Name> ».</span><span class="sxs-lookup"><span data-stu-id="d1667-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="d1667-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d1667-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1667-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1667-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1667-145">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d1667-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1667-146">Identificateur global unique (GUID) du fournisseur qui identifie le fournisseur de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d1667-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="d1667-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d1667-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d1667-148">Dans le cas d’un fournisseur externe, cette propriété est le CLSID de l’objet classe COM du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d1667-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="d1667-149">Pour que l’hôte héberge le fournisseur incorporé, cette propriété est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="d1667-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="d1667-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="d1667-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="d1667-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d1667-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1667-152">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1667-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1667-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1667-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1667-154">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1667-154">The current statuses of the object.</span></span> <span data-ttu-id="d1667-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur :</span><span class="sxs-lookup"><span data-stu-id="d1667-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="d1667-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d1667-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1667-157">Notes</span><span class="sxs-lookup"><span data-stu-id="d1667-157">Remarks</span></span>

<span data-ttu-id="d1667-158">Vous pouvez utiliser n’importe quel fournisseur disponible et la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour activer une relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="d1667-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="d1667-159">Par défaut, Hyper-V choisit l’hôte intégré au fournisseur hôte, qui peut être modifié lors de la création de la réplication.</span><span class="sxs-lookup"><span data-stu-id="d1667-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="d1667-160">Le service de gestion Hyper-V communique avec un fournisseur externe à l’aide de COM.</span><span class="sxs-lookup"><span data-stu-id="d1667-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1667-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1667-161">Requirements</span></span>



| <span data-ttu-id="d1667-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1667-162">Requirement</span></span> | <span data-ttu-id="d1667-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1667-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1667-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1667-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d1667-165">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1667-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d1667-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1667-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d1667-167">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1667-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1667-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d1667-168">Namespace</span></span><br/>                | <span data-ttu-id="d1667-169">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1667-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1667-170">MOF</span><span class="sxs-lookup"><span data-stu-id="d1667-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1667-171"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1667-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1667-172">DLL</span><span class="sxs-lookup"><span data-stu-id="d1667-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1667-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1667-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1667-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1667-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1667-175">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d1667-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="d1667-176">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d1667-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

