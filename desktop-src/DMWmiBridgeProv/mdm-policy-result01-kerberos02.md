---
title: Classe MDM_Policy_Result01_Kerberos02
description: La \_ classe Kerberos02 de la stratégie MDM \_ Result01 \_ représente les stratégies Kerberos.
ms.assetid: a628272d-723f-491a-a6a1-70514e5096ef
keywords:
- Classe MDM_Policy_Result01_Kerberos02
- Classe MDM_Policy_Result01_Kerberos02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Kerberos02
- MDM_Policy_Result01_Kerberos02.InstanceID
- MDM_Policy_Result01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713d7747fe45fa72cb7dcf44a02aa57526161c17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465015"
---
# <a name="mdm_policy_result01_kerberos02-class"></a><span data-ttu-id="6bf98-105">\_Classe Kerberos02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="6bf98-105">MDM\_Policy\_Result01\_Kerberos02 class</span></span>

<span data-ttu-id="6bf98-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="6bf98-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bf98-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="6bf98-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bf98-108">La \_ classe Kerberos02 de la stratégie MDM \_ Result01 \_ représente les stratégies Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6bf98-108">The MDM\_Policy\_Result01\_Kerberos02 class represents the Kerberos policies.</span></span>

<span data-ttu-id="6bf98-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6bf98-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf98-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bf98-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="6bf98-111">Membres</span><span class="sxs-lookup"><span data-stu-id="6bf98-111">Members</span></span>

<span data-ttu-id="6bf98-112">La **classe \_ \_ Result01 \_ Kerberos02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6bf98-112">The **MDM\_Policy\_Result01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="6bf98-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6bf98-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bf98-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6bf98-114">Properties</span></span>

<span data-ttu-id="6bf98-115">La **classe \_ \_ Result01 \_ Kerberos02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6bf98-115">The **MDM\_Policy\_Result01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6bf98-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="6bf98-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6bf98-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6bf98-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6bf98-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bf98-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6bf98-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6bf98-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="6bf98-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6bf98-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6bf98-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="6bf98-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6bf98-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6bf98-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6bf98-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="6bf98-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6bf98-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6bf98-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="6bf98-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6bf98-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6bf98-136">SetMaximumContextTokenSize</span><span class="sxs-lookup"><span data-stu-id="6bf98-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bf98-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6bf98-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bf98-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6bf98-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bf98-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bf98-139">Requirements</span></span>



| <span data-ttu-id="6bf98-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bf98-140">Requirement</span></span> | <span data-ttu-id="6bf98-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bf98-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf98-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bf98-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf98-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bf98-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bf98-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bf98-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf98-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bf98-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6bf98-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6bf98-146">Namespace</span></span><br/>                | <span data-ttu-id="6bf98-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="6bf98-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6bf98-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6bf98-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bf98-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bf98-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bf98-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf98-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf98-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bf98-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

