---
title: Classe MDM_Policy_Config01_Messaging02
description: La \_ classe Config01 Messaging02 de la stratégie MDM \_ active la \_ sauvegarde et la restauration des messages texte et la messagerie partout. Cette stratégie permet à une organisation de désactiver ces fonctionnalités pour éviter que des informations soient stockées sur des serveurs en dehors de leur contrôle.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- Classe MDM_Policy_Config01_Messaging02
- Classe MDM_Policy_Config01_Messaging02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508546"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="e8c5e-106">\_Classe Messaging02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="e8c5e-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="e8c5e-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e8c5e-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8c5e-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e8c5e-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8c5e-109">La \_ classe Config01 Messaging02 de la stratégie MDM \_ active la \_ sauvegarde et la restauration des messages texte et la messagerie partout.</span><span class="sxs-lookup"><span data-stu-id="e8c5e-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="e8c5e-110">Cette stratégie permet à une organisation de désactiver ces fonctionnalités pour éviter que des informations soient stockées sur des serveurs en dehors de leur contrôle.</span><span class="sxs-lookup"><span data-stu-id="e8c5e-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="e8c5e-111">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e8c5e-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c5e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8c5e-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="e8c5e-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e8c5e-113">Members</span></span>

<span data-ttu-id="e8c5e-114">La **classe \_ \_ Config01 \_ Messaging02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e8c5e-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="e8c5e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8c5e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8c5e-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8c5e-116">Properties</span></span>

<span data-ttu-id="e8c5e-117">La **classe \_ \_ Config01 \_ Messaging02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8c5e-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e8c5e-118">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="e8c5e-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c5e-119">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e8c5e-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8c5e-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e8c5e-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8c5e-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8c5e-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c5e-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8c5e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8c5e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8c5e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8c5e-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8c5e-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8c5e-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="e8c5e-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8c5e-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8c5e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8c5e-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8c5e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8c5e-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8c5e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8c5e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8c5e-129">Requirements</span></span>



| <span data-ttu-id="e8c5e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8c5e-130">Requirement</span></span> | <span data-ttu-id="e8c5e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8c5e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c5e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8c5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c5e-133">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8c5e-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8c5e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8c5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c5e-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8c5e-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e8c5e-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e8c5e-136">Namespace</span></span><br/>                | <span data-ttu-id="e8c5e-137">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e8c5e-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e8c5e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e8c5e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8c5e-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8c5e-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8c5e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e8c5e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8c5e-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c5e-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

