---
description: Définit une connexion actuellement activée et configurée pour fournir une communication entre deux \_ objets SERVICEACCESSPOINT CIM.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529717"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="11f77-103">\_Classe ACTIVECONNECTION CIM</span><span class="sxs-lookup"><span data-stu-id="11f77-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="11f77-104">Définit une connexion actuellement activée et configurée pour fournir une communication entre deux objets **\_ ServiceAccessPoint CIM** .</span><span class="sxs-lookup"><span data-stu-id="11f77-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="11f77-105">**CIM \_ ActiveConnection** est utilisé lorsque la connexion n’est pas traitée comme un objet **CIM \_ propriété ManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="11f77-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="11f77-106">Les points d’accès de service qui sont connectés par une connexion active sont généralement au même niveau réseau ou couche application.</span><span class="sxs-lookup"><span data-stu-id="11f77-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f77-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11f77-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="11f77-108">Membres</span><span class="sxs-lookup"><span data-stu-id="11f77-108">Members</span></span>

<span data-ttu-id="11f77-109">La classe **CIM \_ ActiveConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="11f77-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="11f77-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11f77-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11f77-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11f77-111">Properties</span></span>

<span data-ttu-id="11f77-112">La classe **CIM \_ ActiveConnection** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="11f77-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11f77-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="11f77-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f77-114">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="11f77-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="11f77-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11f77-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f77-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="11f77-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="11f77-117">Point d’accès au service connecté à l’autre point d’accès de service via la connexion active.</span><span class="sxs-lookup"><span data-stu-id="11f77-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="11f77-118">**CIM \_ Objet ServiceAccessPoint** .</span><span class="sxs-lookup"><span data-stu-id="11f77-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="11f77-119">Dans une connexion unidirectionnelle, ce point d’accès est celui qui transmet les données.</span><span class="sxs-lookup"><span data-stu-id="11f77-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="11f77-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="11f77-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f77-121">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="11f77-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="11f77-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11f77-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f77-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="11f77-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="11f77-124">Point d’accès au service qui est configuré pour communiquer ou qui communique activement avec le point d’accès au service spécifié dans la propriété **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="11f77-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="11f77-125">Dans une connexion unidirectionnelle, ce point d’accès est celui qui reçoit des données.</span><span class="sxs-lookup"><span data-stu-id="11f77-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="11f77-126">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="11f77-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f77-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="11f77-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11f77-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11f77-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11f77-129">True si la connexion est unidirectionnelle ; false si la connexion est bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="11f77-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="11f77-130">Lorsque la connexion est unidirectionnelle, la propriété **Antecedent** spécifie le point d’accès qui transmet les données.</span><span class="sxs-lookup"><span data-stu-id="11f77-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="11f77-131">Dans une connexion bidirectionnelle, l' **antécédent** peut spécifier un point d’accès affecté à la connexion.</span><span class="sxs-lookup"><span data-stu-id="11f77-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="11f77-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="11f77-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f77-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11f77-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f77-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11f77-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f77-135">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIM \_ ActiveConnection**.**TrafficType**")</span><span class="sxs-lookup"><span data-stu-id="11f77-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="11f77-136">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="11f77-136">This property is deprecated.</span></span> <span data-ttu-id="11f77-137">Au lieu de cela, nous vous recommandons de spécifier ces informations dans l’adressage, le protocole et les fonctionnalités de base des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="11f77-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="11f77-138">Description du type de trafic qui est spécifié lorsque la propriété **TrafficType** est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="11f77-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="11f77-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="11f77-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f77-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11f77-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11f77-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11f77-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f77-142">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIM \_ ActiveConnection**.**OtherTrafficDescription**")</span><span class="sxs-lookup"><span data-stu-id="11f77-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="11f77-143">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="11f77-143">This property is deprecated.</span></span> <span data-ttu-id="11f77-144">Au lieu de cela, nous vous recommandons de spécifier ces informations dans l’adressage, le protocole et les fonctionnalités de base des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="11f77-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="11f77-145">Type de trafic transmis sur cette connexion.</span><span class="sxs-lookup"><span data-stu-id="11f77-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11f77-146">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="11f77-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11f77-147">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="11f77-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="11f77-148">**Monodiffusion** (2)</span><span class="sxs-lookup"><span data-stu-id="11f77-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="11f77-149">**Diffusion** (3)</span><span class="sxs-lookup"><span data-stu-id="11f77-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="11f77-150">**Multidiffusion** (4)</span><span class="sxs-lookup"><span data-stu-id="11f77-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="11f77-151">**Anycast** (5)</span><span class="sxs-lookup"><span data-stu-id="11f77-151">**Anycast** (5)</span></span>


<span data-ttu-id="11f77-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="11f77-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="11f77-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11f77-153">Requirements</span></span>



| <span data-ttu-id="11f77-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11f77-154">Requirement</span></span> | <span data-ttu-id="11f77-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="11f77-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f77-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11f77-156">Minimum supported client</span></span><br/> | <span data-ttu-id="11f77-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="11f77-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="11f77-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11f77-158">Minimum supported server</span></span><br/> | <span data-ttu-id="11f77-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11f77-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="11f77-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11f77-160">Namespace</span></span><br/>                | <span data-ttu-id="11f77-161">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="11f77-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="11f77-162">MOF</span><span class="sxs-lookup"><span data-stu-id="11f77-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11f77-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11f77-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11f77-164">DLL</span><span class="sxs-lookup"><span data-stu-id="11f77-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f77-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11f77-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11f77-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11f77-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f77-167">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="11f77-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

