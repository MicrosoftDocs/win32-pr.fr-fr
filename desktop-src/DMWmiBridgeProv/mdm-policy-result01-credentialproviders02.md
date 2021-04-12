---
title: Classe MDM_Policy_Result01_CredentialProviders02
description: La \_ classe Result01 CredentialProviders02 de la stratégie MDM \_ \_ représente les stratégies de fournisseur d’informations d’identification disponibles.
ms.assetid: dc9e276b-8813-46cf-8e5a-0d41a93331ea
keywords:
- Classe MDM_Policy_Result01_CredentialProviders02
- Classe MDM_Policy_Result01_CredentialProviders02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialProviders02
- MDM_Policy_Result01_CredentialProviders02.InstanceID
- MDM_Policy_Result01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a2e6c0ababbf2706e82606ddb7c7c13a9087a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464643"
---
# <a name="mdm_policy_result01_credentialproviders02-class"></a><span data-ttu-id="18750-105">\_Classe CredentialProviders02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="18750-105">MDM\_Policy\_Result01\_CredentialProviders02 class</span></span>

<span data-ttu-id="18750-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="18750-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="18750-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="18750-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="18750-108">La \_ classe Result01 CredentialProviders02 de la stratégie MDM \_ \_ représente les stratégies de fournisseur d’informations d’identification disponibles.</span><span class="sxs-lookup"><span data-stu-id="18750-108">The MDM\_Policy\_Result01\_CredentialProviders02 class represents the available credential provider policies.</span></span>

<span data-ttu-id="18750-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18750-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18750-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18750-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="18750-111">Membres</span><span class="sxs-lookup"><span data-stu-id="18750-111">Members</span></span>

<span data-ttu-id="18750-112">La **classe \_ \_ Result01 \_ CredentialProviders02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18750-112">The **MDM\_Policy\_Result01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="18750-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18750-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18750-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18750-114">Properties</span></span>

<span data-ttu-id="18750-115">La **classe \_ \_ Result01 \_ CredentialProviders02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="18750-115">The **MDM\_Policy\_Result01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="18750-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="18750-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18750-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18750-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18750-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18750-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18750-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="18750-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18750-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18750-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18750-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18750-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="18750-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="18750-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18750-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="18750-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18750-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="18750-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18750-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18750-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18750-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18750-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18750-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18750-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18750-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18750-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18750-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="18750-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18750-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18750-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18750-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18750-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18750-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18750-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18750-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18750-133">Requirements</span></span>



| <span data-ttu-id="18750-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18750-134">Requirement</span></span> | <span data-ttu-id="18750-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="18750-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18750-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18750-136">Minimum supported client</span></span><br/> | <span data-ttu-id="18750-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18750-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18750-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18750-138">Minimum supported server</span></span><br/> | <span data-ttu-id="18750-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18750-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="18750-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18750-140">Namespace</span></span><br/>                | <span data-ttu-id="18750-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="18750-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="18750-142">MOF</span><span class="sxs-lookup"><span data-stu-id="18750-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18750-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18750-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18750-144">DLL</span><span class="sxs-lookup"><span data-stu-id="18750-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18750-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18750-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

