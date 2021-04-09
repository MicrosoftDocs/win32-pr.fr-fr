---
title: Classe MDM_Update_InstallableUpdates01_01
description: La \_ classe mise à jour MDM \_ InstallableUpdates01 \_ 01 est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- Classe MDM_Update_InstallableUpdates01_01
- Classe MDM_Update_InstallableUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843125"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="329be-105">\_Classe de mise à jour MDM \_ InstallableUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="329be-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="329be-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="329be-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="329be-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="329be-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="329be-108">La **classe \_ mise à jour MDM \_ InstallableUpdates01 \_ 01** est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.</span><span class="sxs-lookup"><span data-stu-id="329be-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="329be-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="329be-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="329be-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="329be-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="329be-111">Membres</span><span class="sxs-lookup"><span data-stu-id="329be-111">Members</span></span>

<span data-ttu-id="329be-112">La **classe \_ \_ InstallableUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="329be-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="329be-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="329be-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="329be-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="329be-114">Properties</span></span>

<span data-ttu-id="329be-115">La classe de **\_ mise à jour MDM \_ InstallableUpdates01 \_ 01** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="329be-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="329be-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="329be-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329be-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="329be-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329be-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="329be-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329be-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="329be-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="329be-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="329be-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="329be-121">Pour cette classe, la chaîne est le GUID de la mise à jour approuvée.</span><span class="sxs-lookup"><span data-stu-id="329be-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="329be-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="329be-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="329be-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="329be-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="329be-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="329be-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="329be-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="329be-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="329be-126">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="329be-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="329be-127">Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/InstallableUpdates »</span><span class="sxs-lookup"><span data-stu-id="329be-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="329be-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="329be-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="329be-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="329be-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="329be-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="329be-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="329be-131">Type</span><span class="sxs-lookup"><span data-stu-id="329be-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="329be-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="329be-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="329be-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="329be-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="329be-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="329be-134">Requirements</span></span>



| <span data-ttu-id="329be-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="329be-135">Requirement</span></span> | <span data-ttu-id="329be-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="329be-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329be-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="329be-137">Minimum supported client</span></span><br/> | <span data-ttu-id="329be-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="329be-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="329be-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="329be-139">Minimum supported server</span></span><br/> | <span data-ttu-id="329be-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="329be-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="329be-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="329be-141">Namespace</span></span><br/>                | <span data-ttu-id="329be-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="329be-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="329be-143">MOF</span><span class="sxs-lookup"><span data-stu-id="329be-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="329be-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="329be-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="329be-145">DLL</span><span class="sxs-lookup"><span data-stu-id="329be-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="329be-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="329be-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

