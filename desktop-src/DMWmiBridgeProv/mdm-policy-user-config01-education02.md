---
title: Classe MDM_Policy_User_Config01_Education02
description: La \_ classe Education02 de la stratégie MDM \_ User \_ Config01 \_ configure les stratégies de formation.
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- Classe MDM_Policy_User_Config01_Education02
- Classe MDM_Policy_User_Config01_Education02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae8508668b95edce1d4c4a2d0e99cbba2bc6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941835"
---
# <a name="mdm_policy_user_config01_education02-class"></a><span data-ttu-id="8c6d4-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Education02</span><span class="sxs-lookup"><span data-stu-id="8c6d4-105">MDM\_Policy\_User\_Config01\_Education02 class</span></span>

<span data-ttu-id="8c6d4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c6d4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8c6d4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c6d4-108">La \_ classe Education02 de la stratégie MDM \_ User \_ Config01 \_ configure les stratégies de formation.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-108">The MDM\_Policy\_User\_Config01\_Education02 class configures the education policies.</span></span>

<span data-ttu-id="8c6d4-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6d4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c6d4-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="8c6d4-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8c6d4-111">Members</span></span>

<span data-ttu-id="8c6d4-112">La **classe \_ \_ \_ Config01 \_ Education02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c6d4-112">The **MDM\_Policy\_User\_Config01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="8c6d4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c6d4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c6d4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c6d4-114">Properties</span></span>

<span data-ttu-id="8c6d4-115">La **classe \_ \_ \_ Config01 \_ Education02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c6d4-115">The **MDM\_Policy\_User\_Config01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c6d4-116">DefaultPrinterName</span><span class="sxs-lookup"><span data-stu-id="8c6d4-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6d4-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c6d4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c6d4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6d4-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c6d4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c6d4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c6d4-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6d4-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c6d4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c6d4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c6d4-127">PreventAddingNewPrinters</span><span class="sxs-lookup"><span data-stu-id="8c6d4-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6d4-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c6d4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c6d4-130">PrinterNames</span><span class="sxs-lookup"><span data-stu-id="8c6d4-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c6d4-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c6d4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c6d4-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c6d4-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c6d4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c6d4-133">Requirements</span></span>



| <span data-ttu-id="8c6d4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c6d4-134">Requirement</span></span> | <span data-ttu-id="8c6d4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c6d4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6d4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c6d4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6d4-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c6d4-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c6d4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c6d4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6d4-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c6d4-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8c6d4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8c6d4-140">Namespace</span></span><br/>                | <span data-ttu-id="8c6d4-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8c6d4-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8c6d4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8c6d4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c6d4-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c6d4-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c6d4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8c6d4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c6d4-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6d4-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

