---
title: Classe MDM_Firewall_Action04
description: La \_ classe Action04 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- Classe MDM_Firewall_Action04
- Classe MDM_Firewall_Action04, Description
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464866"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="37bfa-105">\_Classe Action04 du pare-feu MDM \_</span><span class="sxs-lookup"><span data-stu-id="37bfa-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="37bfa-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="37bfa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37bfa-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="37bfa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37bfa-108">La \_ classe Action04 du pare-feu MDM \_ est utilisée pour configurer les paramètres du pare-feu Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="37bfa-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="37bfa-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37bfa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bfa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37bfa-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="37bfa-111">Membres</span><span class="sxs-lookup"><span data-stu-id="37bfa-111">Members</span></span>

<span data-ttu-id="37bfa-112">La **classe \_ \_ Action04 du pare-feu MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37bfa-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="37bfa-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37bfa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37bfa-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37bfa-114">Properties</span></span>

<span data-ttu-id="37bfa-115">La **classe \_ \_ Action04 du pare-feu MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="37bfa-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37bfa-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37bfa-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37bfa-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37bfa-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37bfa-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="37bfa-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37bfa-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37bfa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37bfa-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="37bfa-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-125">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="37bfa-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37bfa-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37bfa-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37bfa-127">Requirements</span></span>



| <span data-ttu-id="37bfa-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37bfa-128">Requirement</span></span> | <span data-ttu-id="37bfa-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="37bfa-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bfa-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bfa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="37bfa-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37bfa-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37bfa-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bfa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="37bfa-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bfa-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="37bfa-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37bfa-134">Namespace</span></span><br/>                | <span data-ttu-id="37bfa-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="37bfa-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="37bfa-136">MOF</span><span class="sxs-lookup"><span data-stu-id="37bfa-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37bfa-137"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37bfa-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="37bfa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37bfa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37bfa-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37bfa-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

