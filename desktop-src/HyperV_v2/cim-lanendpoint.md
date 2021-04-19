---
description: Point de terminaison de communication qui peut se connecter à un réseau local pour envoyer et recevoir des trames de données. Les points de terminaison LAN incluent les interfaces Ethernet, Token Ring et FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Classe CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545184"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="15f26-104">\_Classe CIM LANEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f26-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="15f26-105">Point de terminaison de communication qui peut se connecter à un réseau local pour envoyer et recevoir des trames de données.</span><span class="sxs-lookup"><span data-stu-id="15f26-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="15f26-106">Les points de terminaison LAN incluent les interfaces Ethernet, Token Ring et FDDI.</span><span class="sxs-lookup"><span data-stu-id="15f26-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f26-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f26-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="15f26-108">Membres</span><span class="sxs-lookup"><span data-stu-id="15f26-108">Members</span></span>

<span data-ttu-id="15f26-109">La classe **CIM \_ LANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15f26-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="15f26-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15f26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15f26-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="15f26-111">Properties</span></span>

<span data-ttu-id="15f26-112">La classe **CIM \_ LANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="15f26-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15f26-113">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="15f26-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="15f26-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15f26-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15f26-116">Tableau qui contient d’autres adresses monodiffusion qui peuvent être utilisées pour communiquer avec le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="15f26-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="15f26-117">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="15f26-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="15f26-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15f26-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15f26-120">Tableau qui contient les adresses de multidiffusion sur lesquelles le point de terminaison LAN écoute.</span><span class="sxs-lookup"><span data-stu-id="15f26-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="15f26-121">**LANID**</span><span class="sxs-lookup"><span data-stu-id="15f26-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15f26-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f26-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f26-124">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LANID, CIM \_ LANSegment. LANID")</span><span class="sxs-lookup"><span data-stu-id="15f26-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="15f26-125">Étiquette ou identificateur du segment LAN auquel le point de terminaison est connecté.</span><span class="sxs-lookup"><span data-stu-id="15f26-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="15f26-126">Si le point de terminaison n’est pas actuellement connecté ou si ces informations sont inconnues, **LANID** a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="15f26-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="15f26-127">**LANType**</span><span class="sxs-lookup"><span data-stu-id="15f26-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15f26-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15f26-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f26-130">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")</span><span class="sxs-lookup"><span data-stu-id="15f26-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="15f26-131">Description déconseillée : type de technologie utilisée sur le réseau local.</span><span class="sxs-lookup"><span data-stu-id="15f26-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="15f26-132">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="15f26-132">This property is deprecated.</span></span> <span data-ttu-id="15f26-133">Au lieu de cela, nous vous recommandons d’utiliser la propriété **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="15f26-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15f26-134">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="15f26-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15f26-135">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="15f26-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="15f26-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="15f26-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="15f26-137">**TokenRing** (3)</span><span class="sxs-lookup"><span data-stu-id="15f26-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="15f26-138">**FDDI** (4)</span><span class="sxs-lookup"><span data-stu-id="15f26-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15f26-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="15f26-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15f26-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f26-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f26-142">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="15f26-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="15f26-143">Adresse de monodiffusion principale utilisée par le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="15f26-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="15f26-144">L’adresse MAC doit être mise en forme avec les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="15f26-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="15f26-145">L’adresse se compose de douze chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="15f26-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="15f26-146">Chaque paire de chiffres représente l’un des six octets de l’adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="15f26-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="15f26-147">Chaque paire de chiffres doit être dans l’ordre des bits canoniques conformément à la norme RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="15f26-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="15f26-148">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="15f26-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15f26-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15f26-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f26-151">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="15f26-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="15f26-152">Taille maximale, en octets, des champs de données envoyés ou reçus par le point de terminaison LAN.</span><span class="sxs-lookup"><span data-stu-id="15f26-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="15f26-153">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="15f26-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f26-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="15f26-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f26-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="15f26-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f26-156">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**\_ ProtocolEndpoint CIM**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")</span><span class="sxs-lookup"><span data-stu-id="15f26-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="15f26-157">Description déconseillée : type de technologie utilisée sur le réseau local lorsque la propriété **LANType** est définie sur « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="15f26-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="15f26-158">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="15f26-158">This property is deprecated.</span></span> <span data-ttu-id="15f26-159">Au lieu de cela, nous vous recommandons d’utiliser la propriété **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="15f26-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15f26-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15f26-160">Requirements</span></span>



| <span data-ttu-id="15f26-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15f26-161">Requirement</span></span> | <span data-ttu-id="15f26-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f26-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f26-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f26-163">Minimum supported client</span></span><br/> | <span data-ttu-id="15f26-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15f26-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15f26-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f26-165">Minimum supported server</span></span><br/> | <span data-ttu-id="15f26-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f26-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15f26-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15f26-167">Namespace</span></span><br/>                | <span data-ttu-id="15f26-168">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="15f26-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15f26-169">MOF</span><span class="sxs-lookup"><span data-stu-id="15f26-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15f26-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15f26-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15f26-171">DLL</span><span class="sxs-lookup"><span data-stu-id="15f26-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15f26-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15f26-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15f26-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f26-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f26-174">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="15f26-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

