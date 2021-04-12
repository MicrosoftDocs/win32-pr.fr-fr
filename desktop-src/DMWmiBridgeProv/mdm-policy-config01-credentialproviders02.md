---
title: Classe MDM_Policy_Config01_CredentialProviders02
description: La \_ classe Config01 CredentialProviders02 de la stratégie MDM \_ \_ configure les stratégies de fournisseur d’informations d’identification disponibles.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- Classe MDM_Policy_Config01_CredentialProviders02
- Classe MDM_Policy_Config01_CredentialProviders02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464847"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="2b968-105">\_Classe CredentialProviders02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="2b968-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="2b968-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="2b968-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2b968-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="2b968-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2b968-108">La \_ classe Config01 CredentialProviders02 de la stratégie MDM \_ \_ configure les stratégies de fournisseur d’informations d’identification disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b968-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="2b968-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2b968-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b968-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b968-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="2b968-111">Membres</span><span class="sxs-lookup"><span data-stu-id="2b968-111">Members</span></span>

<span data-ttu-id="2b968-112">La **classe \_ \_ Config01 \_ CredentialProviders02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b968-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="2b968-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b968-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b968-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b968-114">Properties</span></span>

<span data-ttu-id="2b968-115">La **classe \_ \_ Config01 \_ CredentialProviders02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b968-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2b968-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="2b968-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b968-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b968-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b968-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b968-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2b968-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="2b968-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b968-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b968-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b968-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b968-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2b968-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="2b968-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b968-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="2b968-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b968-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2b968-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b968-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2b968-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b968-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b968-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b968-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b968-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b968-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b968-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b968-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="2b968-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b968-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b968-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b968-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b968-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b968-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b968-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b968-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b968-133">Requirements</span></span>



| <span data-ttu-id="2b968-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b968-134">Requirement</span></span> | <span data-ttu-id="2b968-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b968-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b968-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b968-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2b968-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b968-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b968-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b968-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2b968-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b968-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2b968-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b968-140">Namespace</span></span><br/>                | <span data-ttu-id="2b968-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="2b968-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2b968-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2b968-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b968-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b968-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b968-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2b968-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b968-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b968-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

