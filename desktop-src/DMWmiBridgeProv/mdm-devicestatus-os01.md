---
title: Classe MDM_DeviceStatus_OS01
description: La \_ classe DeviceStatus \_ OS01 MDM est utilisée par l’entreprise pour interroger le système d’exploitation sur les appareils avec leurs stratégies d’entreprise.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Classe MDM_DeviceStatus_OS01
- Classe MDM_DeviceStatus_OS01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105001"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="84ef1-105">\_ \_ Classe OS01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="84ef1-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="84ef1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="84ef1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84ef1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="84ef1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84ef1-108">La **classe \_ DeviceStatus \_ OS01 MDM** est utilisée par l’entreprise pour interroger le système d’exploitation sur les appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="84ef1-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="84ef1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="84ef1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ef1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84ef1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="84ef1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="84ef1-111">Members</span></span>

<span data-ttu-id="84ef1-112">La **classe \_ DeviceStatus \_ OS01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84ef1-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="84ef1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84ef1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84ef1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84ef1-114">Properties</span></span>

<span data-ttu-id="84ef1-115">La **classe \_ DeviceStatus \_ OS01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="84ef1-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="84ef1-116">Édition</span><span class="sxs-lookup"><span data-stu-id="84ef1-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84ef1-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84ef1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84ef1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="84ef1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84ef1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84ef1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84ef1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84ef1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84ef1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84ef1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84ef1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84ef1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84ef1-123">Nœud de la requête du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="84ef1-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="84ef1-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="84ef1-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84ef1-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84ef1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84ef1-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84ef1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84ef1-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84ef1-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84ef1-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="84ef1-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="84ef1-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="84ef1-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84ef1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84ef1-130">Requirements</span></span>



| <span data-ttu-id="84ef1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84ef1-131">Requirement</span></span> | <span data-ttu-id="84ef1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="84ef1-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84ef1-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84ef1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="84ef1-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84ef1-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84ef1-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84ef1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="84ef1-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="84ef1-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84ef1-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84ef1-137">Namespace</span></span><br/>                | <span data-ttu-id="84ef1-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="84ef1-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="84ef1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="84ef1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84ef1-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84ef1-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84ef1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="84ef1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84ef1-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84ef1-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

