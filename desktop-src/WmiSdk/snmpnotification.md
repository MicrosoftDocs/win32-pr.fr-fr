---
description: La classe SnmpNotification mappe la macro de TYPE NOTIFICATION à une classe CIM encapsulée.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: SnmpNotification, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530208"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="8d417-103">SnmpNotification, classe</span><span class="sxs-lookup"><span data-stu-id="8d417-103">SnmpNotification class</span></span>

<span data-ttu-id="8d417-104">La classe **SnmpNotification** mappe la macro de [type notification](notification-type-macro.md) à une classe CIM encapsulée.</span><span class="sxs-lookup"><span data-stu-id="8d417-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="8d417-105">Il s’agit d’une classe de base utilisée par le [fournisseur SNMP](snmp-provider.md) pour toute classe mappée à partir de la macro de [type notification](notification-type-macro.md) à une classe CIM encapsulée par le fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="8d417-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="8d417-106">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8d417-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8d417-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d417-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="8d417-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8d417-108">Members</span></span>

<span data-ttu-id="8d417-109">La classe **SnmpNotification** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d417-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="8d417-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d417-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d417-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d417-111">Properties</span></span>

<span data-ttu-id="8d417-112">La classe **SnmpNotification** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8d417-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d417-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="8d417-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-116">Adresse réseau de l’entité qui a créé la notification.</span><span class="sxs-lookup"><span data-stu-id="8d417-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="8d417-117">Il s’agit de l’adresse réelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8d417-117">This is the actual address of the device.</span></span> <span data-ttu-id="8d417-118">Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8d417-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="8d417-119">Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="8d417-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="8d417-120">Cette propriété est valide uniquement pour SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="8d417-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-121">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="8d417-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-124">Protocole de transport utilisé par l’entité émettrice.</span><span class="sxs-lookup"><span data-stu-id="8d417-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="8d417-125">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8d417-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-126">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="8d417-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-129">Adresse réseau de l’entité qui a envoyé la notification.</span><span class="sxs-lookup"><span data-stu-id="8d417-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="8d417-130">Il s’agit de l’adresse de la dernière entité qui a transféré la notification.</span><span class="sxs-lookup"><span data-stu-id="8d417-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="8d417-131">Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="8d417-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="8d417-132">Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport fait référence à une adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="8d417-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="8d417-133">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8d417-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-134">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="8d417-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-137">Protocole de transport utilisé par l’entité émettrice.</span><span class="sxs-lookup"><span data-stu-id="8d417-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-138">**Communauté**</span><span class="sxs-lookup"><span data-stu-id="8d417-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-141">Nom de communauté associé à une instance de la PDU.</span><span class="sxs-lookup"><span data-stu-id="8d417-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="8d417-142">Le nom de la communauté authentifie l’expéditeur de l’PDU.</span><span class="sxs-lookup"><span data-stu-id="8d417-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="8d417-143">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8d417-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-144">**Identification**</span><span class="sxs-lookup"><span data-stu-id="8d417-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d417-147">Qualificateurs : **\_ Convention textuelle** (« OBJECTIDENTIFIER »), **encodage** (« OBJECTIDENTIFIER ») **, \_ syntaxe d’objet** (« OBJECTIDENTIFIER »), **\_ identificateur d’objet** (« 1.3.6.1.6.3.1.1.4.1 »)</span><span class="sxs-lookup"><span data-stu-id="8d417-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="8d417-148">Identification faisant autorité de cette notification.</span><span class="sxs-lookup"><span data-stu-id="8d417-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="8d417-149">Mappe directement à la liaison de variable SnmpTrapOID.</span><span class="sxs-lookup"><span data-stu-id="8d417-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="8d417-150">Cette propriété est valide uniquement pour SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8d417-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="8d417-151">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="8d417-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-152">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8d417-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8d417-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-154">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="8d417-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8d417-155">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8d417-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="8d417-156">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8d417-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d417-157">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="8d417-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-158">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d417-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d417-160">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="8d417-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8d417-161">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="8d417-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8d417-162">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="8d417-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="8d417-163">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8d417-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8d417-164">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8d417-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8d417-165">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="8d417-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d417-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d417-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d417-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d417-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d417-168">Qualificateurs : **\_ Convention textuelle** (« graduations »), **encodage** (« graduations ») **, \_ syntaxe d’objet** (« graduations »), **\_ identificateur d’objet** (« 1.3.6.1.2.1.1.3 »)</span><span class="sxs-lookup"><span data-stu-id="8d417-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="8d417-169">Durée en centièmes de seconde depuis la dernière réinitialisation de la partie gestion du réseau de l’agent.</span><span class="sxs-lookup"><span data-stu-id="8d417-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="8d417-170">Variable MIB sysUptime. 0, qui est de type **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="8d417-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="8d417-171">Cette propriété est mappée à l' **horodateur** de propriété de la classe CIM, qui est de type **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="8d417-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="8d417-172">Cette propriété est valide uniquement pour SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8d417-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d417-173">Notes</span><span class="sxs-lookup"><span data-stu-id="8d417-173">Remarks</span></span>

<span data-ttu-id="8d417-174">Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **timestamp** ou **identification** provoque un conflit de mappage.</span><span class="sxs-lookup"><span data-stu-id="8d417-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="8d417-175">Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.</span><span class="sxs-lookup"><span data-stu-id="8d417-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="8d417-176">Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **Community** provoque un conflit de mappage.</span><span class="sxs-lookup"><span data-stu-id="8d417-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="8d417-177">Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.</span><span class="sxs-lookup"><span data-stu-id="8d417-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d417-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d417-178">Requirements</span></span>



| <span data-ttu-id="8d417-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d417-179">Requirement</span></span> | <span data-ttu-id="8d417-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d417-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="8d417-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d417-181">Minimum supported client</span></span><br/> | <span data-ttu-id="8d417-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d417-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="8d417-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d417-183">Minimum supported server</span></span><br/> | <span data-ttu-id="8d417-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d417-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="8d417-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d417-185">Namespace</span></span><br/>                | <span data-ttu-id="8d417-186">\\Hôte SNMP \\ racine</span><span class="sxs-lookup"><span data-stu-id="8d417-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d417-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d417-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d417-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="8d417-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="8d417-189">Macro de TYPE NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8d417-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

