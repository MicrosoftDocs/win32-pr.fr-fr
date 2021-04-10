---
title: Classe MDM_PassportForWork_Biometrics01
description: La \_ \_ classe Biometrics01 MDM PassportForWork définit des paramètres biométriques.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- Classe MDM_PassportForWork_Biometrics01
- Classe MDM_PassportForWork_Biometrics01, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103329"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="eb4e6-105">\_ \_ Classe BIOMETRICS01 PassportForWork MDM</span><span class="sxs-lookup"><span data-stu-id="eb4e6-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="eb4e6-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb4e6-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="eb4e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb4e6-108">La **classe \_ \_ Biometrics01 MDM PassportForWork** définit des paramètres biométriques.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="eb4e6-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4e6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb4e6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="eb4e6-111">Membres</span><span class="sxs-lookup"><span data-stu-id="eb4e6-111">Members</span></span>

<span data-ttu-id="eb4e6-112">La **classe \_ PassportForWork \_ Biometrics01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb4e6-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="eb4e6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb4e6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb4e6-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb4e6-114">Properties</span></span>

<span data-ttu-id="eb4e6-115">La **classe \_ PassportForWork \_ Biometrics01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eb4e6-116">FacialFeaturesUseEnhancedAntiSpoofing</span><span class="sxs-lookup"><span data-stu-id="eb4e6-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb4e6-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb4e6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb4e6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb4e6-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb4e6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb4e6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb4e6-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="eb4e6-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb4e6-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb4e6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb4e6-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb4e6-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb4e6-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="eb4e6-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/PassportForWork/ »</span><span class="sxs-lookup"><span data-stu-id="eb4e6-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="eb4e6-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="eb4e6-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb4e6-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eb4e6-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb4e6-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb4e6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb4e6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb4e6-133">Requirements</span></span>



| <span data-ttu-id="eb4e6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb4e6-134">Requirement</span></span> | <span data-ttu-id="eb4e6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb4e6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4e6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb4e6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4e6-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb4e6-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb4e6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb4e6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4e6-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb4e6-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eb4e6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb4e6-140">Namespace</span></span><br/>                | <span data-ttu-id="eb4e6-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="eb4e6-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eb4e6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="eb4e6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb4e6-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb4e6-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb4e6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="eb4e6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb4e6-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4e6-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4e6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb4e6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4e6-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="eb4e6-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

