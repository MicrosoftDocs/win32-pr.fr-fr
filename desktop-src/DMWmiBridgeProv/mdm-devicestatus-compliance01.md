---
title: Classe MDM_DeviceStatus_Compliance01
description: La \_ classe DeviceStatus \_ Compliance01 MDM vous permet de demander si l’appareil est conforme à la stratégie de chiffrement d’entreprise.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- Classe MDM_DeviceStatus_Compliance01
- Classe MDM_DeviceStatus_Compliance01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105007"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="4638d-105">\_ \_ Classe COMPLIANCE01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="4638d-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="4638d-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4638d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4638d-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="4638d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4638d-108">La **classe \_ DeviceStatus \_ Compliance01 MDM** vous permet de demander si l’appareil est conforme à la stratégie de chiffrement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4638d-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="4638d-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4638d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4638d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4638d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="4638d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4638d-111">Members</span></span>

<span data-ttu-id="4638d-112">La **classe \_ DeviceStatus \_ Compliance01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4638d-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="4638d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4638d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4638d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4638d-114">Properties</span></span>

<span data-ttu-id="4638d-115">La **classe \_ DeviceStatus \_ Compliance01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4638d-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4638d-116">EncryptionCompliance</span><span class="sxs-lookup"><span data-stu-id="4638d-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4638d-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4638d-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4638d-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4638d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4638d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4638d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4638d-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4638d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4638d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4638d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4638d-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4638d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4638d-123">Nœud pour les requêtes de conformité.</span><span class="sxs-lookup"><span data-stu-id="4638d-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="4638d-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="4638d-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4638d-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4638d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4638d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4638d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4638d-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4638d-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4638d-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="4638d-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="4638d-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="4638d-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4638d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4638d-130">Requirements</span></span>



| <span data-ttu-id="4638d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4638d-131">Requirement</span></span> | <span data-ttu-id="4638d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4638d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4638d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4638d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4638d-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4638d-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4638d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4638d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4638d-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4638d-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4638d-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4638d-137">Namespace</span></span><br/>                | <span data-ttu-id="4638d-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="4638d-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4638d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4638d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4638d-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4638d-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4638d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4638d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4638d-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4638d-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4638d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4638d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4638d-144">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="4638d-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

