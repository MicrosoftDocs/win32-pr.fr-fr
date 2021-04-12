---
title: Classe MDM_Update_FailedUpdates01_01
description: La \_ classe FailedUpdates01 01 de la mise à jour MDM \_ \_ est utilisée pour gérer les mises à jour ayant échoué.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- Classe MDM_Update_FailedUpdates01_01
- Classe MDM_Update_FailedUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464346"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="70cac-105">\_Classe de mise à jour MDM \_ FailedUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="70cac-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="70cac-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="70cac-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="70cac-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="70cac-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="70cac-108">La **classe \_ \_ FailedUpdates01 \_ 01 de la mise à jour MDM** est utilisée pour gérer les mises à jour ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="70cac-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="70cac-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70cac-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cac-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70cac-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="70cac-111">Membres</span><span class="sxs-lookup"><span data-stu-id="70cac-111">Members</span></span>

<span data-ttu-id="70cac-112">La **classe \_ \_ FailedUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70cac-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="70cac-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70cac-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70cac-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70cac-114">Properties</span></span>

<span data-ttu-id="70cac-115">La classe de **\_ mise à jour MDM \_ FailedUpdates01 \_ 01** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70cac-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="70cac-116">HResult</span><span class="sxs-lookup"><span data-stu-id="70cac-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cac-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="70cac-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="70cac-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70cac-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70cac-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="70cac-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cac-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70cac-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70cac-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70cac-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70cac-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70cac-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="70cac-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="70cac-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="70cac-124">Pour cette classe, la chaîne est le GUID de la mise à jour ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="70cac-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="70cac-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="70cac-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cac-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70cac-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70cac-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70cac-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70cac-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70cac-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="70cac-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="70cac-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="70cac-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/FailedUpdates »</span><span class="sxs-lookup"><span data-stu-id="70cac-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="70cac-131">**State**</span><span class="sxs-lookup"><span data-stu-id="70cac-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cac-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="70cac-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="70cac-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="70cac-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70cac-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70cac-134">Requirements</span></span>



| <span data-ttu-id="70cac-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70cac-135">Requirement</span></span> | <span data-ttu-id="70cac-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="70cac-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70cac-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70cac-137">Minimum supported client</span></span><br/> | <span data-ttu-id="70cac-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70cac-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70cac-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70cac-139">Minimum supported server</span></span><br/> | <span data-ttu-id="70cac-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70cac-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="70cac-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70cac-141">Namespace</span></span><br/>                | <span data-ttu-id="70cac-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="70cac-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="70cac-143">MOF</span><span class="sxs-lookup"><span data-stu-id="70cac-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70cac-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70cac-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="70cac-145">DLL</span><span class="sxs-lookup"><span data-stu-id="70cac-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70cac-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="70cac-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

