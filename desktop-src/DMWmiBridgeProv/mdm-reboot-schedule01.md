---
title: Classe MDM_Reboot_Schedule01
description: Le \_ Schedule01class de redémarrage MDM \_ est utilisé pour configurer une heure spécifique pour le redémarrage d’un appareil.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Classe MDM_Reboot_Schedule01
- Classe MDM_Reboot_Schedule01, Description
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464358"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="a0cdd-105">\_Classe Schedule01 de redémarrage MDM \_</span><span class="sxs-lookup"><span data-stu-id="a0cdd-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="a0cdd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0cdd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a0cdd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a0cdd-108">La **classe \_ \_ Schedule01 de redémarrage MDM** est utilisée pour configurer une heure spécifique pour le redémarrage d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="a0cdd-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cdd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0cdd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="a0cdd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a0cdd-111">Members</span></span>

<span data-ttu-id="a0cdd-112">La **classe \_ \_ Schedule01 de redémarrage MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0cdd-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="a0cdd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0cdd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0cdd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0cdd-114">Properties</span></span>

<span data-ttu-id="a0cdd-115">La **classe \_ \_ Schedule01 de redémarrage MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a0cdd-116">DailyRecurrent</span><span class="sxs-lookup"><span data-stu-id="a0cdd-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0cdd-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0cdd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0cdd-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0cdd-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0cdd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0cdd-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0cdd-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="a0cdd-124">Pour cette classe, la chaîne est « Schedule ».</span><span class="sxs-lookup"><span data-stu-id="a0cdd-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="a0cdd-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0cdd-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0cdd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0cdd-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0cdd-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a0cdd-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="a0cdd-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Reboot »</span><span class="sxs-lookup"><span data-stu-id="a0cdd-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="a0cdd-131">Unique</span><span class="sxs-lookup"><span data-stu-id="a0cdd-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0cdd-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0cdd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0cdd-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0cdd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0cdd-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0cdd-134">Requirements</span></span>



| <span data-ttu-id="a0cdd-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0cdd-135">Requirement</span></span> | <span data-ttu-id="a0cdd-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0cdd-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cdd-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cdd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cdd-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0cdd-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a0cdd-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cdd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cdd-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0cdd-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a0cdd-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a0cdd-141">Namespace</span></span><br/>                | <span data-ttu-id="a0cdd-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a0cdd-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a0cdd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a0cdd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0cdd-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0cdd-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="a0cdd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a0cdd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0cdd-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="a0cdd-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

