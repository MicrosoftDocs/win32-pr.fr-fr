---
title: Classe MDM_DeviceManageability_Provider01_01
description: La \_ classe MDM DeviceManageability \_ Provider01 \_ 01 est utilisée pour récupérer les informations générales sur les fonctionnalités de configuration MDM sur l’appareil.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- Classe MDM_DeviceManageability_Provider01_01
- Classe MDM_DeviceManageability_Provider01_01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843969"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="b398c-105">\_Classe DeviceManageability \_ PROVIDER01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="b398c-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="b398c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b398c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b398c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b398c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b398c-108">La \_ classe MDM DeviceManageability \_ Provider01 \_ 01 est utilisée pour récupérer les informations générales sur les fonctionnalités de configuration MDM sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b398c-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="b398c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b398c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b398c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b398c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="b398c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b398c-111">Members</span></span>

<span data-ttu-id="b398c-112">La classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b398c-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b398c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b398c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b398c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b398c-114">Properties</span></span>

<span data-ttu-id="b398c-115">La classe **MDM \_ DeviceManageability \_ Provider01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b398c-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b398c-116">ConfigInfo</span><span class="sxs-lookup"><span data-stu-id="b398c-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b398c-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b398c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b398c-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b398c-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b398c-119">Vous devez définir la valeur sur \_ serveur pont WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="b398c-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="b398c-120">L’appelant ne peut pas définir dynamiquement l’ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b398c-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="b398c-121">EnrollmentInfo</span><span class="sxs-lookup"><span data-stu-id="b398c-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b398c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b398c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b398c-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b398c-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b398c-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b398c-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b398c-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b398c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b398c-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b398c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b398c-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b398c-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b398c-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="b398c-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b398c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b398c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b398c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b398c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b398c-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b398c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b398c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b398c-132">Requirements</span></span>



| <span data-ttu-id="b398c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b398c-133">Requirement</span></span> | <span data-ttu-id="b398c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b398c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b398c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b398c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b398c-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b398c-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b398c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b398c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b398c-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b398c-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b398c-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b398c-139">Namespace</span></span><br/>                | <span data-ttu-id="b398c-140">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b398c-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b398c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b398c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b398c-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b398c-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b398c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b398c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b398c-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b398c-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

