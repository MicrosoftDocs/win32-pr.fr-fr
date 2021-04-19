---
description: Le \_ TCPIPPrinterPort Win32&\# 32 ; La classe WMI représente un point d’accès au service TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Classe Win32_TCPIPPrinterPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516396"
---
# <a name="win32_tcpipprinterport-class"></a><span data-ttu-id="8abb6-103">\_Classe TCPIPPrinterPort Win32</span><span class="sxs-lookup"><span data-stu-id="8abb6-103">Win32\_TCPIPPrinterPort class</span></span>

<span data-ttu-id="8abb6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TCPIPPrinterPort** WMI représente un point d’accès au service TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="8abb6-104">The **Win32\_TCPIPPrinterPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a TCP/IP service access point.</span></span>

<span data-ttu-id="8abb6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8abb6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8abb6-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8abb6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8abb6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8abb6-107">Syntax</span></span>

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a><span data-ttu-id="8abb6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8abb6-108">Members</span></span>

<span data-ttu-id="8abb6-109">La classe **Win32 \_ TCPIPPrinterPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8abb6-109">The **Win32\_TCPIPPrinterPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8abb6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8abb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8abb6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8abb6-111">Properties</span></span>

<span data-ttu-id="8abb6-112">La classe **Win32 \_ TCPIPPrinterPort** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8abb6-112">The **Win32\_TCPIPPrinterPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8abb6-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="8abb6-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8abb6-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-116">Si la **valeur est true**, l’ordinateur compte les octets dans un document avant de les envoyer à l’imprimante et l’imprimante renvoie le nombre d’octets réellement lus.</span><span class="sxs-lookup"><span data-stu-id="8abb6-116">If **TRUE**, the computer counts the bytes in a document before sending them to the printer and the printer reports back the number of bytes actually read.</span></span> <span data-ttu-id="8abb6-117">Cette fonctionnalité est utilisée pour les diagnostics quand des octets manquants sont détectés dans le résultat de l’impression.</span><span class="sxs-lookup"><span data-stu-id="8abb6-117">This capability is used for diagnostics when missing bytes are detected in the print output.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8abb6-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-121">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8abb6-122">A short textual description of the object.</span></span>

<span data-ttu-id="8abb6-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8abb6-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-127">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8abb6-127">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-128">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="8abb6-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8abb6-129">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="8abb6-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8abb6-130">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-130">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="8abb6-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-134">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8abb6-134">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8abb6-135">A textual description of the object.</span></span>

<span data-ttu-id="8abb6-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-137">**HostAddress**</span><span class="sxs-lookup"><span data-stu-id="8abb6-137">**HostAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-140">Adresse du périphérique ou du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="8abb6-140">Address of the device or print server.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8abb6-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-142">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8abb6-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-144">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8abb6-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-145">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8abb6-145">Indicates when the object was installed.</span></span> <span data-ttu-id="8abb6-146">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8abb6-146">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8abb6-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-148">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8abb6-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-151">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8abb6-151">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-152">Identifie de façon unique le point d’accès au service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="8abb6-152">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="8abb6-153">Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8abb6-153">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="8abb6-154">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-154">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-155">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="8abb6-155">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-156">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8abb6-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-158">Nombre de ports TCP utilisés par le moniteur de port pour communiquer avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8abb6-158">Number of the TCP ports used by the port monitor to communicate with the device.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-159">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="8abb6-159">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8abb6-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-162">Protocole d’impression utilisé.</span><span class="sxs-lookup"><span data-stu-id="8abb6-162">Printing protocol used.</span></span> <span data-ttu-id="8abb6-163">Certaines imprimantes prennent uniquement en charge LPR.</span><span class="sxs-lookup"><span data-stu-id="8abb6-163">Some printers support only LPR.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8abb6-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8abb6-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8abb6-165">RAW</span><span class="sxs-lookup"><span data-stu-id="8abb6-165">RAW</span></span>

<span data-ttu-id="8abb6-166">Impression directe sur un appareil ou un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="8abb6-166">Printing directly to a device or print server.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8abb6-167"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8abb6-167"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8abb6-168">LPR</span><span class="sxs-lookup"><span data-stu-id="8abb6-168">LPR</span></span>

<span data-ttu-id="8abb6-169">Protocole hérité, qui est finalement remplacé par RAW.</span><span class="sxs-lookup"><span data-stu-id="8abb6-169">Legacy protocol, which is eventually replaced by RAW.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8abb6-170">**File d'attente**</span><span class="sxs-lookup"><span data-stu-id="8abb6-170">**Queue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-173">Nom de la file d’attente à l’impression sur le serveur lorsqu’il est utilisé avec le protocole LPR.</span><span class="sxs-lookup"><span data-stu-id="8abb6-173">Name of the print queue on the server when used with the LPR protocol.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-174">**SNMPCommunity**</span><span class="sxs-lookup"><span data-stu-id="8abb6-174">**SNMPCommunity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-177">Valeur de niveau de sécurité pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8abb6-177">Security level value for the device.</span></span>

<span data-ttu-id="8abb6-178">Exemple : « public »</span><span class="sxs-lookup"><span data-stu-id="8abb6-178">Example: "public'"</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-179">**SNMPDevIndex**</span><span class="sxs-lookup"><span data-stu-id="8abb6-179">**SNMPDevIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-180">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8abb6-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-182">Numéro d’index SNMP de cet appareil pour l’agent SNMP.</span><span class="sxs-lookup"><span data-stu-id="8abb6-182">SNMP index number of this device for the SNMP agent.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-183">**SNMPEnabled**</span><span class="sxs-lookup"><span data-stu-id="8abb6-183">**SNMPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8abb6-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-186">Si la **valeur est true**, cette imprimante prend en charge [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (simple Network Management Protocol) et peut fournir des informations d’État enrichies à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8abb6-186">If **TRUE**, this printer supports [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) and can provide rich status information from the device.</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-187">**État**</span><span class="sxs-lookup"><span data-stu-id="8abb6-187">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-190">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8abb6-190">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-191">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8abb6-191">String that indicates the current status of the object.</span></span> <span data-ttu-id="8abb6-192">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="8abb6-192">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8abb6-193">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="8abb6-193">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8abb6-194">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="8abb6-194">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8abb6-195">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8abb6-195">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8abb6-196">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8abb6-196">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8abb6-197">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8abb6-197">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8abb6-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8abb6-199">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8abb6-199">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8abb6-200">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-200">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8abb6-201">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-201">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8abb6-202">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-202">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8abb6-203">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8abb6-203">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8abb6-204">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-204">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8abb6-205">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-205">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8abb6-206">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-206">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8abb6-207">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-207">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8abb6-208">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-208">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8abb6-209">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-209">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8abb6-210">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-210">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8abb6-211">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8abb6-211">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8abb6-212">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8abb6-212">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-215">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8abb6-215">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-216">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8abb6-216">The scoping system's creation class name.</span></span>

<span data-ttu-id="8abb6-217">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-217">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-218">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8abb6-218">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8abb6-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-221">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8abb6-221">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-222">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8abb6-222">The scoping system's name.</span></span>

<span data-ttu-id="8abb6-223">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-223">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="8abb6-224">**Type**</span><span class="sxs-lookup"><span data-stu-id="8abb6-224">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8abb6-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8abb6-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8abb6-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8abb6-227">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8abb6-227">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8abb6-228">Type de SAP, tel que attaché ou redirigé.</span><span class="sxs-lookup"><span data-stu-id="8abb6-228">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="8abb6-229">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-229">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="8abb6-230">**Écriture** (1)</span><span class="sxs-lookup"><span data-stu-id="8abb6-230">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="8abb6-231">**Lecture** (2)</span><span class="sxs-lookup"><span data-stu-id="8abb6-231">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="8abb6-232">**Redirigé** (4)</span><span class="sxs-lookup"><span data-stu-id="8abb6-232">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="8abb6-233">**Réseau \_ Attaché** (8)</span><span class="sxs-lookup"><span data-stu-id="8abb6-233">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8abb6-234">**inconnu** (16)</span><span class="sxs-lookup"><span data-stu-id="8abb6-234">**unknown** (16)</span></span>


<span data-ttu-id="8abb6-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8abb6-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8abb6-236">Notes</span><span class="sxs-lookup"><span data-stu-id="8abb6-236">Remarks</span></span>

<span data-ttu-id="8abb6-237">La classe **Win32 \_ TCPIPPrinterPort** est dérivée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) qui dérive de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8abb6-237">The **Win32\_TCPIPPrinterPort** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="8abb6-238">Le privilège **SeLoadDriverPrivilege** est requis pour supprimer une instance de cette classe WMI.</span><span class="sxs-lookup"><span data-stu-id="8abb6-238">The **SeLoadDriverPrivilege** privilege is required to delete an instance of this WMI class.</span></span> <span data-ttu-id="8abb6-239">L’extrait de script suivant montre comment établir une connexion à WMI qui utilise ce privilège.</span><span class="sxs-lookup"><span data-stu-id="8abb6-239">The following script snippet demonstrates how to make a connection to WMI that uses this privilege.</span></span>

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a><span data-ttu-id="8abb6-240">Exemples</span><span class="sxs-lookup"><span data-stu-id="8abb6-240">Examples</span></span>

<span data-ttu-id="8abb6-241">L’exemple PowerShell suivant supprime une imprimante et le port d’imprimante TCP/IP associé.</span><span class="sxs-lookup"><span data-stu-id="8abb6-241">The following PowerShell sample removes a printer and the associated TCPIP printer port.</span></span>


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a><span data-ttu-id="8abb6-242">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8abb6-242">Requirements</span></span>



| <span data-ttu-id="8abb6-243">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8abb6-243">Requirement</span></span> | <span data-ttu-id="8abb6-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="8abb6-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abb6-245">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8abb6-245">Minimum supported client</span></span><br/> | <span data-ttu-id="8abb6-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8abb6-246">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8abb6-247">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8abb6-247">Minimum supported server</span></span><br/> | <span data-ttu-id="8abb6-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8abb6-248">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8abb6-249">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8abb6-249">Namespace</span></span><br/>                | <span data-ttu-id="8abb6-250">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8abb6-250">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="8abb6-251">MOF</span><span class="sxs-lookup"><span data-stu-id="8abb6-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8abb6-252"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8abb6-252"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="8abb6-253">DLL</span><span class="sxs-lookup"><span data-stu-id="8abb6-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8abb6-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8abb6-254"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8abb6-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8abb6-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8abb6-256">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="8abb6-256">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dt>

[<span data-ttu-id="8abb6-257">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="8abb6-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
