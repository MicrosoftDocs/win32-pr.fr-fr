---
description: Fournit des informations détaillées sur une image de stockage montée manuellement.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759651"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="bb977-103">MSVM \_ MountedStorageImage, classe</span><span class="sxs-lookup"><span data-stu-id="bb977-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="bb977-104">Fournit des informations détaillées sur une image de stockage montée manuellement.</span><span class="sxs-lookup"><span data-stu-id="bb977-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="bb977-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bb977-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb977-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb977-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="bb977-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bb977-107">Members</span></span>

<span data-ttu-id="bb977-108">La classe **MSVM \_ MountedStorageImage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bb977-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="bb977-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb977-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb977-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb977-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb977-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb977-111">Methods</span></span>

<span data-ttu-id="bb977-112">La classe **MSVM \_ MountedStorageImage** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bb977-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="bb977-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="bb977-113">Method</span></span>                                                                          | <span data-ttu-id="bb977-114">Description</span><span class="sxs-lookup"><span data-stu-id="bb977-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="bb977-115">**DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="bb977-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="bb977-116">Détache l’image de stockage montée.</span><span class="sxs-lookup"><span data-stu-id="bb977-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bb977-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb977-117">Properties</span></span>

<span data-ttu-id="bb977-118">La classe **MSVM \_ MountedStorageImage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb977-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb977-119">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="bb977-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-120">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-122">Accès sous lequel l’image de stockage est montée.</span><span class="sxs-lookup"><span data-stu-id="bb977-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="bb977-123">**Lecture seule** (1)</span><span class="sxs-lookup"><span data-stu-id="bb977-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="bb977-124">**Lecture/écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="bb977-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb977-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bb977-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-128">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bb977-128">A short description of the object.</span></span> <span data-ttu-id="bb977-129">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et contient toujours « image de stockage montée ».</span><span class="sxs-lookup"><span data-stu-id="bb977-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="bb977-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="bb977-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-133">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="bb977-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bb977-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="bb977-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-138">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="bb977-138">A description of the object.</span></span> <span data-ttu-id="bb977-139">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et contient toujours « informations sur une image de stockage montée ».</span><span class="sxs-lookup"><span data-stu-id="bb977-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="bb977-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bb977-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-141">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-143">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bb977-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bb977-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bb977-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-148">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bb977-148">A display name for the object.</span></span> <span data-ttu-id="bb977-149">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et contient toujours « image de stockage montée ».</span><span class="sxs-lookup"><span data-stu-id="bb977-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="bb977-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bb977-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-153">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="bb977-153">The current health of the element.</span></span> <span data-ttu-id="bb977-154">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="bb977-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="bb977-155">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="bb977-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="bb977-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="bb977-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bb977-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-158">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bb977-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-160">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="bb977-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="bb977-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bb977-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bb977-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb977-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb977-165">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="bb977-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bb977-166">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="bb977-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bb977-167">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-168">**Lun**</span><span class="sxs-lookup"><span data-stu-id="bb977-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-169">Type de données : **UINT8**</span><span class="sxs-lookup"><span data-stu-id="bb977-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb977-171">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb977-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb977-172">ID d’unité logique d’adresse SCSI.</span><span class="sxs-lookup"><span data-stu-id="bb977-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-173">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bb977-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-176">Chemin d’accès au disque dur virtuel monté.</span><span class="sxs-lookup"><span data-stu-id="bb977-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="bb977-177">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bb977-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bb977-178">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="bb977-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-181">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bb977-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bb977-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bb977-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-184">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb977-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-186">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bb977-186">The current status of the object.</span></span> <span data-ttu-id="bb977-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-188">**PathId**</span><span class="sxs-lookup"><span data-stu-id="bb977-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-189">Type de données : **UINT8**</span><span class="sxs-lookup"><span data-stu-id="bb977-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb977-191">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb977-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb977-192">ID du chemin d’accès de l’adresse SCSI.</span><span class="sxs-lookup"><span data-stu-id="bb977-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-193">**PnpDevicePath**</span><span class="sxs-lookup"><span data-stu-id="bb977-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-196">Chemin d’accès du périphérique PNP.</span><span class="sxs-lookup"><span data-stu-id="bb977-196">The PNP device path.</span></span>

<span data-ttu-id="bb977-197">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="bb977-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-198">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="bb977-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-199">Type de données : **UINT8**</span><span class="sxs-lookup"><span data-stu-id="bb977-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb977-201">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb977-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb977-202">Numéro de port de l’adresse SCSI.</span><span class="sxs-lookup"><span data-stu-id="bb977-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-203">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="bb977-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-204">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-206">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="bb977-206">Provides high level status information.</span></span> <span data-ttu-id="bb977-207">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="bb977-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="bb977-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="bb977-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-209">**État**</span><span class="sxs-lookup"><span data-stu-id="bb977-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb977-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="bb977-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="bb977-213">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bb977-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-214">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="bb977-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb977-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-216">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="bb977-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="bb977-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="bb977-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="bb977-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="bb977-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-219">Type de données : **UINT8**</span><span class="sxs-lookup"><span data-stu-id="bb977-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb977-221">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb977-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bb977-222">ID cible de l’adresse SCSI.</span><span class="sxs-lookup"><span data-stu-id="bb977-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="bb977-223">**Type**</span><span class="sxs-lookup"><span data-stu-id="bb977-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb977-224">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb977-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb977-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb977-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb977-226">Type d’image de stockage monté.</span><span class="sxs-lookup"><span data-stu-id="bb977-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="bb977-227">**Disque dur virtuel** (0)</span><span class="sxs-lookup"><span data-stu-id="bb977-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="bb977-228">**Image ISO** (1)</span><span class="sxs-lookup"><span data-stu-id="bb977-228">**ISO Image** (1)</span></span>


<span data-ttu-id="bb977-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bb977-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="bb977-230">Notes</span><span class="sxs-lookup"><span data-stu-id="bb977-230">Remarks</span></span>

<span data-ttu-id="bb977-231">L’accès à la classe **MSVM \_ MountedStorageImage** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="bb977-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bb977-232">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bb977-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb977-233">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb977-233">Requirements</span></span>



| <span data-ttu-id="bb977-234">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb977-234">Requirement</span></span> | <span data-ttu-id="bb977-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb977-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb977-236">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb977-236">Minimum supported client</span></span><br/> | <span data-ttu-id="bb977-237">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb977-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb977-238">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb977-238">Minimum supported server</span></span><br/> | <span data-ttu-id="bb977-239">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb977-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb977-240">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bb977-240">Namespace</span></span><br/>                | <span data-ttu-id="bb977-241">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb977-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb977-242">MOF</span><span class="sxs-lookup"><span data-stu-id="bb977-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb977-243"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb977-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb977-244">DLL</span><span class="sxs-lookup"><span data-stu-id="bb977-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb977-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb977-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb977-246">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb977-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb977-247">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bb977-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="bb977-248">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bb977-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="bb977-249">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="bb977-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

