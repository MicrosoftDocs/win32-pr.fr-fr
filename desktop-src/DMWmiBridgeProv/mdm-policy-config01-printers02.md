---
title: Classe MDM_Policy_Config01_Printers02
description: La \_ classe Config01 Printers02 de la stratégie MDM \_ \_ configure les stratégies d’imprimante.
ms.assetid: c0e6dc53-5f84-4cef-a4c4-08db6486784a
keywords:
- Classe MDM_Policy_Config01_Printers02
- Classe MDM_Policy_Config01_Printers02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Printers02
- MDM_Policy_Config01_Printers02.InstanceID
- MDM_Policy_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2cfdc41cfb956d00a509ba499b22e2435d7973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843545"
---
# <a name="mdm_policy_config01_printers02-class"></a><span data-ttu-id="bf9f6-105">\_Classe Printers02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="bf9f6-105">MDM\_Policy\_Config01\_Printers02 class</span></span>

<span data-ttu-id="bf9f6-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bf9f6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf9f6-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bf9f6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf9f6-108">La \_ classe Config01 Printers02 de la stratégie MDM \_ \_ configure les stratégies d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="bf9f6-108">The MDM\_Policy\_Config01\_Printers02 class configures the printer policies.</span></span>

<span data-ttu-id="bf9f6-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bf9f6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9f6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf9f6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="bf9f6-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bf9f6-111">Members</span></span>

<span data-ttu-id="bf9f6-112">La **classe \_ \_ Config01 \_ Printers02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bf9f6-112">The **MDM\_Policy\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="bf9f6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf9f6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf9f6-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bf9f6-114">Properties</span></span>

<span data-ttu-id="bf9f6-115">La **classe \_ \_ Config01 \_ Printers02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf9f6-115">The **MDM\_Policy\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf9f6-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf9f6-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf9f6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf9f6-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf9f6-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf9f6-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bf9f6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf9f6-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf9f6-124">PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="bf9f6-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf9f6-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf9f6-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf9f6-127">PublishPrinters</span><span class="sxs-lookup"><span data-stu-id="bf9f6-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf9f6-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bf9f6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf9f6-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bf9f6-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf9f6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf9f6-130">Requirements</span></span>



| <span data-ttu-id="bf9f6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf9f6-131">Requirement</span></span> | <span data-ttu-id="bf9f6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9f6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9f6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9f6-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf9f6-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf9f6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9f6-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9f6-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bf9f6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf9f6-137">Namespace</span></span><br/>                | <span data-ttu-id="bf9f6-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="bf9f6-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bf9f6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bf9f6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf9f6-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf9f6-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf9f6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9f6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9f6-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9f6-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

