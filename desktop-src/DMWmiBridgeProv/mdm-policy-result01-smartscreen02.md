---
title: Classe MDM_Policy_Result01_SmartScreen02
description: La \_ classe SmartScreen02 de la stratégie MDM \_ Result01 \_ représente les stratégies d’écran intelligent.
ms.assetid: 9a775712-ce42-48c2-b286-eaf7ca8fed20
keywords:
- Classe MDM_Policy_Result01_SmartScreen02
- Classe MDM_Policy_Result01_SmartScreen02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_SmartScreen02
- MDM_Policy_Result01_SmartScreen02.InstanceID
- MDM_Policy_Result01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a49aad764492c54b43327cfb71c0c93fa36870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106228"
---
# <a name="mdm_policy_result01_smartscreen02-class"></a><span data-ttu-id="64597-105">\_Classe SmartScreen02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="64597-105">MDM\_Policy\_Result01\_SmartScreen02 class</span></span>

<span data-ttu-id="64597-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="64597-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="64597-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="64597-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="64597-108">la \_ classe SmartScreen02 de la stratégie MDM \_ Result01 \_ représente les stratégies d’écran intelligent.</span><span class="sxs-lookup"><span data-stu-id="64597-108">the MDM\_Policy\_Result01\_SmartScreen02 class represents the smart screen policies.</span></span>

<span data-ttu-id="64597-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="64597-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64597-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64597-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="64597-111">Membres</span><span class="sxs-lookup"><span data-stu-id="64597-111">Members</span></span>

<span data-ttu-id="64597-112">La **classe \_ \_ Result01 \_ SmartScreen02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="64597-112">The **MDM\_Policy\_Result01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="64597-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="64597-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64597-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="64597-114">Properties</span></span>

<span data-ttu-id="64597-115">La **classe \_ \_ Result01 \_ SmartScreen02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="64597-115">The **MDM\_Policy\_Result01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="64597-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="64597-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64597-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="64597-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64597-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64597-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64597-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="64597-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64597-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="64597-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64597-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64597-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64597-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="64597-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64597-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="64597-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64597-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="64597-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64597-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64597-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64597-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="64597-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64597-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="64597-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64597-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="64597-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64597-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64597-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64597-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="64597-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64597-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="64597-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64597-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="64597-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64597-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64597-133">Requirements</span></span>



| <span data-ttu-id="64597-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64597-134">Requirement</span></span> | <span data-ttu-id="64597-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="64597-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64597-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64597-136">Minimum supported client</span></span><br/> | <span data-ttu-id="64597-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64597-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64597-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64597-138">Minimum supported server</span></span><br/> | <span data-ttu-id="64597-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="64597-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="64597-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="64597-140">Namespace</span></span><br/>                | <span data-ttu-id="64597-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="64597-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="64597-142">MOF</span><span class="sxs-lookup"><span data-stu-id="64597-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64597-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64597-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="64597-144">DLL</span><span class="sxs-lookup"><span data-stu-id="64597-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64597-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64597-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

