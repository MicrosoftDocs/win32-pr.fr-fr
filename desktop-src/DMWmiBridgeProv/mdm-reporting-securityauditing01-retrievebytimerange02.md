---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: La \_ \_ \_ classe SecurityAuditing01 RETRIEVEBYTIMERANGE02 de rapports MDM est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740061"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="bf44c-105">\_ \_ Classe RetrieveByTimeRange02 SecurityAuditing01 de création de rapports MDM \_</span><span class="sxs-lookup"><span data-stu-id="bf44c-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="bf44c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bf44c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf44c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bf44c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf44c-108">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 de rapports MDM** est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime. les StartTime et StopTime sont exprimés au format ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="bf44c-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="bf44c-109">Si les valeurs StartTime et StopTime ne sont pas spécifiées, les valeurs sont interprétées comme étant la première ou la dernière heure existante.</span><span class="sxs-lookup"><span data-stu-id="bf44c-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="bf44c-110">Voici les autres scénarios possibles :</span><span class="sxs-lookup"><span data-stu-id="bf44c-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="bf44c-111">Si les StartTime et StopTime ne sont pas spécifiés, il retourne tous les journaux existants.</span><span class="sxs-lookup"><span data-stu-id="bf44c-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="bf44c-112">Si le StopTime est spécifié, mais que l’heure de début n’est pas spécifiée, tous les journaux qui existent avant le StopTime sont retournés.</span><span class="sxs-lookup"><span data-stu-id="bf44c-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="bf44c-113">Si l’heure de début est spécifiée, mais que le StopTime n’est pas spécifié, tous les journaux qui existent à partir de StartTime sont retournés.</span><span class="sxs-lookup"><span data-stu-id="bf44c-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="bf44c-114">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bf44c-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf44c-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf44c-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="bf44c-116">Membres</span><span class="sxs-lookup"><span data-stu-id="bf44c-116">Members</span></span>

<span data-ttu-id="bf44c-117">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf44c-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="bf44c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf44c-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf44c-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf44c-119">Properties</span></span>

<span data-ttu-id="bf44c-120">La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf44c-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf44c-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf44c-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf44c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf44c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf44c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf44c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf44c-125">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bf44c-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="bf44c-126">Pour cette classe, la chaîne est « RetrieveByTimeRange ».</span><span class="sxs-lookup"><span data-stu-id="bf44c-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="bf44c-127">Journaux</span><span class="sxs-lookup"><span data-stu-id="bf44c-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf44c-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf44c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf44c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf44c-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="bf44c-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf44c-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf44c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf44c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf44c-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf44c-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bf44c-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf44c-135">Pour cette classe, la chaîne est « ./Vendor/MSFT/SecurityAuditing »</span><span class="sxs-lookup"><span data-stu-id="bf44c-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="bf44c-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="bf44c-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf44c-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf44c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf44c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf44c-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="bf44c-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf44c-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf44c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf44c-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf44c-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf44c-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf44c-142">Requirements</span></span>



| <span data-ttu-id="bf44c-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf44c-143">Requirement</span></span> | <span data-ttu-id="bf44c-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf44c-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf44c-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf44c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bf44c-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf44c-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bf44c-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf44c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bf44c-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf44c-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="bf44c-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf44c-149">Namespace</span></span><br/>                | <span data-ttu-id="bf44c-150">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="bf44c-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="bf44c-151">MOF</span><span class="sxs-lookup"><span data-stu-id="bf44c-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf44c-152"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf44c-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="bf44c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bf44c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf44c-154"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="bf44c-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

