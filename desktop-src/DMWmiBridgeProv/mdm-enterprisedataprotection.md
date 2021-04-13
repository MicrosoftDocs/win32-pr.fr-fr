---
title: Classe MDM_EnterpriseDataProtection
description: La \_ classe ENTERPRISEDATAPROTECTION MDM est utilisée pour déterminer l’état actuel des paramètres spécifiques de Windows information protection (WIP) (anciennement appelé protection des données d’entreprise).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- Classe MDM_EnterpriseDataProtection
- Classe MDM_EnterpriseDataProtection, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466206"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="676db-105">\_Classe ENTERPRISEDATAPROTECTION MDM</span><span class="sxs-lookup"><span data-stu-id="676db-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="676db-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="676db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="676db-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="676db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="676db-108">La **classe \_ EnterpriseDataProtection MDM** est utilisée pour déterminer l’état actuel des paramètres spécifiques de Windows information protection (WIP) (anciennement appelé protection des données d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="676db-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="676db-109">Pour plus d’informations sur les travaux en cours, consultez [protéger vos données d’entreprise à l’aide de la protection des données d’entreprise (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="676db-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="676db-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="676db-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="676db-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="676db-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="676db-112">Membres</span><span class="sxs-lookup"><span data-stu-id="676db-112">Members</span></span>

<span data-ttu-id="676db-113">La **classe \_ EnterpriseDataProtection MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="676db-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="676db-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="676db-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="676db-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="676db-115">Properties</span></span>

<span data-ttu-id="676db-116">La **classe \_ EnterpriseDataProtection MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="676db-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="676db-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="676db-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="676db-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="676db-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="676db-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="676db-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="676db-120">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="676db-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="676db-121">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="676db-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="676db-122">Pour cette classe, la chaîne est « EnterpriseDataProtection ».</span><span class="sxs-lookup"><span data-stu-id="676db-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="676db-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="676db-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="676db-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="676db-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="676db-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="676db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="676db-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="676db-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="676db-127">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="676db-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="676db-128">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="676db-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="676db-129">État</span><span class="sxs-lookup"><span data-stu-id="676db-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="676db-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="676db-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="676db-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="676db-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="676db-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="676db-132">Requirements</span></span>



| <span data-ttu-id="676db-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="676db-133">Requirement</span></span> | <span data-ttu-id="676db-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="676db-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="676db-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="676db-135">Minimum supported client</span></span><br/> | <span data-ttu-id="676db-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="676db-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="676db-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="676db-137">Minimum supported server</span></span><br/> | <span data-ttu-id="676db-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="676db-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="676db-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="676db-139">Namespace</span></span><br/>                | <span data-ttu-id="676db-140">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="676db-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="676db-141">MOF</span><span class="sxs-lookup"><span data-stu-id="676db-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="676db-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="676db-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="676db-143">DLL</span><span class="sxs-lookup"><span data-stu-id="676db-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="676db-144"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="676db-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

