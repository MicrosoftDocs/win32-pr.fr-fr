---
title: Classe MDM_Policy_Config01_Location02
description: La \_ \_ classe Location02 de la stratégie MDM Config01 \_ configure le service d’emplacement de l’appareil.
ms.assetid: 8a40628e-1167-45ed-89bf-f3383dfb08d4
keywords:
- Classe MDM_Policy_Config01_Location02
- Classe MDM_Policy_Config01_Location02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Location02
- MDM_Policy_Config01_Location02.InstanceID
- MDM_Policy_Config01_Location02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ced896905395d577546630ff97e4eff45719773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843553"
---
# <a name="mdm_policy_config01_location02-class"></a><span data-ttu-id="50185-105">\_Classe Location02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="50185-105">MDM\_Policy\_Config01\_Location02 class</span></span>

<span data-ttu-id="50185-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="50185-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="50185-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="50185-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="50185-108">La \_ \_ classe Location02 de la stratégie MDM Config01 \_ configure le service d’emplacement de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="50185-108">The MDM\_Policy\_Config01\_Location02 class configures the location service of the device.</span></span>

<span data-ttu-id="50185-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="50185-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="50185-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50185-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Location02
{
  string InstanceID;
  string ParentID;
  sint32 EnableLocation;
};
```

## <a name="members"></a><span data-ttu-id="50185-111">Membres</span><span class="sxs-lookup"><span data-stu-id="50185-111">Members</span></span>

<span data-ttu-id="50185-112">La **classe \_ \_ Config01 \_ Location02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="50185-112">The **MDM\_Policy\_Config01\_Location02** class has these types of members:</span></span>

-   [<span data-ttu-id="50185-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50185-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50185-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50185-114">Properties</span></span>

<span data-ttu-id="50185-115">La **classe \_ \_ Config01 \_ Location02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="50185-115">The **MDM\_Policy\_Config01\_Location02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50185-116">**EnableLocation**</span><span class="sxs-lookup"><span data-stu-id="50185-116">**EnableLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50185-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="50185-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="50185-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50185-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="50185-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="50185-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50185-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="50185-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50185-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50185-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50185-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="50185-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="50185-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="50185-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50185-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="50185-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50185-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50185-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50185-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="50185-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50185-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50185-127">Requirements</span></span>



| <span data-ttu-id="50185-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50185-128">Requirement</span></span> | <span data-ttu-id="50185-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="50185-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50185-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50185-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50185-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50185-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50185-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50185-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50185-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="50185-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="50185-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="50185-134">Namespace</span></span><br/>                | <span data-ttu-id="50185-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="50185-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="50185-136">MOF</span><span class="sxs-lookup"><span data-stu-id="50185-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50185-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50185-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="50185-138">DLL</span><span class="sxs-lookup"><span data-stu-id="50185-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50185-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50185-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

