---
title: Classe MDM_Policy_Result01_CredentialsUI02
description: La \_ classe Result01 CredentialsUI02 de la stratégie MDM \_ \_ représente les stratégies d’informations d’identification disponibles.
ms.assetid: d50a4cc5-e87f-44a5-9345-744126615d04
keywords:
- Classe MDM_Policy_Result01_CredentialsUI02
- Classe MDM_Policy_Result01_CredentialsUI02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02.InstanceID
- MDM_Policy_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e444e36f2602fa30ca51601e6cd08e7fa8e30c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464642"
---
# <a name="mdm_policy_result01_credentialsui02-class"></a><span data-ttu-id="c4f0a-105">\_Classe CredentialsUI02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="c4f0a-105">MDM\_Policy\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="c4f0a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c4f0a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c4f0a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c4f0a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c4f0a-108">La \_ classe Result01 CredentialsUI02 de la stratégie MDM \_ \_ représente les stratégies d’informations d’identification disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4f0a-108">The MDM\_Policy\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="c4f0a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c4f0a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f0a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4f0a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="c4f0a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c4f0a-111">Members</span></span>

<span data-ttu-id="c4f0a-112">La **classe \_ \_ Result01 \_ CredentialsUI02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4f0a-112">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="c4f0a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4f0a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4f0a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4f0a-114">Properties</span></span>

<span data-ttu-id="c4f0a-115">La **classe \_ \_ Result01 \_ CredentialsUI02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c4f0a-115">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c4f0a-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="c4f0a-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f0a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4f0a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c4f0a-119">EnumerateAdministrators</span><span class="sxs-lookup"><span data-stu-id="c4f0a-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f0a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4f0a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4f0a-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f0a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4f0a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4f0a-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4f0a-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f0a-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4f0a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c4f0a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f0a-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4f0a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4f0a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4f0a-130">Requirements</span></span>



| <span data-ttu-id="c4f0a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4f0a-131">Requirement</span></span> | <span data-ttu-id="c4f0a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4f0a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f0a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4f0a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f0a-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4f0a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4f0a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4f0a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f0a-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4f0a-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c4f0a-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4f0a-137">Namespace</span></span><br/>                | <span data-ttu-id="c4f0a-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c4f0a-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c4f0a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c4f0a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4f0a-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4f0a-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4f0a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f0a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f0a-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f0a-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

