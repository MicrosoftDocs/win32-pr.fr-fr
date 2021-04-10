---
title: Classe MDM_DeviceStatus_DeviceGuard01
description: La \_ classe DeviceStatus \_ DeviceGuard01 MDM est utilisée par l’entreprise pour effectuer le suivi de l’inventaire des appareils et interroger l’état de conformité de ces appareils avec leurs stratégies d’entreprise.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- Classe MDM_DeviceStatus_DeviceGuard01
- Classe MDM_DeviceStatus_DeviceGuard01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942528"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="5c3c9-105">\_ \_ Classe DEVICEGUARD01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="5c3c9-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="5c3c9-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="5c3c9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5c3c9-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="5c3c9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5c3c9-108">La \_ classe DeviceStatus \_ DeviceGuard01 MDM est utilisée par l’entreprise pour effectuer le suivi de l’inventaire des appareils et interroger l’état de conformité de ces appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5c3c9-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="5c3c9-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5c3c9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3c9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c3c9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="5c3c9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="5c3c9-111">Members</span></span>

<span data-ttu-id="5c3c9-112">La **classe \_ DeviceStatus \_ DeviceGuard01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5c3c9-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="5c3c9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c3c9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c3c9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c3c9-114">Properties</span></span>

<span data-ttu-id="5c3c9-115">La **classe \_ DeviceStatus \_ DeviceGuard01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5c3c9-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c3c9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3c9-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c3c9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c3c9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5c3c9-120">LsaCfgCredGuardStatus</span><span class="sxs-lookup"><span data-stu-id="5c3c9-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3c9-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5c3c9-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c3c9-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3c9-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c3c9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c3c9-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5c3c9-127">VirtualizationBasedSecurityHwReq</span><span class="sxs-lookup"><span data-stu-id="5c3c9-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3c9-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5c3c9-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5c3c9-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="5c3c9-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3c9-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5c3c9-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c3c9-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5c3c9-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c3c9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c3c9-133">Requirements</span></span>



| <span data-ttu-id="5c3c9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c3c9-134">Requirement</span></span> | <span data-ttu-id="5c3c9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c3c9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3c9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c3c9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3c9-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c3c9-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c3c9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c3c9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3c9-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c3c9-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5c3c9-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5c3c9-140">Namespace</span></span><br/>                | <span data-ttu-id="5c3c9-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="5c3c9-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5c3c9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5c3c9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c3c9-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c3c9-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c3c9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5c3c9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c3c9-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c3c9-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

