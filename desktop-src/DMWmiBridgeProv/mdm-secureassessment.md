---
title: Classe MDM_SecureAssessment
description: Le \_ SECUREASSESSMENTCLASS MDM est utilisé pour fournir des informations de configuration pour le navigateur d’évaluation sécurisée.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- Classe MDM_SecureAssessment
- Classe MDM_SecureAssessment, Description
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941697"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="2650c-105">\_Classe SECUREASSESSMENT MDM</span><span class="sxs-lookup"><span data-stu-id="2650c-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="2650c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="2650c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2650c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="2650c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2650c-108">La **classe \_ SecureAssessment MDM** est utilisée pour fournir des informations de configuration pour le navigateur d’évaluation sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2650c-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="2650c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2650c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2650c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2650c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="2650c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="2650c-111">Members</span></span>

<span data-ttu-id="2650c-112">La **classe \_ SecureAssessment MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2650c-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="2650c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2650c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2650c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2650c-114">Properties</span></span>

<span data-ttu-id="2650c-115">La **classe \_ SecureAssessment MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2650c-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2650c-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="2650c-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2650c-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2650c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2650c-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="2650c-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2650c-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2650c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2650c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2650c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2650c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2650c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2650c-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2650c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2650c-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="2650c-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="2650c-127">Pour cette classe, la chaîne est « SecureAssessment ».</span><span class="sxs-lookup"><span data-stu-id="2650c-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="2650c-128">LaunchURI</span><span class="sxs-lookup"><span data-stu-id="2650c-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2650c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2650c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2650c-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="2650c-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2650c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2650c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2650c-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2650c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2650c-135">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="2650c-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="2650c-136">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="2650c-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="2650c-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="2650c-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2650c-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2650c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2650c-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="2650c-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2650c-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2650c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2650c-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2650c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2650c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2650c-143">Requirements</span></span>



| <span data-ttu-id="2650c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2650c-144">Requirement</span></span> | <span data-ttu-id="2650c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="2650c-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2650c-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2650c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2650c-147">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2650c-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2650c-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2650c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2650c-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2650c-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2650c-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2650c-150">Namespace</span></span><br/>                | <span data-ttu-id="2650c-151">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="2650c-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2650c-152">MOF</span><span class="sxs-lookup"><span data-stu-id="2650c-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2650c-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2650c-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="2650c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="2650c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2650c-155"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="2650c-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

