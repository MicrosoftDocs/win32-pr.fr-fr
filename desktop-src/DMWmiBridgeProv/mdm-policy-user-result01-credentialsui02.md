---
title: Classe MDM_Policy_User_Result01_CredentialsUI02
description: La \_ \_ classe Result01 CredentialsUI02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’informations d’identification disponibles.
ms.assetid: e1df7798-676a-4846-89e5-2c05d0259086
keywords:
- Classe MDM_Policy_User_Result01_CredentialsUI02
- Classe MDM_Policy_User_Result01_CredentialsUI02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_CredentialsUI02
- MDM_Policy_User_Result01_CredentialsUI02.InstanceID
- MDM_Policy_User_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7659990ee980872059bd26b0a8b553202e6cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032905"
---
# <a name="mdm_policy_user_result01_credentialsui02-class"></a><span data-ttu-id="11873-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="11873-105">MDM\_Policy\_User\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="11873-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="11873-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11873-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="11873-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11873-108">La \_ \_ classe Result01 CredentialsUI02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’informations d’identification disponibles.</span><span class="sxs-lookup"><span data-stu-id="11873-108">The MDM\_Policy\_User\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="11873-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="11873-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11873-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11873-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="11873-111">Membres</span><span class="sxs-lookup"><span data-stu-id="11873-111">Members</span></span>

<span data-ttu-id="11873-112">La **classe \_ \_ \_ Result01 \_ CredentialsUI02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="11873-112">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="11873-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11873-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11873-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11873-114">Properties</span></span>

<span data-ttu-id="11873-115">La **classe \_ \_ \_ Result01 \_ CredentialsUI02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="11873-115">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11873-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="11873-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11873-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11873-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11873-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="11873-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11873-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11873-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11873-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11873-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11873-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11873-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11873-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11873-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11873-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="11873-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11873-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="11873-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11873-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="11873-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11873-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11873-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11873-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11873-127">Requirements</span></span>



| <span data-ttu-id="11873-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11873-128">Requirement</span></span> | <span data-ttu-id="11873-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="11873-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11873-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11873-130">Minimum supported client</span></span><br/> | <span data-ttu-id="11873-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11873-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11873-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11873-132">Minimum supported server</span></span><br/> | <span data-ttu-id="11873-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="11873-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11873-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11873-134">Namespace</span></span><br/>                | <span data-ttu-id="11873-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="11873-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11873-136">MOF</span><span class="sxs-lookup"><span data-stu-id="11873-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11873-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11873-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11873-138">DLL</span><span class="sxs-lookup"><span data-stu-id="11873-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11873-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11873-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

