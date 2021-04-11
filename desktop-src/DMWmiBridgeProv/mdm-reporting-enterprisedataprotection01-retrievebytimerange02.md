---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: La \_ \_ \_ classe EnterpriseDataProtection01 RETRIEVEBYTIMERANGE02 de rapports MDM est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032391"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="eb5b1-105">\_ \_ Classe RetrieveByTimeRange02 EnterpriseDataProtection01 de création de rapports MDM \_</span><span class="sxs-lookup"><span data-stu-id="eb5b1-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="eb5b1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb5b1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="eb5b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb5b1-108">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 de rapports MDM** est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="eb5b1-109">Les StartTime et StopTime sont exprimés au format ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="eb5b1-110">Si les valeurs StartTime et StopTime ne sont pas spécifiées, les valeurs sont interprétées comme étant la première ou la dernière heure existante.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="eb5b1-111">Voici les autres scénarios possibles :</span><span class="sxs-lookup"><span data-stu-id="eb5b1-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="eb5b1-112">Si les StartTime et StopTime ne sont pas spécifiés, il retourne tous les journaux existants.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="eb5b1-113">Si le StopTime est spécifié, mais que l’heure de début n’est pas spécifiée, tous les journaux qui existent avant le StopTime sont retournés.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="eb5b1-114">Si l’heure de début est spécifiée, mais que le StopTime n’est pas spécifié, tous les journaux qui existent à partir de StartTime sont retournés.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="eb5b1-115">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5b1-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb5b1-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="eb5b1-117">Membres</span><span class="sxs-lookup"><span data-stu-id="eb5b1-117">Members</span></span>

<span data-ttu-id="eb5b1-118">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb5b1-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="eb5b1-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb5b1-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb5b1-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb5b1-120">Properties</span></span>

<span data-ttu-id="eb5b1-121">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb5b1-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb5b1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb5b1-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb5b1-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="eb5b1-127">Pour cette classe, la chaîne est « RetrieveByTimeRange ».</span><span class="sxs-lookup"><span data-stu-id="eb5b1-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="eb5b1-128">Journaux</span><span class="sxs-lookup"><span data-stu-id="eb5b1-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb5b1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb5b1-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb5b1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb5b1-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb5b1-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb5b1-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="eb5b1-136">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseDataProtection »</span><span class="sxs-lookup"><span data-stu-id="eb5b1-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="eb5b1-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="eb5b1-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb5b1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb5b1-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="eb5b1-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb5b1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb5b1-143">Type</span><span class="sxs-lookup"><span data-stu-id="eb5b1-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb5b1-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="eb5b1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb5b1-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb5b1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb5b1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb5b1-146">Requirements</span></span>



| <span data-ttu-id="eb5b1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb5b1-147">Requirement</span></span> | <span data-ttu-id="eb5b1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb5b1-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5b1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb5b1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="eb5b1-150">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb5b1-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eb5b1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb5b1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="eb5b1-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb5b1-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="eb5b1-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb5b1-153">Namespace</span></span><br/>                | <span data-ttu-id="eb5b1-154">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="eb5b1-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="eb5b1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="eb5b1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb5b1-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb5b1-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="eb5b1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="eb5b1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb5b1-158"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb5b1-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

