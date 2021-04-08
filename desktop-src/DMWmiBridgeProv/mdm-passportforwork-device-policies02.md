---
title: Classe MDM_PassportForWork_Device_Policies02
description: La \_ \_ classe Policies02 de l’appareil MDM PassportForWork \_ définit les paramètres de la stratégie Windows Hello entreprise.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- Classe MDM_PassportForWork_Device_Policies02
- Classe MDM_PassportForWork_Device_Policies02, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941937"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="e3d7c-105">\_Classe de \_ Policies02 d’appareil PassportForWork MDM \_</span><span class="sxs-lookup"><span data-stu-id="e3d7c-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="e3d7c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e3d7c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e3d7c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e3d7c-108">La classe Policies02 de l' **\_ \_ appareil \_ MDM PassportForWork** définit les paramètres de la stratégie Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="e3d7c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d7c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3d7c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="e3d7c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e3d7c-111">Members</span></span>

<span data-ttu-id="e3d7c-112">La classe Policies02 de l' **\_ \_ appareil \_ PassportForWork MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3d7c-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="e3d7c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3d7c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3d7c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3d7c-114">Properties</span></span>

<span data-ttu-id="e3d7c-115">La classe Policies02 de l' **\_ \_ appareil \_ MDM PassportForWork** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3d7c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e3d7c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d7c-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e3d7c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d7c-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3d7c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d7c-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3d7c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3d7c-120">Nœud pour les paramètres de stratégie Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="e3d7c-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="e3d7c-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d7c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e3d7c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3d7c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e3d7c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d7c-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3d7c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3d7c-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e3d7c-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="e3d7c-126">Pour cette classe, la chaîne est « ./Device/Vendor/MSFT/PassPortForWork/*TenantID*/ »</span><span class="sxs-lookup"><span data-stu-id="e3d7c-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="e3d7c-127">UseCertificateForOnPremAuth</span><span class="sxs-lookup"><span data-stu-id="e3d7c-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d7c-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e3d7c-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3d7c-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e3d7c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3d7c-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3d7c-130">Requirements</span></span>



| <span data-ttu-id="e3d7c-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3d7c-131">Requirement</span></span> | <span data-ttu-id="e3d7c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3d7c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d7c-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d7c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d7c-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3d7c-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3d7c-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d7c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d7c-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3d7c-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e3d7c-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e3d7c-137">Namespace</span></span><br/>                | <span data-ttu-id="e3d7c-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e3d7c-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e3d7c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e3d7c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3d7c-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3d7c-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3d7c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e3d7c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3d7c-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3d7c-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

