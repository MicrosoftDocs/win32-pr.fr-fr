---
title: Classe MDM_DeviceStatus
description: La \_ classe DEVICESTATUS MDM est utilisée par l’entreprise pour effectuer le suivi de l’inventaire des appareils et interroger l’état de conformité de ces appareils avec leurs stratégies d’entreprise.
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- Classe MDM_DeviceStatus
- Classe MDM_DeviceStatus, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104995"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="37a64-105">\_Classe DEVICESTATUS MDM</span><span class="sxs-lookup"><span data-stu-id="37a64-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="37a64-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="37a64-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37a64-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="37a64-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37a64-108">La **classe \_ DeviceStatus MDM** est utilisée par l’entreprise pour effectuer le suivi de l’inventaire des appareils et interroger l’état de conformité de ces appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="37a64-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="37a64-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37a64-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a64-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37a64-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="37a64-111">Membres</span><span class="sxs-lookup"><span data-stu-id="37a64-111">Members</span></span>

<span data-ttu-id="37a64-112">La **classe \_ DeviceStatus MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37a64-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="37a64-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37a64-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37a64-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37a64-114">Properties</span></span>

<span data-ttu-id="37a64-115">La **classe \_ DeviceStatus MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="37a64-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="37a64-116">DomainName</span><span class="sxs-lookup"><span data-stu-id="37a64-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37a64-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37a64-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37a64-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37a64-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37a64-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37a64-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37a64-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37a64-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37a64-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37a64-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37a64-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37a64-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="37a64-123">Nœud racine du fournisseur de services de configuration DeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="37a64-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="37a64-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="37a64-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37a64-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37a64-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37a64-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37a64-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37a64-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37a64-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="37a64-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="37a64-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="37a64-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="37a64-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="37a64-130">SecureBootState</span><span class="sxs-lookup"><span data-stu-id="37a64-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37a64-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="37a64-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="37a64-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37a64-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37a64-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37a64-133">Requirements</span></span>



| <span data-ttu-id="37a64-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37a64-134">Requirement</span></span> | <span data-ttu-id="37a64-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a64-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a64-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37a64-136">Minimum supported client</span></span><br/> | <span data-ttu-id="37a64-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37a64-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37a64-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37a64-138">Minimum supported server</span></span><br/> | <span data-ttu-id="37a64-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37a64-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="37a64-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37a64-140">Namespace</span></span><br/>                | <span data-ttu-id="37a64-141">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="37a64-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="37a64-142">MOF</span><span class="sxs-lookup"><span data-stu-id="37a64-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37a64-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37a64-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37a64-144">DLL</span><span class="sxs-lookup"><span data-stu-id="37a64-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37a64-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37a64-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a64-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37a64-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a64-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="37a64-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

