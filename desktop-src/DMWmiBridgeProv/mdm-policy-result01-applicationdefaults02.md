---
title: Classe MDM_Policy_Result01_ApplicationDefaults02
description: La \_ classe Result01 ApplicationDefaults02 de la stratégie MDM \_ \_ représente les stratégies de paramètres par défaut de l’application disponibles.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- Classe MDM_Policy_Result01_ApplicationDefaults02
- Classe MDM_Policy_Result01_ApplicationDefaults02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103885"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="3b413-105">\_Classe ApplicationDefaults02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="3b413-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="3b413-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3b413-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b413-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3b413-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b413-108">La \_ classe Result01 ApplicationDefaults02 de la stratégie MDM \_ \_ représente les stratégies de paramètres par défaut de l’application disponibles.</span><span class="sxs-lookup"><span data-stu-id="3b413-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="3b413-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b413-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b413-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b413-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="3b413-111">Membres</span><span class="sxs-lookup"><span data-stu-id="3b413-111">Members</span></span>

<span data-ttu-id="3b413-112">La **classe \_ \_ Result01 \_ ApplicationDefaults02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b413-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="3b413-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b413-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b413-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b413-114">Properties</span></span>

<span data-ttu-id="3b413-115">La **classe \_ \_ Result01 \_ ApplicationDefaults02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3b413-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b413-116">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b413-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b413-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b413-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b413-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b413-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b413-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b413-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b413-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b413-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b413-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b413-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b413-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b413-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b413-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="3b413-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b413-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b413-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b413-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b413-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b413-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b413-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b413-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b413-127">Requirements</span></span>



| <span data-ttu-id="3b413-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b413-128">Requirement</span></span> | <span data-ttu-id="3b413-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b413-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b413-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b413-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3b413-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b413-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b413-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b413-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3b413-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b413-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b413-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b413-134">Namespace</span></span><br/>                | <span data-ttu-id="3b413-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3b413-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3b413-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3b413-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b413-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b413-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b413-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3b413-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b413-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b413-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

