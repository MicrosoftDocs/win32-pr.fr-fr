---
description: Représente les paramètres pour l’allocation de stockage virtuel.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756621"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="8d859-103">\_Classe CIM StorageAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="8d859-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="8d859-104">Représente les paramètres pour l’allocation de stockage virtuel.</span><span class="sxs-lookup"><span data-stu-id="8d859-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d859-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d859-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="8d859-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8d859-106">Members</span></span>

<span data-ttu-id="8d859-107">La classe **CIM \_ StorageAllocationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d859-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8d859-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d859-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d859-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d859-109">Properties</span></span>

<span data-ttu-id="8d859-110">La classe **CIM \_ StorageAllocationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8d859-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d859-111">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="8d859-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d859-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-114">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Accès**»)</span><span class="sxs-lookup"><span data-stu-id="8d859-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-115">Prise en charge en lecture/écriture de l’allocation de stockage.</span><span class="sxs-lookup"><span data-stu-id="8d859-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d859-116">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8d859-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="8d859-117">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="8d859-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="8d859-118">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="8d859-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="8d859-119">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="8d859-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8d859-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8d859-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d859-121">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="8d859-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d859-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-124">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="8d859-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-125">Identificateur unique de l’étendue de stockage hôte.</span><span class="sxs-lookup"><span data-stu-id="8d859-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-126">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="8d859-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d859-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-129">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**»)</span><span class="sxs-lookup"><span data-stu-id="8d859-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-130">Format de la valeur de la propriété **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="8d859-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d859-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8d859-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8d859-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8d859-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="8d859-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="8d859-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8d859-134">Numéro de série/fournisseur/modèle (SNVM) SNVM est 3 chaînes représentant le nom du fournisseur, le nom du produit dans l’espace de noms du fournisseur et le numéro de série dans l’espace de noms du modèle.</span><span class="sxs-lookup"><span data-stu-id="8d859-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="8d859-135">Les chaînes sont délimitées par un' + '.</span><span class="sxs-lookup"><span data-stu-id="8d859-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="8d859-136">Les espaces peuvent être inclus et significatifs.</span><span class="sxs-lookup"><span data-stu-id="8d859-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="8d859-137">Le numéro de série est la représentation textuelle du numéro de série en majuscules hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="8d859-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="8d859-138">Cela représente le fournisseur et l’ID de modèle des données de recherche SCSI ; le champ Vendor doit avoir une largeur de 8 caractères et le champ Product doit avoir une largeur de 16 caractères.</span><span class="sxs-lookup"><span data-stu-id="8d859-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="8d859-139">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="8d859-139">For example,</span></span>

<span data-ttu-id="8d859-140">« Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458 » ( \_ est un espace)</span><span class="sxs-lookup"><span data-stu-id="8d859-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="8d859-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="8d859-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8d859-142">9 = NAA comme format générique.</span><span class="sxs-lookup"><span data-stu-id="8d859-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="8d859-143">Consultez</span><span class="sxs-lookup"><span data-stu-id="8d859-143">See</span></span>

<span data-ttu-id="8d859-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="8d859-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="8d859-145">Mise en forme en tant que 16 ou 32 caractères hexadécimaux non séparés (2 par octet binaire).</span><span class="sxs-lookup"><span data-stu-id="8d859-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="8d859-146">Par exemple, ' 21000020372D3C73 '</span><span class="sxs-lookup"><span data-stu-id="8d859-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="8d859-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="8d859-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8d859-148">EUI comme format générique (EUI64) consultez</span><span class="sxs-lookup"><span data-stu-id="8d859-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="8d859-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="8d859-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="8d859-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="8d859-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8d859-151">Format d’identificateur de fournisseur T10 tel qu’il est retourné par la page d’interrogation SCSI 83, type d’identificateur 1.</span><span class="sxs-lookup"><span data-stu-id="8d859-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="8d859-152">Consultez la spécification de T10 SPC-3.</span><span class="sxs-lookup"><span data-stu-id="8d859-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="8d859-153">Il s’agit de l’ID de fournisseur ASCII de 8 octets du registre de T10 suivi d’un identificateur ASCII spécifique au fournisseur ; les espaces sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="8d859-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="8d859-154">Pour les volumes non-SCSI, « SNVM » peut être le choix le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="8d859-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="8d859-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nom du périphérique du système d’exploitation** (12)</span><span class="sxs-lookup"><span data-stu-id="8d859-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="8d859-156">Nom du périphérique du système d’exploitation (pour LogicalDisks).</span><span class="sxs-lookup"><span data-stu-id="8d859-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="8d859-157">Pour plus d’informations, consultez Description du nom de disque logique.</span><span class="sxs-lookup"><span data-stu-id="8d859-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8d859-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8d859-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d859-159">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="8d859-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-160">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d859-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-162">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Espace de noms**»)</span><span class="sxs-lookup"><span data-stu-id="8d859-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-163">Format d’affectation de noms pour la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="8d859-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d859-164">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8d859-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8d859-165">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8d859-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="8d859-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="8d859-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="8d859-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="8d859-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="8d859-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="8d859-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="8d859-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="8d859-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="8d859-170">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="8d859-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="8d859-171">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="8d859-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="8d859-172">**Espace de noms du périphérique du système d’exploitation** (8)</span><span class="sxs-lookup"><span data-stu-id="8d859-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8d859-173">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8d859-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d859-174">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="8d859-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-175">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-177">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**CIM \_ BasedOn**](cim-basedon.md).\*\*\*\* De l’un des»)</span><span class="sxs-lookup"><span data-stu-id="8d859-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-178">Adresse de départ sur l’étendue de stockage de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="8d859-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="8d859-179">Valeur NULL ; UE indique qu’il n’existe pas de mappage direct entre l’extension de stockage virtuel et l’extension de stockage hôte.</span><span class="sxs-lookup"><span data-stu-id="8d859-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-180">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="8d859-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-181">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-183">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Blocksize**"), **punitif** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="8d859-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-184">Taille, en octets, des blocs alloués sur l’hôte pour l’allocation de stockage.</span><span class="sxs-lookup"><span data-stu-id="8d859-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="8d859-185">Si la taille de bloc est variable, la taille de bloc maximale en octets doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8d859-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="8d859-186">Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur « 1 » (inconnu) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="8d859-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="8d859-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-188">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-190">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="8d859-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-191">Nombre maximal de blocs qui seront accordés pour l’allocation des ressources de stockage sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="8d859-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="8d859-192">La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="8d859-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-193">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="8d859-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d859-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-196">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="8d859-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-197">Format de la propriété **HostExtentName** si la propriété a la valeur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="8d859-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="8d859-198">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="8d859-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d859-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-201">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="8d859-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-202">Chaîne qui décrit l’espace de noms de la propriété **HostExtentName** si la valeur de la propriété **HostExtentNameNamespace** est « 1 » (other).</span><span class="sxs-lookup"><span data-stu-id="8d859-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="8d859-203">**Réservation**</span><span class="sxs-lookup"><span data-stu-id="8d859-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-204">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-206">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="8d859-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-207">Quantité de blocs dont la disponibilité est garantie pour l’allocation des ressources de stockage sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="8d859-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="8d859-208">La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="8d859-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8d859-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-210">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-212">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="8d859-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-213">Nombre de blocs que l’allocation de stockage présente au consommateur.</span><span class="sxs-lookup"><span data-stu-id="8d859-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="8d859-214">La propriété **VirtualQuantity** peut spécifier une taille de bloc de « 1 », même si **VirtualResourceBlockSize** est inconnu.</span><span class="sxs-lookup"><span data-stu-id="8d859-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="8d859-215">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="8d859-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d859-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-218">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="8d859-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="8d859-219">Unités utilisées par la propriété **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="8d859-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="8d859-220">Cette valeur doit être définie sur « nombre (bloc de taille fixe) » ou « octet ».</span><span class="sxs-lookup"><span data-stu-id="8d859-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="8d859-221">La valeur par défaut, « nombre (bloc de taille fixe) » doit être utilisée pour une taille de bloc fixe, et « octet » doit être utilisé pour une taille de bloc inconnue ou variable.</span><span class="sxs-lookup"><span data-stu-id="8d859-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="8d859-222">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="8d859-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d859-223">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d859-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d859-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d859-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d859-225">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Blocksize**"), **punitif** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="8d859-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="8d859-226">Taille, en octets, des blocs qui forment la demande d’allocation de stockage.</span><span class="sxs-lookup"><span data-stu-id="8d859-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="8d859-227">Si la taille de bloc est variable, la taille de bloc maximale doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8d859-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="8d859-228">Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la taille de bloc doit être « 1 » (inconnu).</span><span class="sxs-lookup"><span data-stu-id="8d859-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d859-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d859-229">Requirements</span></span>



| <span data-ttu-id="8d859-230">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d859-230">Requirement</span></span> | <span data-ttu-id="8d859-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d859-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d859-232">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d859-232">Minimum supported client</span></span><br/> | <span data-ttu-id="8d859-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8d859-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8d859-234">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d859-234">Minimum supported server</span></span><br/> | <span data-ttu-id="8d859-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d859-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8d859-236">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d859-236">Namespace</span></span><br/>                | <span data-ttu-id="8d859-237">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8d859-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8d859-238">MOF</span><span class="sxs-lookup"><span data-stu-id="8d859-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d859-239"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d859-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d859-240">DLL</span><span class="sxs-lookup"><span data-stu-id="8d859-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d859-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d859-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8d859-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d859-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d859-243">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="8d859-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

