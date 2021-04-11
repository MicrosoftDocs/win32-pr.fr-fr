---
title: Classe MDM_Reboot
description: Le \_ REBOOTCLASS MDM est utilisé pour configurer les paramètres de redémarrage.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- Classe MDM_Reboot
- Classe MDM_Reboot, Description
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032396"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="c4182-105">\_Classe de redémarrage MDM</span><span class="sxs-lookup"><span data-stu-id="c4182-105">MDM\_Reboot class</span></span>

<span data-ttu-id="c4182-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c4182-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c4182-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c4182-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c4182-108">La classe de **\_ redémarrage MDM** est utilisée pour configurer les paramètres de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="c4182-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="c4182-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c4182-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4182-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4182-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="c4182-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c4182-111">Members</span></span>

<span data-ttu-id="c4182-112">La classe de **\_ redémarrage MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4182-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="c4182-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4182-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4182-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4182-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4182-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4182-115">Methods</span></span>

<span data-ttu-id="c4182-116">La **classe \_ redémarrage MDM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c4182-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="c4182-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="c4182-117">Method</span></span>                                                | <span data-ttu-id="c4182-118">Description</span><span class="sxs-lookup"><span data-stu-id="c4182-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="c4182-119">**RebootNowMethod**</span><span class="sxs-lookup"><span data-stu-id="c4182-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="c4182-120">Cette méthode exécute un redémarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c4182-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4182-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4182-121">Properties</span></span>

<span data-ttu-id="c4182-122">La classe de **\_ redémarrage MDM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c4182-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4182-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4182-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4182-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4182-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4182-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4182-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4182-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4182-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4182-127">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c4182-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="c4182-128">Pour cette classe, la chaîne est « reboot ».</span><span class="sxs-lookup"><span data-stu-id="c4182-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="c4182-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="c4182-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4182-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4182-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4182-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4182-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4182-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4182-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4182-133">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c4182-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="c4182-134">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="c4182-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4182-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4182-135">Requirements</span></span>



| <span data-ttu-id="c4182-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4182-136">Requirement</span></span> | <span data-ttu-id="c4182-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4182-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4182-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4182-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c4182-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4182-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c4182-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4182-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c4182-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4182-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c4182-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4182-142">Namespace</span></span><br/>                | <span data-ttu-id="c4182-143">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c4182-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c4182-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c4182-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4182-145"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4182-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c4182-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c4182-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4182-147"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4182-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

