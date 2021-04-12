---
title: Classe MDM_Policy_Result01_Maps02
description: La \_ classe Result01 Maps02 de la stratégie MDM \_ \_ représente les stratégies de mappage disponibles.
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- Classe MDM_Policy_Result01_Maps02
- Classe MDM_Policy_Result01_Maps02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465010"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="fb402-105">\_Classe Maps02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="fb402-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="fb402-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fb402-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb402-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fb402-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb402-108">La **classe \_ \_ Result01 \_ Maps02 de la stratégie MDM** représente les stratégies de mappage disponibles.</span><span class="sxs-lookup"><span data-stu-id="fb402-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="fb402-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fb402-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb402-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb402-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="fb402-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fb402-111">Members</span></span>

<span data-ttu-id="fb402-112">La **classe \_ \_ Result01 \_ Maps02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb402-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="fb402-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb402-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb402-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb402-114">Properties</span></span>

<span data-ttu-id="fb402-115">La **classe \_ \_ Result01 \_ Maps02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fb402-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fb402-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="fb402-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb402-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fb402-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb402-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fb402-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fb402-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="fb402-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb402-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fb402-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb402-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fb402-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb402-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb402-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb402-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb402-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb402-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb402-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb402-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb402-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb402-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fb402-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="fb402-127">Pour cette classe, la chaîne est « Maps ».</span><span class="sxs-lookup"><span data-stu-id="fb402-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="fb402-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="fb402-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb402-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fb402-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb402-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb402-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb402-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb402-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fb402-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fb402-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="fb402-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="fb402-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb402-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb402-134">Requirements</span></span>



| <span data-ttu-id="fb402-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb402-135">Requirement</span></span> | <span data-ttu-id="fb402-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb402-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb402-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb402-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fb402-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb402-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb402-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb402-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fb402-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb402-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fb402-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb402-141">Namespace</span></span><br/>                | <span data-ttu-id="fb402-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fb402-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fb402-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fb402-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb402-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb402-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="fb402-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fb402-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb402-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb402-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

