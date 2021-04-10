---
title: Classe MDM_Update_ApprovedUpdates01_01
description: La \_ classe mise à jour MDM \_ ApprovedUpdates01 \_ 01 est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- Classe MDM_Update_ApprovedUpdates01_01
- Classe MDM_Update_ApprovedUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941696"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="758e1-105">\_Classe de mise à jour MDM \_ ApprovedUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="758e1-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="758e1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="758e1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="758e1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="758e1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="758e1-108">La **classe \_ mise à jour MDM \_ ApprovedUpdates01 \_ 01** est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.</span><span class="sxs-lookup"><span data-stu-id="758e1-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="758e1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="758e1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="758e1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="758e1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="758e1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="758e1-111">Members</span></span>

<span data-ttu-id="758e1-112">La **classe \_ \_ ApprovedUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="758e1-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="758e1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758e1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="758e1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758e1-114">Properties</span></span>

<span data-ttu-id="758e1-115">La classe de **\_ mise à jour MDM \_ ApprovedUpdates01 \_ 01** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="758e1-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="758e1-116">ApprovedTime</span><span class="sxs-lookup"><span data-stu-id="758e1-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="758e1-117">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="758e1-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="758e1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="758e1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="758e1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="758e1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="758e1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="758e1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="758e1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="758e1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="758e1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="758e1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="758e1-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="758e1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="758e1-124">Pour cette classe, la chaîne est le GUID de la mise à jour approuvée.</span><span class="sxs-lookup"><span data-stu-id="758e1-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="758e1-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="758e1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="758e1-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="758e1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="758e1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="758e1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="758e1-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="758e1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="758e1-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="758e1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="758e1-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/ApprovedUpdates »</span><span class="sxs-lookup"><span data-stu-id="758e1-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="758e1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="758e1-131">Requirements</span></span>



| <span data-ttu-id="758e1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="758e1-132">Requirement</span></span> | <span data-ttu-id="758e1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="758e1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758e1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758e1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="758e1-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="758e1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="758e1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758e1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="758e1-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="758e1-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="758e1-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="758e1-138">Namespace</span></span><br/>                | <span data-ttu-id="758e1-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="758e1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="758e1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="758e1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="758e1-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="758e1-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="758e1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="758e1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="758e1-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="758e1-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

