---
title: Classe MDM_Firewall_App04
description: La \_ classe App04 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- Classe MDM_Firewall_App04
- Classe MDM_Firewall_App04, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103336"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="fff66-105">\_Classe App04 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="fff66-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="fff66-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fff66-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fff66-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fff66-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fff66-108">La \_ classe App04 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="fff66-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="fff66-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fff66-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff66-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fff66-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="fff66-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fff66-111">Members</span></span>

<span data-ttu-id="fff66-112">La **classe \_ \_ App04 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fff66-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="fff66-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fff66-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fff66-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fff66-114">Properties</span></span>

<span data-ttu-id="fff66-115">La **classe \_ \_ App04 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fff66-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fff66-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="fff66-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fff66-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fff66-119">Fqbn</span><span class="sxs-lookup"><span data-stu-id="fff66-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fff66-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fff66-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fff66-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fff66-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fff66-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fff66-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fff66-126">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="fff66-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fff66-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fff66-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="fff66-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fff66-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fff66-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fff66-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fff66-133">FormName</span><span class="sxs-lookup"><span data-stu-id="fff66-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fff66-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fff66-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fff66-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fff66-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fff66-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fff66-136">Requirements</span></span>



| <span data-ttu-id="fff66-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fff66-137">Requirement</span></span> | <span data-ttu-id="fff66-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="fff66-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff66-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff66-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fff66-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fff66-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fff66-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff66-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fff66-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff66-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="fff66-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fff66-143">Namespace</span></span><br/>                | <span data-ttu-id="fff66-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fff66-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="fff66-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fff66-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff66-146"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff66-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff66-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fff66-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff66-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff66-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

