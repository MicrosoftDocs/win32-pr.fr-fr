---
title: Classe MDM_DeviceStatus_Battery01
description: La \_ classe DeviceStatus \_ Battery01 MDM est utilisée par l’entreprise pour interroger l’état de la compatibilité de la batterie des appareils avec leurs stratégies d’entreprise.
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- Classe MDM_DeviceStatus_Battery01
- Classe MDM_DeviceStatus_Battery01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543055"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="21550-105">\_ \_ Classe BATTERY01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="21550-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="21550-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="21550-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="21550-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="21550-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="21550-108">La **classe \_ DeviceStatus \_ Battery01 MDM** est utilisée par l’entreprise pour interroger l’état de la compatibilité de la batterie des appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="21550-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="21550-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="21550-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="21550-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21550-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="21550-111">Membres</span><span class="sxs-lookup"><span data-stu-id="21550-111">Members</span></span>

<span data-ttu-id="21550-112">La **classe \_ DeviceStatus \_ Battery01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="21550-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="21550-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21550-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21550-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21550-114">Properties</span></span>

<span data-ttu-id="21550-115">La **classe \_ DeviceStatus \_ Battery01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="21550-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="21550-116">EstimatedChargeRemaining</span><span class="sxs-lookup"><span data-stu-id="21550-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21550-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="21550-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21550-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21550-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="21550-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="21550-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21550-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="21550-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21550-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21550-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="21550-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="21550-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21550-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21550-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21550-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21550-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21550-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21550-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="21550-126">Nœud de la requête de batterie.</span><span class="sxs-lookup"><span data-stu-id="21550-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="21550-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="21550-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21550-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21550-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21550-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21550-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21550-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21550-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="21550-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="21550-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="21550-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="21550-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="21550-133">État</span><span class="sxs-lookup"><span data-stu-id="21550-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21550-134">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="21550-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21550-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21550-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21550-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21550-136">Requirements</span></span>



| <span data-ttu-id="21550-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21550-137">Requirement</span></span> | <span data-ttu-id="21550-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="21550-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21550-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21550-139">Minimum supported client</span></span><br/> | <span data-ttu-id="21550-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21550-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21550-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21550-141">Minimum supported server</span></span><br/> | <span data-ttu-id="21550-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="21550-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="21550-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21550-143">Namespace</span></span><br/>                | <span data-ttu-id="21550-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="21550-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="21550-145">MOF</span><span class="sxs-lookup"><span data-stu-id="21550-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21550-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21550-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="21550-147">DLL</span><span class="sxs-lookup"><span data-stu-id="21550-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21550-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21550-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

