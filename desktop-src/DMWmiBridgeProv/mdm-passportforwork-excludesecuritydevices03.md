---
title: Classe MDM_PassportForWork_ExcludeSecurityDevices03
description: La \_ \_ classe ExcludeSecurityDevices03 MDM PassportForWork définit les modules de plateforme sécurisée autorisés à utiliser avec Windows Hello entreprise.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- Classe MDM_PassportForWork_ExcludeSecurityDevices03
- Classe MDM_PassportForWork_ExcludeSecurityDevices03, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032679"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="72da3-105">\_ \_ Classe EXCLUDESECURITYDEVICES03 PassportForWork MDM</span><span class="sxs-lookup"><span data-stu-id="72da3-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="72da3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="72da3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72da3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="72da3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72da3-108">La \_ \_ classe ExcludeSecurityDevices03 MDM PassportForWork définit les modules de plateforme sécurisée autorisés à utiliser avec Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="72da3-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="72da3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="72da3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72da3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72da3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="72da3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="72da3-111">Members</span></span>

<span data-ttu-id="72da3-112">La **classe \_ PassportForWork \_ ExcludeSecurityDevices03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="72da3-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="72da3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72da3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72da3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72da3-114">Properties</span></span>

<span data-ttu-id="72da3-115">La **classe \_ PassportForWork \_ ExcludeSecurityDevices03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="72da3-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72da3-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="72da3-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da3-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72da3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72da3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72da3-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72da3-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72da3-120">Nœud racine :</span><span class="sxs-lookup"><span data-stu-id="72da3-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="72da3-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="72da3-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da3-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72da3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da3-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72da3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72da3-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72da3-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72da3-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="72da3-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="72da3-126">Pour plus d’informations, consultez [PASSPORTFORWORK CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="72da3-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="72da3-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="72da3-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da3-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="72da3-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72da3-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72da3-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72da3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72da3-130">Requirements</span></span>



| <span data-ttu-id="72da3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72da3-131">Requirement</span></span> | <span data-ttu-id="72da3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="72da3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72da3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72da3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="72da3-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72da3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72da3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72da3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="72da3-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72da3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="72da3-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="72da3-137">Namespace</span></span><br/>                | <span data-ttu-id="72da3-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="72da3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="72da3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="72da3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72da3-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72da3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="72da3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="72da3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72da3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72da3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

