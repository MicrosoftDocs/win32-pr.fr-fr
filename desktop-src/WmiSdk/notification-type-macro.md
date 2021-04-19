---
description: La macro de TYPE NOTIFICATION contient les éléments suivants.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro de TYPE NOTIFICATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529713"
---
# <a name="notification-type-macro"></a><span data-ttu-id="35f20-103">Macro de TYPE NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="35f20-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="35f20-104">La macro de TYPE NOTIFICATION contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="35f20-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="35f20-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="35f20-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="35f20-106">Composants</span><span class="sxs-lookup"><span data-stu-id="35f20-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="35f20-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descripteur d’objet</span><span class="sxs-lookup"><span data-stu-id="35f20-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="35f20-108">Joint un nom à un événement SNMP dans une macro de TYPE NOTIFICATION.</span><span class="sxs-lookup"><span data-stu-id="35f20-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="35f20-109">La liste suivante répertorie les règles de mappage du descripteur d’objet.</span><span class="sxs-lookup"><span data-stu-id="35f20-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="35f20-110">Type</span><span class="sxs-lookup"><span data-stu-id="35f20-110">Type</span></span>                        | <span data-ttu-id="35f20-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="35f20-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35f20-112">Nom de classe CIM encapsulé</span><span class="sxs-lookup"><span data-stu-id="35f20-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="35f20-113">« SNMP \_ »</span><span class="sxs-lookup"><span data-stu-id="35f20-113">"SNMP\_"</span></span><br/> <span data-ttu-id="35f20-114">Nom de l’identité du module MIB</span><span class="sxs-lookup"><span data-stu-id="35f20-114">MIB module identity name</span></span><br/> <span data-ttu-id="35f20-115">trait de soulignement ( \_ )</span><span class="sxs-lookup"><span data-stu-id="35f20-115">underscore (\_)</span></span><br/> <span data-ttu-id="35f20-116">descripteur d’objet</span><span class="sxs-lookup"><span data-stu-id="35f20-116">object descriptor</span></span><br/> <span data-ttu-id="35f20-117">« \_ Notification »</span><span class="sxs-lookup"><span data-stu-id="35f20-117">"\_Notification"</span></span><br/> <span data-ttu-id="35f20-118">Exemple : la notification **vtpServerDisabled** de **Cisco-VTP-MIB** est mappée à la **\_ notification SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.</span><span class="sxs-lookup"><span data-stu-id="35f20-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="35f20-119">Nom de la classe CIM référent</span><span class="sxs-lookup"><span data-stu-id="35f20-119">Referent CIM class name</span></span>     | <span data-ttu-id="35f20-120">« SNMP \_ »</span><span class="sxs-lookup"><span data-stu-id="35f20-120">"SNMP\_"</span></span><br/> <span data-ttu-id="35f20-121">Nom de l’identité du module MIB</span><span class="sxs-lookup"><span data-stu-id="35f20-121">MIB module identity name</span></span><br/> <span data-ttu-id="35f20-122">trait de soulignement ( \_ )</span><span class="sxs-lookup"><span data-stu-id="35f20-122">underscore (\_)</span></span><br/> <span data-ttu-id="35f20-123">descripteur d’objet</span><span class="sxs-lookup"><span data-stu-id="35f20-123">object descriptor</span></span><br/> <span data-ttu-id="35f20-124">« \_ ExtendedNotification »</span><span class="sxs-lookup"><span data-stu-id="35f20-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="35f20-125">Exemple : la notification **vtpServerDisabled** de **Cisco-VTP-MIB** est mappée à la valeur **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.</span><span class="sxs-lookup"><span data-stu-id="35f20-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="35f20-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Clause OBJECTs</span><span class="sxs-lookup"><span data-stu-id="35f20-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="35f20-127">Énumère le jeu d’objets associés à l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="35f20-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="35f20-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>RÉFÉRENCE (clause)</span><span class="sxs-lookup"><span data-stu-id="35f20-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="35f20-129">Fait référence à un autre document qui contient plus d’informations sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="35f20-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="35f20-130">Elle est mappée à la **référence** de qualificateur de classe CIM, qui est de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="35f20-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="35f20-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION (clause)</span><span class="sxs-lookup"><span data-stu-id="35f20-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="35f20-132">Décrit l’objet en question.</span><span class="sxs-lookup"><span data-stu-id="35f20-132">Describes the object in question.</span></span> <span data-ttu-id="35f20-133">Il correspond à la **Description** de qualificateur de classe CIM, qui est de type chaîne</span><span class="sxs-lookup"><span data-stu-id="35f20-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="35f20-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clause STATUs</span><span class="sxs-lookup"><span data-stu-id="35f20-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="35f20-135">Indique si l’objet doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35f20-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="35f20-136">Lorsque l’État est **obsolète** ou **déconseillé**, la notification est ignorée du mappage.</span><span class="sxs-lookup"><span data-stu-id="35f20-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="35f20-137">Sinon, cette clause correspond à l' **État** du qualificateur de la classe CIM, qui est de type **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="35f20-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="35f20-138">Pour SNMPv1, la valeur par défaut de l' **État** est **obligatoire** ou **facultative**, mais le qualificateur peut contenir une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="35f20-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="35f20-139">Pour SNMPv2C, la valeur par défaut de l' **État** est **en cours** ou **déconseillée**, mais le qualificateur peut contenir une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="35f20-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35f20-140">Notes</span><span class="sxs-lookup"><span data-stu-id="35f20-140">Remarks</span></span>

<span data-ttu-id="35f20-141">Le fournisseur SNMP mappe la macro de **type notification** à une définition de classe encapsulée ou référent.</span><span class="sxs-lookup"><span data-stu-id="35f20-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="35f20-142">Une définition de classe encapsulée n’expose pas les informations d’instance associées à l’objet MIB.</span><span class="sxs-lookup"><span data-stu-id="35f20-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="35f20-143">Au lieu de cela, la définition de classe encode la clause OBJECTs sous la forme d’une série de propriétés de la classe d’événements CIM.</span><span class="sxs-lookup"><span data-stu-id="35f20-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="35f20-144">Chaque propriété CIM reflète le nom, le type et la valeur de l’objet MIB correspondant dans la clause OBJECTs.</span><span class="sxs-lookup"><span data-stu-id="35f20-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="35f20-145">Si vous avez besoin d’informations d’instance, vous devez mapper à une classe référent.</span><span class="sxs-lookup"><span data-stu-id="35f20-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="35f20-146">Une définition de classe encapsulée est mappée à la classe [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="35f20-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="35f20-147">Une classe référent définit un objet MIB et les informations d’instance utilisées pour obtenir l’objet.</span><span class="sxs-lookup"><span data-stu-id="35f20-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="35f20-148">La définition de classe encode la clause OBJECTs sous la forme d’une série de propriétés de la classe d’événements CIM.</span><span class="sxs-lookup"><span data-stu-id="35f20-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="35f20-149">Chaque propriété CIM reflète le nom de l’objet MIB correspondant dans la clause OBJECTs et le type en tant qu’objet incorporé qui reflète une instance de la classe associée à cet objet MIB.</span><span class="sxs-lookup"><span data-stu-id="35f20-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="35f20-150">Le fournisseur génère ensuite une classe associée à l’objet MIB.</span><span class="sxs-lookup"><span data-stu-id="35f20-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="35f20-151">Par exemple, **ifIndex** est mappé à une classe incorporée nommée **SNMP \_ RFC1213 \_ MIB \_ ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="35f20-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="35f20-152">Pour plus d’informations sur ce type de classe, consultez [macro de type objet](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="35f20-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




