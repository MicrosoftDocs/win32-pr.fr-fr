---
description: Représente une entrée dans la base de données de transfert associée à la \_ classe CIM TransparentBridgingService.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Classe CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524497"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="fa658-103">\_Classe CIM DynamicForwardingEntry</span><span class="sxs-lookup"><span data-stu-id="fa658-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="fa658-104">Représente une entrée dans la base de données de transfert associée à la classe [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fa658-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa658-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa658-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="fa658-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fa658-106">Members</span></span>

<span data-ttu-id="fa658-107">La classe **CIM \_ DynamicForwardingEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fa658-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="fa658-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa658-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa658-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa658-109">Properties</span></span>

<span data-ttu-id="fa658-110">La classe **CIM \_ DynamicForwardingEntry** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa658-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa658-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa658-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-114">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fa658-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fa658-115">Nom de la classe ou de la sous-classe utilisée pour créer l’instance.</span><span class="sxs-lookup"><span data-stu-id="fa658-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="fa658-116">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="fa658-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="fa658-117">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="fa658-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa658-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-120">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="fa658-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-121">État de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="fa658-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa658-122">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fa658-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="fa658-123">**Non valide** (2)</span><span class="sxs-lookup"><span data-stu-id="fa658-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="fa658-124">**Appris** (3)</span><span class="sxs-lookup"><span data-stu-id="fa658-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="fa658-125">**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="fa658-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="fa658-126">**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="fa658-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa658-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="fa658-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-130">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="fa658-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-131">Adresse MAC de monodiffusion pour laquelle le service de pontage filtre les informations.</span><span class="sxs-lookup"><span data-stu-id="fa658-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="fa658-132">L’adresse MAC est mise en forme en tant que 12 chiffres hexadécimaux, par exemple 010203040506, chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques, conformément à la RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="fa658-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="fa658-133">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa658-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-136">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ service CIM**](cim-service.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="fa658-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-137">Valeur **CreationClassName** de l’objet de service d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fa658-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="fa658-138">**FormName**</span><span class="sxs-lookup"><span data-stu-id="fa658-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-141">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ service CIM**](cim-service.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="fa658-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-142">Nom du service d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fa658-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="fa658-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa658-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-146">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="fa658-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-147">Valeur **CreationClassName** de l’objet système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fa658-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="fa658-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fa658-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa658-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa658-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa658-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa658-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa658-151">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="fa658-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="fa658-152">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fa658-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa658-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa658-153">Requirements</span></span>



| <span data-ttu-id="fa658-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa658-154">Requirement</span></span> | <span data-ttu-id="fa658-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa658-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa658-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa658-156">Minimum supported client</span></span><br/> | <span data-ttu-id="fa658-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fa658-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fa658-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa658-158">Minimum supported server</span></span><br/> | <span data-ttu-id="fa658-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa658-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fa658-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa658-160">Namespace</span></span><br/>                | <span data-ttu-id="fa658-161">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa658-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fa658-162">MOF</span><span class="sxs-lookup"><span data-stu-id="fa658-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa658-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa658-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa658-164">DLL</span><span class="sxs-lookup"><span data-stu-id="fa658-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa658-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa658-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa658-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa658-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa658-167">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fa658-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

