---
title: Classe MDM_PassportForWork
description: Le \_ PASSPORTFORWORK MDM est utilisé pour approvisionner Windows Hello entreprise.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- Classe MDM_PassportForWork
- Classe MDM_PassportForWork, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032675"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="d7781-105">\_Classe PASSPORTFORWORK MDM</span><span class="sxs-lookup"><span data-stu-id="d7781-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="d7781-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d7781-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d7781-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d7781-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d7781-108">Le **\_ PassportForWork MDM** est utilisé pour approvisionner Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="d7781-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="d7781-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d7781-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7781-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7781-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="d7781-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d7781-111">Members</span></span>

<span data-ttu-id="d7781-112">La **classe \_ PassportForWork MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d7781-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="d7781-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7781-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7781-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7781-114">Properties</span></span>

<span data-ttu-id="d7781-115">La **classe \_ PassportForWork MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d7781-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7781-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d7781-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7781-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d7781-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7781-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7781-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7781-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7781-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7781-120">Spécifie l’ID de locataire sous la forme d’un identificateur global unique (GUID) sans accolades ({,}), qui sera utilisé dans le cadre de l’approvisionnement et de la gestion de Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="d7781-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="d7781-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="d7781-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7781-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d7781-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7781-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7781-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7781-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7781-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7781-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d7781-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d7781-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/PassPortForWork/ »</span><span class="sxs-lookup"><span data-stu-id="d7781-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="d7781-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="d7781-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7781-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d7781-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7781-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d7781-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7781-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7781-130">Requirements</span></span>



| <span data-ttu-id="d7781-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7781-131">Requirement</span></span> | <span data-ttu-id="d7781-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7781-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7781-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7781-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d7781-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7781-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7781-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7781-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d7781-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7781-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d7781-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d7781-137">Namespace</span></span><br/>                | <span data-ttu-id="d7781-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d7781-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d7781-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d7781-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7781-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7781-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7781-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d7781-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7781-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7781-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7781-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7781-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7781-144">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d7781-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

