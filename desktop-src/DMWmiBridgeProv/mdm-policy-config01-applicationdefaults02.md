---
title: Classe MDM_Policy_Config01_ApplicationDefaults02
description: La \_ \_ classe Config01 ApplicationDefaults02 de la stratégie MDM \_ permet à un administrateur de définir le type de fichier et les associations de protocole par défaut. Lorsque cette option est définie, les associations par défaut sont appliquées lors de la connexion au PC.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Classe MDM_Policy_Config01_ApplicationDefaults02
- Classe MDM_Policy_Config01_ApplicationDefaults02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464854"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="aca8f-106">\_Classe ApplicationDefaults02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="aca8f-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="aca8f-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="aca8f-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aca8f-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="aca8f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aca8f-109">La \_ \_ classe Config01 ApplicationDefaults02 de la stratégie MDM \_ permet à un administrateur de définir le type de fichier et les associations de protocole par défaut.</span><span class="sxs-lookup"><span data-stu-id="aca8f-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="aca8f-110">Lorsque cette option est définie, les associations par défaut sont appliquées lors de la connexion au PC.</span><span class="sxs-lookup"><span data-stu-id="aca8f-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="aca8f-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="aca8f-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca8f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aca8f-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="aca8f-113">Membres</span><span class="sxs-lookup"><span data-stu-id="aca8f-113">Members</span></span>

<span data-ttu-id="aca8f-114">La **classe \_ \_ Config01 \_ ApplicationDefaults02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aca8f-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="aca8f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aca8f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aca8f-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aca8f-116">Properties</span></span>

<span data-ttu-id="aca8f-117">La **classe \_ \_ Config01 \_ ApplicationDefaults02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="aca8f-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aca8f-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="aca8f-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aca8f-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aca8f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aca8f-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aca8f-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aca8f-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aca8f-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aca8f-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aca8f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aca8f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aca8f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aca8f-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aca8f-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aca8f-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="aca8f-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aca8f-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aca8f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aca8f-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aca8f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aca8f-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aca8f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aca8f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aca8f-129">Requirements</span></span>



| <span data-ttu-id="aca8f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aca8f-130">Requirement</span></span> | <span data-ttu-id="aca8f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="aca8f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca8f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aca8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aca8f-133">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aca8f-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aca8f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aca8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aca8f-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aca8f-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aca8f-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aca8f-136">Namespace</span></span><br/>                | <span data-ttu-id="aca8f-137">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="aca8f-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aca8f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="aca8f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aca8f-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aca8f-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aca8f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="aca8f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aca8f-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aca8f-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

