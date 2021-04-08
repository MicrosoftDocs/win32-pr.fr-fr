---
title: Classe MDM_Policy_Config01_Games02
description: La \_ classe Config01 Games02 de la stratégie MDM \_ \_ configure les services de jeux avancés.
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- Classe MDM_Policy_Config01_Games02
- Classe MDM_Policy_Config01_Games02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033166"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="10079-105">\_Classe Games02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="10079-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="10079-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="10079-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="10079-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="10079-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="10079-108">La \_ classe Config01 Games02 de la stratégie MDM \_ \_ configure les services de jeux avancés.</span><span class="sxs-lookup"><span data-stu-id="10079-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="10079-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="10079-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10079-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10079-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="10079-111">Membres</span><span class="sxs-lookup"><span data-stu-id="10079-111">Members</span></span>

<span data-ttu-id="10079-112">La **classe \_ \_ Config01 \_ Games02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="10079-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="10079-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="10079-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10079-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="10079-114">Properties</span></span>

<span data-ttu-id="10079-115">La **classe \_ \_ Config01 \_ Games02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="10079-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="10079-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="10079-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="10079-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="10079-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="10079-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="10079-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10079-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="10079-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10079-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10079-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10079-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10079-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10079-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10079-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10079-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="10079-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10079-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="10079-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10079-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="10079-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10079-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10079-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10079-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10079-127">Requirements</span></span>



| <span data-ttu-id="10079-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10079-128">Requirement</span></span> | <span data-ttu-id="10079-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="10079-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10079-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10079-130">Minimum supported client</span></span><br/> | <span data-ttu-id="10079-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10079-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10079-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10079-132">Minimum supported server</span></span><br/> | <span data-ttu-id="10079-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="10079-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="10079-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="10079-134">Namespace</span></span><br/>                | <span data-ttu-id="10079-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="10079-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="10079-136">MOF</span><span class="sxs-lookup"><span data-stu-id="10079-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10079-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10079-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="10079-138">DLL</span><span class="sxs-lookup"><span data-stu-id="10079-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10079-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10079-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

