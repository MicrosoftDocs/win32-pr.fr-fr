---
title: Classe MDM_DeviceStatus_TPM01
description: La \_ classe DeviceStatus \_ TPM01 MDM est utilisée par l’entreprise pour interroger la version TPM des appareils avec leurs stratégies d’entreprise.
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- Classe MDM_DeviceStatus_TPM01
- Classe MDM_DeviceStatus_TPM01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843961"
---
# <a name="mdm_devicestatus_tpm01-class"></a><span data-ttu-id="f46f0-105">\_ \_ Classe TPM01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="f46f0-105">MDM\_DeviceStatus\_TPM01 class</span></span>

<span data-ttu-id="f46f0-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f46f0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f46f0-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f46f0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f46f0-108">La **classe \_ DeviceStatus \_ TPM01 MDM** est utilisée par l’entreprise pour interroger la version TPM des appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f46f0-108">The **MDM\_DeviceStatus\_TPM01** class is used by the enterprise to query the TPM version of devices with their enterprise policies.</span></span>

<span data-ttu-id="f46f0-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f46f0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f46f0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f46f0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a><span data-ttu-id="f46f0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="f46f0-111">Members</span></span>

<span data-ttu-id="f46f0-112">La **classe \_ DeviceStatus \_ TPM01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f46f0-112">The **MDM\_DeviceStatus\_TPM01** class has these types of members:</span></span>

-   [<span data-ttu-id="f46f0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f46f0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f46f0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f46f0-114">Properties</span></span>

<span data-ttu-id="f46f0-115">La **classe \_ DeviceStatus \_ TPM01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f46f0-115">The **MDM\_DeviceStatus\_TPM01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f46f0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f46f0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f46f0-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f46f0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f46f0-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f46f0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46f0-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f46f0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f46f0-120">Nœud de la requête TPM.</span><span class="sxs-lookup"><span data-stu-id="f46f0-120">Node for the TPM query.</span></span>

</dd> <dt>

<span data-ttu-id="f46f0-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="f46f0-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f46f0-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f46f0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f46f0-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f46f0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f46f0-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f46f0-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f46f0-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="f46f0-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="f46f0-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="f46f0-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="f46f0-127">SpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="f46f0-127">SpecificationVersion</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f46f0-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f46f0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f46f0-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f46f0-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f46f0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f46f0-130">Requirements</span></span>



| <span data-ttu-id="f46f0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f46f0-131">Requirement</span></span> | <span data-ttu-id="f46f0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f46f0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46f0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f46f0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f46f0-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f46f0-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f46f0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f46f0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f46f0-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f46f0-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f46f0-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f46f0-137">Namespace</span></span><br/>                | <span data-ttu-id="f46f0-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="f46f0-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f46f0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f46f0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f46f0-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f46f0-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f46f0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f46f0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f46f0-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f46f0-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

