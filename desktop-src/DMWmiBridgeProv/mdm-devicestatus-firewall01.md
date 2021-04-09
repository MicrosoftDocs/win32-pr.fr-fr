---
title: Classe MDM_DeviceStatus_Firewall01
description: La \_ classe DeviceStatus \_ Firewall01 MDM est utilisée par l’entreprise pour interroger l’état de conformité du pare-feu des appareils avec leurs stratégies d’entreprise.
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- Classe MDM_DeviceStatus_Firewall01
- Classe MDM_DeviceStatus_Firewall01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742628"
---
# <a name="mdm_devicestatus_firewall01-class"></a><span data-ttu-id="d8dd7-105">\_ \_ Classe FIREWALL01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="d8dd7-105">MDM\_DeviceStatus\_Firewall01 class</span></span>

<span data-ttu-id="d8dd7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8dd7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d8dd7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8dd7-108">La **classe \_ DeviceStatus \_ Firewall01 MDM** est utilisée par l’entreprise pour interroger l’état de conformité du pare-feu des appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-108">The **MDM\_DeviceStatus\_Firewall01** class is used by the enterprise to query the state of firewall compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="d8dd7-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8dd7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8dd7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="d8dd7-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d8dd7-111">Members</span></span>

<span data-ttu-id="d8dd7-112">La **classe \_ DeviceStatus \_ Firewall01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8dd7-112">The **MDM\_DeviceStatus\_Firewall01** class has these types of members:</span></span>

-   [<span data-ttu-id="d8dd7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8dd7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8dd7-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8dd7-114">Properties</span></span>

<span data-ttu-id="d8dd7-115">La **classe \_ DeviceStatus \_ Firewall01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-115">The **MDM\_DeviceStatus\_Firewall01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8dd7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8dd7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8dd7-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8dd7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8dd7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8dd7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8dd7-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8dd7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8dd7-120">Nœud pour la requête de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-120">Node for the firewall query.</span></span>

</dd> <dt>

<span data-ttu-id="d8dd7-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="d8dd7-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8dd7-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8dd7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8dd7-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8dd7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8dd7-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8dd7-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8dd7-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d8dd7-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="d8dd7-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="d8dd7-127">État</span><span class="sxs-lookup"><span data-stu-id="d8dd7-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8dd7-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8dd7-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8dd7-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d8dd7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8dd7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8dd7-130">Requirements</span></span>



| <span data-ttu-id="d8dd7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8dd7-131">Requirement</span></span> | <span data-ttu-id="d8dd7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8dd7-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dd7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8dd7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8dd7-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8dd7-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8dd7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8dd7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8dd7-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8dd7-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8dd7-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8dd7-137">Namespace</span></span><br/>                | <span data-ttu-id="d8dd7-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d8dd7-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d8dd7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d8dd7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8dd7-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8dd7-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8dd7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d8dd7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8dd7-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8dd7-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

