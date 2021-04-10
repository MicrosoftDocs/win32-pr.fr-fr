---
description: Représente les paramètres utilisés pour tester la connectivité réseau d’un ordinateur virtuel.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Classe Msvm_NetworkConnectionDiagnosticSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035222"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="9d5be-103">MSVM \_ NetworkConnectionDiagnosticSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="9d5be-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="9d5be-104">Représente les paramètres utilisés pour tester la connectivité réseau d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9d5be-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="9d5be-105">Utilisé par la méthode [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9d5be-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="9d5be-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9d5be-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d5be-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="9d5be-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9d5be-108">Members</span></span>

<span data-ttu-id="9d5be-109">La classe **MSVM \_ NetworkConnectionDiagnosticSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9d5be-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9d5be-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d5be-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d5be-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d5be-111">Properties</span></span>

<span data-ttu-id="9d5be-112">La classe **MSVM \_ NetworkConnectionDiagnosticSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d5be-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d5be-113">**IsolationId**</span><span class="sxs-lookup"><span data-stu-id="9d5be-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5be-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-116">ID d’isolation.</span><span class="sxs-lookup"><span data-stu-id="9d5be-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-117">**IsSender**</span><span class="sxs-lookup"><span data-stu-id="9d5be-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="9d5be-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-120">Indique si cette méthode est appelée au niveau de l’expéditeur ou du récepteur.</span><span class="sxs-lookup"><span data-stu-id="9d5be-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-121">**PayloadSize**</span><span class="sxs-lookup"><span data-stu-id="9d5be-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5be-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-124">Taille de la charge utile.</span><span class="sxs-lookup"><span data-stu-id="9d5be-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-125">**ReceiverIP**</span><span class="sxs-lookup"><span data-stu-id="9d5be-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d5be-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-128">Adresse IP du récepteur.</span><span class="sxs-lookup"><span data-stu-id="9d5be-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-129">**ReceiverMac**</span><span class="sxs-lookup"><span data-stu-id="9d5be-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d5be-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-132">Adresse MAC du destinataire.</span><span class="sxs-lookup"><span data-stu-id="9d5be-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-133">**SenderIP**</span><span class="sxs-lookup"><span data-stu-id="9d5be-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d5be-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-136">Adresse IP de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="9d5be-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d5be-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="9d5be-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5be-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5be-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5be-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d5be-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d5be-140">Numéro séquentiel.</span><span class="sxs-lookup"><span data-stu-id="9d5be-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d5be-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d5be-141">Requirements</span></span>



| <span data-ttu-id="9d5be-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d5be-142">Requirement</span></span> | <span data-ttu-id="9d5be-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d5be-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5be-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5be-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5be-145">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d5be-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9d5be-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5be-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5be-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d5be-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9d5be-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d5be-148">Namespace</span></span><br/>                | <span data-ttu-id="9d5be-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d5be-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d5be-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9d5be-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d5be-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d5be-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d5be-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9d5be-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d5be-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d5be-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d5be-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d5be-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5be-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="9d5be-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




