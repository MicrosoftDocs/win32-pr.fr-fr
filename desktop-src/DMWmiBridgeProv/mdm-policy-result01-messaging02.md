---
title: Classe MDM_Policy_Result01_Messaging02
description: La \_ classe Result01 Messaging02 de la stratégie MDM \_ \_ représente le message texte sauvegarder et restaurer et la messagerie partout.
ms.assetid: cdc92999-3a2b-4653-b64f-79e19abe5559
keywords:
- Classe MDM_Policy_Result01_Messaging02
- Classe MDM_Policy_Result01_Messaging02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Messaging02
- MDM_Policy_Result01_Messaging02.InstanceID
- MDM_Policy_Result01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd0eda84b9e2492243b2af85457450b0e443a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942013"
---
# <a name="mdm_policy_result01_messaging02-class"></a><span data-ttu-id="bc9be-105">\_Classe Messaging02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="bc9be-105">MDM\_Policy\_Result01\_Messaging02 class</span></span>

<span data-ttu-id="bc9be-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bc9be-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc9be-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bc9be-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc9be-108">La \_ classe Result01 Messaging02 de la stratégie MDM \_ \_ représente le message texte sauvegarder et restaurer et la messagerie partout.</span><span class="sxs-lookup"><span data-stu-id="bc9be-108">The MDM\_Policy\_Result01\_Messaging02 class represents the text message back up and restore and Messaging Everywhere.</span></span>

<span data-ttu-id="bc9be-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bc9be-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9be-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc9be-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="bc9be-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bc9be-111">Members</span></span>

<span data-ttu-id="bc9be-112">La **classe \_ \_ Result01 \_ Messaging02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc9be-112">The **MDM\_Policy\_Result01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc9be-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc9be-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc9be-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc9be-114">Properties</span></span>

<span data-ttu-id="bc9be-115">La **classe \_ \_ Result01 \_ Messaging02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bc9be-115">The **MDM\_Policy\_Result01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc9be-116">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="bc9be-116">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9be-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc9be-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc9be-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bc9be-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc9be-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc9be-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9be-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc9be-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc9be-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc9be-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc9be-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc9be-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc9be-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="bc9be-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc9be-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bc9be-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc9be-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bc9be-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc9be-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc9be-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc9be-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc9be-127">Requirements</span></span>



| <span data-ttu-id="bc9be-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc9be-128">Requirement</span></span> | <span data-ttu-id="bc9be-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc9be-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9be-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc9be-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9be-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc9be-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc9be-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc9be-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9be-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc9be-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc9be-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bc9be-134">Namespace</span></span><br/>                | <span data-ttu-id="bc9be-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="bc9be-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc9be-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bc9be-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc9be-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc9be-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc9be-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bc9be-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc9be-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc9be-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

