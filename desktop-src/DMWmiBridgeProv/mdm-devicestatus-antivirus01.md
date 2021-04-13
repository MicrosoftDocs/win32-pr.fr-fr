---
title: Classe MDM_DeviceStatus_Antivirus01
description: La \_ classe DeviceStatus \_ Antivirus01 MDM est utilisée par l’entreprise pour interroger l’état de conformité antivirus des appareils avec leurs stratégies d’entreprise.
ms.assetid: 8b3145a6-b836-4750-a0c3-88472f9a12c5
keywords:
- Classe MDM_DeviceStatus_Antivirus01
- Classe MDM_DeviceStatus_Antivirus01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antivirus01
- MDM_DeviceStatus_Antivirus01.InstanceID
- MDM_DeviceStatus_Antivirus01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3197dddb9bea498de63d08a025050963d4348054
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466215"
---
# <a name="mdm_devicestatus_antivirus01-class"></a><span data-ttu-id="02d6c-105">\_ \_ Classe ANTIVIRUS01 DeviceStatus MDM</span><span class="sxs-lookup"><span data-stu-id="02d6c-105">MDM\_DeviceStatus\_Antivirus01 class</span></span>

<span data-ttu-id="02d6c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="02d6c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="02d6c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="02d6c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="02d6c-108">La **classe \_ DeviceStatus \_ Antivirus01 MDM** est utilisée par l’entreprise pour interroger l’état de conformité antivirus des appareils avec leurs stratégies d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="02d6c-108">The **MDM\_DeviceStatus\_Antivirus01** class is used by the enterprise to query the state of antivirus compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="02d6c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="02d6c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d6c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02d6c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antivirus01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="02d6c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="02d6c-111">Members</span></span>

<span data-ttu-id="02d6c-112">La **classe \_ DeviceStatus \_ Antivirus01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="02d6c-112">The **MDM\_DeviceStatus\_Antivirus01** class has these types of members:</span></span>

-   [<span data-ttu-id="02d6c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="02d6c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02d6c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="02d6c-114">Properties</span></span>

<span data-ttu-id="02d6c-115">La **classe \_ DeviceStatus \_ Antivirus01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="02d6c-115">The **MDM\_DeviceStatus\_Antivirus01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02d6c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="02d6c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6c-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02d6c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02d6c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02d6c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02d6c-120">Nœud de la requête antivirus.</span><span class="sxs-lookup"><span data-stu-id="02d6c-120">Node for the antivirus query.</span></span>

</dd> <dt>

<span data-ttu-id="02d6c-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="02d6c-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02d6c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02d6c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02d6c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02d6c-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="02d6c-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="02d6c-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="02d6c-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="02d6c-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="02d6c-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6c-128">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d6c-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="02d6c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02d6c-130">État</span><span class="sxs-lookup"><span data-stu-id="02d6c-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6c-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="02d6c-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02d6c-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="02d6c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02d6c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02d6c-133">Requirements</span></span>



| <span data-ttu-id="02d6c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02d6c-134">Requirement</span></span> | <span data-ttu-id="02d6c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="02d6c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d6c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="02d6c-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02d6c-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02d6c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="02d6c-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="02d6c-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02d6c-140">Namespace</span></span><br/>                | <span data-ttu-id="02d6c-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="02d6c-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="02d6c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="02d6c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02d6c-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="02d6c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="02d6c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02d6c-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

