---
description: Connecte un service de pontage transparent à une entrée de transfert dynamique (adresse MAC apprise).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Classe Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951434"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="e4a8c-103">MSVM \_ TransparentBridgingDynamicForwarding, classe</span><span class="sxs-lookup"><span data-stu-id="e4a8c-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="e4a8c-104">Connecte un service de pontage transparent à une entrée de transfert dynamique (adresse MAC apprise).</span><span class="sxs-lookup"><span data-stu-id="e4a8c-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="e4a8c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e4a8c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4a8c-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e4a8c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e4a8c-107">Members</span></span>

<span data-ttu-id="e4a8c-108">La classe **MSVM \_ TransparentBridgingDynamicForwarding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4a8c-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="e4a8c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4a8c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4a8c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4a8c-110">Properties</span></span>

<span data-ttu-id="e4a8c-111">La classe **MSVM \_ TransparentBridgingDynamicForwarding** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4a8c-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4a8c-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4a8c-113">Type de données : **[ **MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e4a8c-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4a8c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4a8c-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e4a8c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e4a8c-116">Référence à une instance de la classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) qui représente le service de pontage transparent.</span><span class="sxs-lookup"><span data-stu-id="e4a8c-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="e4a8c-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4a8c-118">Type de données : **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e4a8c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4a8c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4a8c-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="e4a8c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e4a8c-121">Référence à une instance de la classe [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) qui représente l’entrée de transfert dynamique de la base de données de transfert.</span><span class="sxs-lookup"><span data-stu-id="e4a8c-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4a8c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e4a8c-122">Remarks</span></span>

<span data-ttu-id="e4a8c-123">L’accès à la classe **MSVM \_ TransparentBridgingDynamicForwarding** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="e4a8c-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e4a8c-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e4a8c-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a8c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4a8c-125">Requirements</span></span>



| <span data-ttu-id="e4a8c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4a8c-126">Requirement</span></span> | <span data-ttu-id="e4a8c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4a8c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a8c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a8c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a8c-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a8c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e4a8c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a8c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a8c-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a8c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4a8c-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4a8c-132">Namespace</span></span><br/>                | <span data-ttu-id="e4a8c-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e4a8c-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e4a8c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e4a8c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4a8c-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4a8c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4a8c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e4a8c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4a8c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4a8c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4a8c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4a8c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a8c-139">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="e4a8c-140">**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**</span><span class="sxs-lookup"><span data-stu-id="e4a8c-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

