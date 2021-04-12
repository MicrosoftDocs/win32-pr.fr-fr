---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: La \_ \_ classe EnterpriseDataProtection01 RetrieveByCount02 de rapports MDM \_ est utilisée pour récupérer un nombre spécifié de journaux à partir de StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464347"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="c2c4f-105">\_ \_ Classe RetrieveByCount02 EnterpriseDataProtection01 de création de rapports MDM \_</span><span class="sxs-lookup"><span data-stu-id="c2c4f-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="c2c4f-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2c4f-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c2c4f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2c4f-108">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 de rapports MDM** est utilisée pour récupérer un nombre spécifié de journaux à partir de StartTime.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="c2c4f-109">L’heure de début est exprimée au format ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="c2c4f-110">Vous pouvez définir le nombre de journaux requis en définissant LogCount et StartTime.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="c2c4f-111">Elle retourne le nombre spécifié de journaux ou moins, si le nombre total de journaux est inférieur à LogCount.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="c2c4f-112">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c4f-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2c4f-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="c2c4f-114">Membres</span><span class="sxs-lookup"><span data-stu-id="c2c4f-114">Members</span></span>

<span data-ttu-id="c2c4f-115">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02** de la gestion des rapports MDM a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c2c4f-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="c2c4f-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2c4f-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2c4f-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c2c4f-117">Properties</span></span>

<span data-ttu-id="c2c4f-118">La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02** de la gestion des rapports MDM a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2c4f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2c4f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2c4f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2c4f-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c2c4f-124">Pour cette classe, la chaîne est « RetrieveByCount ».</span><span class="sxs-lookup"><span data-stu-id="c2c4f-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="c2c4f-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="c2c4f-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c2c4f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c2c4f-128">Journaux</span><span class="sxs-lookup"><span data-stu-id="c2c4f-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c2c4f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2c4f-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c2c4f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2c4f-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2c4f-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c2c4f-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="c2c4f-136">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseDataProtection »</span><span class="sxs-lookup"><span data-stu-id="c2c4f-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="c2c4f-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="c2c4f-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c2c4f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c2c4f-140">Type</span><span class="sxs-lookup"><span data-stu-id="c2c4f-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2c4f-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c2c4f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2c4f-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c2c4f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2c4f-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2c4f-143">Requirements</span></span>



| <span data-ttu-id="c2c4f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2c4f-144">Requirement</span></span> | <span data-ttu-id="c2c4f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2c4f-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c4f-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c4f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c4f-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2c4f-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2c4f-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c4f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c4f-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c4f-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c2c4f-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2c4f-150">Namespace</span></span><br/>                | <span data-ttu-id="c2c4f-151">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c2c4f-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c2c4f-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c2c4f-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2c4f-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2c4f-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c2c4f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c2c4f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2c4f-155"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2c4f-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

