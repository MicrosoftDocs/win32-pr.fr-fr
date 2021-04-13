---
description: Le \_ NetworkProtocol Win32&\# 8194 ; La classe WMI représente un protocole et ses caractéristiques réseau sur un système informatique Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483792"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="be95d-103">\_Classe NetworkProtocol Win32</span><span class="sxs-lookup"><span data-stu-id="be95d-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="be95d-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkProtocol** représente un protocole et ses caractéristiques réseau sur un système informatique Win32.</span><span class="sxs-lookup"><span data-stu-id="be95d-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="be95d-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be95d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="be95d-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="be95d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be95d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be95d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="be95d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="be95d-108">Members</span></span>

<span data-ttu-id="be95d-109">La classe **Win32 \_ NetworkProtocol** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be95d-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="be95d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be95d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be95d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be95d-111">Properties</span></span>

<span data-ttu-id="be95d-112">La classe **Win32 \_ NetworkProtocol** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="be95d-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be95d-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="be95d-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be95d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="be95d-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be95d-117">A short textual description of the object.</span></span>

<span data-ttu-id="be95d-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be95d-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be95d-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="be95d-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-122">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP1 \_ sans connexion »)</span><span class="sxs-lookup"><span data-stu-id="be95d-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-123">Le protocole prend en charge le service sans connexion.</span><span class="sxs-lookup"><span data-stu-id="be95d-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="be95d-124">Un service sans connexion (datagramme) décrit un protocole de communication ou un transport dans lequel les paquets de données sont acheminés indépendamment les uns des autres et peuvent suivre différents itinéraires et arriver dans un ordre différent de celui dans lequel ils ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="be95d-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="be95d-125">À l’inverse, un service orienté connexion fournit un circuit virtuel par le biais duquel les paquets de données sont reçus dans l’ordre dans lequel ils ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="be95d-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="be95d-126">Si la connexion entre les ordinateurs échoue, l’application est avertie.</span><span class="sxs-lookup"><span data-stu-id="be95d-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="be95d-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be95d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-130">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="be95d-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-131">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be95d-131">A textual description of the object.</span></span>

<span data-ttu-id="be95d-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be95d-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be95d-133">**GuaranteesDelivery**</span><span class="sxs-lookup"><span data-stu-id="be95d-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-136">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ garanti \_ Delivery »)</span><span class="sxs-lookup"><span data-stu-id="be95d-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-137">Le protocole prend en charge la remise des paquets de données.</span><span class="sxs-lookup"><span data-stu-id="be95d-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="be95d-138">Si cet indicateur a la **valeur false**, il est incertain que toutes les données envoyées atteindront la destination prévue.</span><span class="sxs-lookup"><span data-stu-id="be95d-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-139">**GuaranteesSequencing**</span><span class="sxs-lookup"><span data-stu-id="be95d-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-142">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ \_ ordre garanti »)</span><span class="sxs-lookup"><span data-stu-id="be95d-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-143">Le protocole permet de s’assurer que les données arrivent dans l’ordre dans lequel elles ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="be95d-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="be95d-144">N’oubliez pas que cette caractéristique ne garantit pas la distribution des données, mais uniquement leur ordre.</span><span class="sxs-lookup"><span data-stu-id="be95d-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be95d-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be95d-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-148">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="be95d-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-149">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="be95d-149">Indicates when the object was installed.</span></span> <span data-ttu-id="be95d-150">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="be95d-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="be95d-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be95d-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be95d-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="be95d-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be95d-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-155">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| iMaxSockAddr »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)</span><span class="sxs-lookup"><span data-stu-id="be95d-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-156">Longueur maximale d’une adresse de socket prise en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="be95d-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="be95d-157">Les adresses de socket peuvent être des éléments tels qu’une URL ( `www.microsoft.com` ) ou une adresse IP ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="be95d-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="be95d-158">**MaximumMessageSize**</span><span class="sxs-lookup"><span data-stu-id="be95d-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be95d-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-161">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwMessageSize »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)</span><span class="sxs-lookup"><span data-stu-id="be95d-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-162">Taille maximale des messages prise en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="be95d-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="be95d-163">Il s’agit de la taille maximale d’un message qui peut être envoyé ou reçu par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="be95d-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="be95d-164">Pour les protocoles qui ne prennent pas en charge le tramage de message, la taille maximale réelle d’un message qui peut être envoyé à une adresse donnée peut être inférieure à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="be95d-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-165">**MessageOriented**</span><span class="sxs-lookup"><span data-stu-id="be95d-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-166">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-168">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ \_ orienté message »)</span><span class="sxs-lookup"><span data-stu-id="be95d-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-169">Le protocole est orienté message.</span><span class="sxs-lookup"><span data-stu-id="be95d-169">Protocol is message-oriented.</span></span> <span data-ttu-id="be95d-170">Un protocole orienté message utilise des paquets de données pour transférer des informations.</span><span class="sxs-lookup"><span data-stu-id="be95d-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="be95d-171">À l’inverse, les protocoles orientés flux transfèrent les données sous la forme d’un flux continu d’octets.</span><span class="sxs-lookup"><span data-stu-id="be95d-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="be95d-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-173">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be95d-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-175">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| iMinSockAddr »), [**unités**](../wmisdk/standard-qualifiers.md) (« caractères »)</span><span class="sxs-lookup"><span data-stu-id="be95d-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-176">Longueur minimale d’une adresse de socket prise en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="be95d-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-177">**Nom**</span><span class="sxs-lookup"><span data-stu-id="be95d-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be95d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-180">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| lpProtocol")</span><span class="sxs-lookup"><span data-stu-id="be95d-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-181">Nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="be95d-181">Name for the protocol.</span></span>

<span data-ttu-id="be95d-182">Exemple : « TCP/IP »</span><span class="sxs-lookup"><span data-stu-id="be95d-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="be95d-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="be95d-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-186">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ Pseudo \_ Stream »)</span><span class="sxs-lookup"><span data-stu-id="be95d-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-187">Le protocole est un protocole orienté message qui peut recevoir des paquets de données de longueur variable ou des données diffusées en continu pour toutes les opérations de réception.</span><span class="sxs-lookup"><span data-stu-id="be95d-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="be95d-188">Cette capacité facultative est utile lorsqu’une application ne souhaite pas que le protocole trame des messages et nécessite des caractéristiques orientées flux.</span><span class="sxs-lookup"><span data-stu-id="be95d-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="be95d-189">Si la **valeur est true**, le protocole est Pseudo-orienté en flux continu.</span><span class="sxs-lookup"><span data-stu-id="be95d-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-190">**État**</span><span class="sxs-lookup"><span data-stu-id="be95d-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be95d-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-193">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="be95d-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-194">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be95d-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="be95d-195">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="be95d-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="be95d-196">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="be95d-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="be95d-197">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="be95d-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="be95d-198">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="be95d-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="be95d-199">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="be95d-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="be95d-200">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="be95d-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="be95d-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be95d-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="be95d-202">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="be95d-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="be95d-203">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="be95d-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="be95d-204">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="be95d-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="be95d-205">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="be95d-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="be95d-206">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="be95d-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="be95d-207">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="be95d-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="be95d-208">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="be95d-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="be95d-209">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="be95d-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="be95d-210">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="be95d-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="be95d-211">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="be95d-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="be95d-212">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="be95d-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="be95d-213">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="be95d-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="be95d-214">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="be95d-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="be95d-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="be95d-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-218">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ prend en charge la \_ diffusion »)</span><span class="sxs-lookup"><span data-stu-id="be95d-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-219">Le protocole prend en charge un mécanisme de diffusion des messages sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="be95d-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-221">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-223">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ Connect \_ Data »)</span><span class="sxs-lookup"><span data-stu-id="be95d-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-224">Le protocole autorise la connexion des données sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="be95d-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-226">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-228">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ déconnecte les \_ données »)</span><span class="sxs-lookup"><span data-stu-id="be95d-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-229">Le protocole autorise la déconnexion des données sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="be95d-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-233">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ chiffre »)</span><span class="sxs-lookup"><span data-stu-id="be95d-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-234">Le protocole prend en charge le chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="be95d-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-235">**SupportsExpeditedData**</span><span class="sxs-lookup"><span data-stu-id="be95d-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-236">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-238">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ Expedited \_ Data »)</span><span class="sxs-lookup"><span data-stu-id="be95d-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-239">Le protocole prend en charge les données expédiées (également appelées données urgentes) sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="be95d-240">Les données expédiées peuvent contourner le contrôle de Flow et recevoir la priorité sur les paquets de données normaux.</span><span class="sxs-lookup"><span data-stu-id="be95d-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-241">**SupportsFragmentation**</span><span class="sxs-lookup"><span data-stu-id="be95d-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-242">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-244">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| Protocol \_ info \| dwServiceFlags \| XP \_ fragmentation »)</span><span class="sxs-lookup"><span data-stu-id="be95d-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-245">Le protocole prend en charge la transmission des données par fragments.</span><span class="sxs-lookup"><span data-stu-id="be95d-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="be95d-246">L’unité de transfert maximale (MTU) du réseau physique est masquée dans les applications.</span><span class="sxs-lookup"><span data-stu-id="be95d-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="be95d-247">Chaque type de média a une taille de trame maximale qui ne peut pas être dépassée.</span><span class="sxs-lookup"><span data-stu-id="be95d-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="be95d-248">La couche de liaison Découvre la MTU et la signale aux protocoles utilisés.</span><span class="sxs-lookup"><span data-stu-id="be95d-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="be95d-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-250">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-252">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ normal \_ Close »)</span><span class="sxs-lookup"><span data-stu-id="be95d-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-253">Le protocole prend en charge les opérations de fermeture en deux phases, également appelées « opérations de fermeture gracieuse ».</span><span class="sxs-lookup"><span data-stu-id="be95d-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="be95d-254">Si ce n’est pas le cas, le protocole prend en charge uniquement les opérations de fermeture abandonnées.</span><span class="sxs-lookup"><span data-stu-id="be95d-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-255">**SupportsGuaranteedBandwidth**</span><span class="sxs-lookup"><span data-stu-id="be95d-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-256">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-258">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ allocation de bande passante \_ »)</span><span class="sxs-lookup"><span data-stu-id="be95d-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-259">Le protocole a un mécanisme permettant d’établir et de maintenir une bande passante.</span><span class="sxs-lookup"><span data-stu-id="be95d-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="be95d-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-261">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-263">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| protocole \_ info \| dwServiceFlags \| XP \_ prend en charge la \_ multidiffusion »)</span><span class="sxs-lookup"><span data-stu-id="be95d-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-264">Le protocole prend en charge la multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="be95d-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="be95d-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="be95d-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be95d-266">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be95d-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be95d-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be95d-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be95d-268">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32 \_ API \| Windows Sockets structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ pris en charge »)</span><span class="sxs-lookup"><span data-stu-id="be95d-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="be95d-269">Le protocole peut prendre en charge la qualité de service (QoS) par le fournisseur de services en couche sous-jacent ou le transporteur de transport.</span><span class="sxs-lookup"><span data-stu-id="be95d-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="be95d-270">La qualité de service (QoS) est un ensemble de composants qui activent la différenciation et le traitement préférentiel pour les sous-ensembles de données transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="be95d-271">La qualité de service (QoS) signifie que les sous-ensembles de données obtiennent une priorité plus élevée ou un service garanti lors du parcours d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="be95d-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be95d-272">Notes</span><span class="sxs-lookup"><span data-stu-id="be95d-272">Remarks</span></span>

<span data-ttu-id="be95d-273">La classe **Win32 \_ NetworkProtocol** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="be95d-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="be95d-274">Exemples</span><span class="sxs-lookup"><span data-stu-id="be95d-274">Examples</span></span>

<span data-ttu-id="be95d-275">L’exemple de code VBScript suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances de **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="be95d-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="be95d-276">L’exemple de code perl suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances de **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="be95d-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="be95d-277">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be95d-277">Requirements</span></span>



| <span data-ttu-id="be95d-278">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be95d-278">Requirement</span></span> | <span data-ttu-id="be95d-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="be95d-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be95d-280">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be95d-280">Minimum supported client</span></span><br/> | <span data-ttu-id="be95d-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be95d-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be95d-282">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be95d-282">Minimum supported server</span></span><br/> | <span data-ttu-id="be95d-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be95d-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be95d-284">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be95d-284">Namespace</span></span><br/>                | <span data-ttu-id="be95d-285">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="be95d-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be95d-286">MOF</span><span class="sxs-lookup"><span data-stu-id="be95d-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be95d-287"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be95d-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be95d-288">DLL</span><span class="sxs-lookup"><span data-stu-id="be95d-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be95d-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be95d-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be95d-290">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be95d-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be95d-291">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="be95d-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="be95d-292">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="be95d-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
