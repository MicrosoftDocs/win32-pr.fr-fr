---
title: Classe MDM_Policy_Result01_Handwriting02
description: La \_ \_ classe Result01 Handwriting02 de la stratégie MDM \_ représente le mode par défaut pour le panneau d’écriture manuscrite.
ms.assetid: b21d0208-210d-476f-9269-f8d8a3307f17
keywords:
- Classe MDM_Policy_Result01_Handwriting02
- Classe MDM_Policy_Result01_Handwriting02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Handwriting02
- MDM_Policy_Result01_Handwriting02.InstanceID
- MDM_Policy_Result01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636dcfbb0d3bceaf60697d2aaa6e7f158a052bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104020"
---
# <a name="mdm_policy_result01_handwriting02-class"></a><span data-ttu-id="747b9-105">\_Classe Handwriting02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="747b9-105">MDM\_Policy\_Result01\_Handwriting02 class</span></span>

<span data-ttu-id="747b9-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="747b9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="747b9-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="747b9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="747b9-108">La \_ \_ classe Result01 Handwriting02 de la stratégie MDM \_ représente le mode par défaut pour le panneau d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="747b9-108">The MDM\_Policy\_Result01\_Handwriting02 class represents the default mode for the handwriting panel.</span></span>

<span data-ttu-id="747b9-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="747b9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="747b9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="747b9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="747b9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="747b9-111">Members</span></span>

<span data-ttu-id="747b9-112">La **classe \_ \_ Result01 \_ Handwriting02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="747b9-112">The **MDM\_Policy\_Result01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="747b9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="747b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="747b9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="747b9-114">Properties</span></span>

<span data-ttu-id="747b9-115">La **classe \_ \_ Result01 \_ Handwriting02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="747b9-115">The **MDM\_Policy\_Result01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="747b9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="747b9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="747b9-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="747b9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="747b9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="747b9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="747b9-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="747b9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="747b9-120">PanelDefaultModeDocked</span><span class="sxs-lookup"><span data-stu-id="747b9-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="747b9-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="747b9-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="747b9-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="747b9-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="747b9-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="747b9-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="747b9-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="747b9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="747b9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="747b9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="747b9-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="747b9-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="747b9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="747b9-127">Requirements</span></span>



| <span data-ttu-id="747b9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="747b9-128">Requirement</span></span> | <span data-ttu-id="747b9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="747b9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747b9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="747b9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="747b9-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="747b9-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="747b9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="747b9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="747b9-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="747b9-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="747b9-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="747b9-134">Namespace</span></span><br/>                | <span data-ttu-id="747b9-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="747b9-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="747b9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="747b9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="747b9-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="747b9-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="747b9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="747b9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="747b9-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="747b9-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

