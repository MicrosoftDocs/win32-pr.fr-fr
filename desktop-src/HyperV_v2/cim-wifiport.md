---
description: Représente un périphérique de communication de réseau local sans fil conforme à la série IEEE 802,11 de spécifications.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: Classe CIM_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865778"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="7aeea-103">\_Classe CIM WiFiPort</span><span class="sxs-lookup"><span data-stu-id="7aeea-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="7aeea-104">Représente un périphérique de communication de réseau local sans fil conforme à la série IEEE 802,11 de spécifications.</span><span class="sxs-lookup"><span data-stu-id="7aeea-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aeea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7aeea-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="7aeea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7aeea-106">Members</span></span>

<span data-ttu-id="7aeea-107">La classe **CIM \_ WiFiPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7aeea-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="7aeea-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7aeea-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7aeea-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7aeea-109">Properties</span></span>

<span data-ttu-id="7aeea-110">La classe **CIM \_ WiFiPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7aeea-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7aeea-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="7aeea-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aeea-112">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aeea-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7aeea-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Maxspeed")</span><span class="sxs-lookup"><span data-stu-id="7aeea-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="7aeea-115">Bande passante maximale prise en charge, en bits par seconde, en fonction du mode de fonctionnement spécifié dans la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="7aeea-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="7aeea-116">Par exemple, **Maxspeed** est « 11 millions » si **PortType** contient « 71 » (802.11 b).</span><span class="sxs-lookup"><span data-stu-id="7aeea-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="7aeea-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="7aeea-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aeea-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7aeea-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7aeea-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="7aeea-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="7aeea-121">Tableau qui contient les adresses MAC IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="7aeea-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="7aeea-122">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux, chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques.</span><span class="sxs-lookup"><span data-stu-id="7aeea-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="7aeea-123">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="7aeea-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aeea-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7aeea-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7aeea-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-126">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span><span class="sxs-lookup"><span data-stu-id="7aeea-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="7aeea-127">Adresse MAC IEEE 802 EUI-48 du port.</span><span class="sxs-lookup"><span data-stu-id="7aeea-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="7aeea-128">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux, chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques.</span><span class="sxs-lookup"><span data-stu-id="7aeea-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="7aeea-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="7aeea-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aeea-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7aeea-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7aeea-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-132">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="7aeea-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="7aeea-133">Mode d’opération 802,11 activé sur le port.</span><span class="sxs-lookup"><span data-stu-id="7aeea-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7aeea-134">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="7aeea-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7aeea-135">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="7aeea-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="7aeea-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="7aeea-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="7aeea-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="7aeea-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="7aeea-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="7aeea-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="7aeea-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="7aeea-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7aeea-140">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7aeea-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7aeea-141">**Fournisseur réservé** (16000...)</span><span class="sxs-lookup"><span data-stu-id="7aeea-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7aeea-142">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="7aeea-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aeea-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aeea-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7aeea-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aeea-145">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span><span class="sxs-lookup"><span data-stu-id="7aeea-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="7aeea-146">Débit de données auquel l’unité de données de protocole PPDU (PLCP (Physical Layer convergence Protocol) actuelle a été reçue, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="7aeea-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="7aeea-147">Cette valeur est encodée dans les 4 premiers bits de l’en-tête PLCP dans chaque frame PLCP.</span><span class="sxs-lookup"><span data-stu-id="7aeea-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7aeea-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7aeea-148">Requirements</span></span>



| <span data-ttu-id="7aeea-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7aeea-149">Requirement</span></span> | <span data-ttu-id="7aeea-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="7aeea-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aeea-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7aeea-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7aeea-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7aeea-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7aeea-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7aeea-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7aeea-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7aeea-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7aeea-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7aeea-155">Namespace</span></span><br/>                | <span data-ttu-id="7aeea-156">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7aeea-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7aeea-157">MOF</span><span class="sxs-lookup"><span data-stu-id="7aeea-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aeea-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7aeea-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7aeea-159">DLL</span><span class="sxs-lookup"><span data-stu-id="7aeea-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aeea-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7aeea-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7aeea-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7aeea-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aeea-162">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="7aeea-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

