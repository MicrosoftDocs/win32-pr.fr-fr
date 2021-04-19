---
description: La classe SnmpExtendedNotification est la classe de base pour toute classe mappée à partir de la macro de TYPE NOTIFICATION à une classe CIM par le fournisseur SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524568"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="3d3d3-103">SnmpExtendedNotification, classe</span><span class="sxs-lookup"><span data-stu-id="3d3d3-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="3d3d3-104">La classe **SnmpExtendedNotification** est la classe de base pour toute classe mappée à partir de la macro de [type notification](notification-type-macro.md) à une classe CIM par le [fournisseur SNMP](snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="3d3d3-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="3d3d3-106">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d3d3-107">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d3d3-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="3d3d3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3d3d3-109">Members</span></span>

<span data-ttu-id="3d3d3-110">La classe **SnmpExtendedNotification** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3d3d3-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="3d3d3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d3d3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d3d3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3d3d3-112">Properties</span></span>

<span data-ttu-id="3d3d3-113">La classe **SnmpExtendedNotification** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d3d3-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-117">Adresse réseau de l’entité qui a créé la notification.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="3d3d3-118">Il s’agit de l’adresse réelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-118">This is the actual address of the device.</span></span> <span data-ttu-id="3d3d3-119">Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="3d3d3-120">Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="3d3d3-121">Cette propriété est valide uniquement pour SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-122">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-125">Protocole de transport utilisé par l’entité émettrice.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="3d3d3-126">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-127">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-130">Adresse réseau de l’entité qui a envoyé la notification.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="3d3d3-131">Il s’agit de l’adresse de la dernière entité qui a transféré la notification.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="3d3d3-132">Lorsque l’entité de gestion utilise SNMP sur UDP, l’adresse de transport fait référence à une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="3d3d3-133">Lorsque l’entité de gestion utilise SNMP sur IPX, l’adresse de transport fait référence à une adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="3d3d3-134">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-135">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-138">Protocole de transport utilisé par l’entité émettrice.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-139">**Communauté**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-142">Nom de communauté associé à une instance de la PDU.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="3d3d3-143">Le nom de la communauté authentifie l’expéditeur de l’PDU.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="3d3d3-144">Cette propriété est valide pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-145">**Identification**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-148">Qualificateurs : **\_ Convention textuelle** (« OBJECTIDENTIFIER »), **encodage** (« OBJECTIDENTIFIER ») **, \_ syntaxe d’objet** (« OBJECTIDENTIFIER »), **\_ identificateur d’objet** (« 1.3.6.1.6.3.1.1.4.1 »)</span><span class="sxs-lookup"><span data-stu-id="3d3d3-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-149">Identification faisant autorité de cette notification.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="3d3d3-150">Mappe directement à l’entrée MIB liaison de variable SnmpTrapOID.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="3d3d3-151">Cette propriété est valide uniquement pour SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-152">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-153">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-155">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="3d3d3-156">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="3d3d3-157">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-158">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-159">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-161">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="3d3d3-162">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="3d3d3-163">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="3d3d3-164">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="3d3d3-165">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3d3d3-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3d3d3-166">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d3d3-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d3d3-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d3d3-169">Qualificateurs : **\_ Convention textuelle** (« graduations »), **encodage** (« graduations ») **, \_ syntaxe d’objet** (« graduations »), **\_ identificateur d’objet** (« 1.3.6.1.2.1.1.3 »)</span><span class="sxs-lookup"><span data-stu-id="3d3d3-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="3d3d3-170">Durée en centièmes de seconde depuis la dernière réinitialisation de la partie gestion du réseau de l’agent.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="3d3d3-171">Correspond à la variable MIB sysUptime. 0, qui est de type **INTEGER32**.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="3d3d3-172">Cette propriété est mappée à l' **horodateur** de propriété de la classe CIM, qui est de type **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="3d3d3-173">Cette propriété est valide uniquement pour SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d3d3-174">Notes</span><span class="sxs-lookup"><span data-stu-id="3d3d3-174">Remarks</span></span>

<span data-ttu-id="3d3d3-175">Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **timestamp** ou **identification** provoque un conflit de mappage.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="3d3d3-176">Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="3d3d3-177">Une macro de [type notification](notification-type-macro.md) qui contient des références à une macro de [type objet](object-type-macro.md) nommée **Community** provoque un conflit de mappage.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="3d3d3-178">Si ce conflit se produit, les propriétés requises sont prioritaires et les références en conflit doivent être renommées.</span><span class="sxs-lookup"><span data-stu-id="3d3d3-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3d3-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d3d3-179">Requirements</span></span>



| <span data-ttu-id="3d3d3-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d3d3-180">Requirement</span></span> | <span data-ttu-id="3d3d3-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d3d3-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3d3-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d3d3-182">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3d3-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d3d3-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d3d3-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d3d3-184">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3d3-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d3d3-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d3d3-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3d3d3-186">Namespace</span></span><br/>                | <span data-ttu-id="3d3d3-187">\\Stockage SMIR SNMP \\ racine</span><span class="sxs-lookup"><span data-stu-id="3d3d3-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="3d3d3-188">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3d3-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3d3-189"><dt>SnmpSmiR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d3d3-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3d3-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d3d3-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3d3-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="3d3d3-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="3d3d3-192">Macro de TYPE NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3d3d3-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

