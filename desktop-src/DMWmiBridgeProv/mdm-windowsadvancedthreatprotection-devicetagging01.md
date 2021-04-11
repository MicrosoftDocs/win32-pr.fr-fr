---
title: Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: La \_ classe WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM est utilisée pour intégrer, déterminer l’état de configuration et d’intégrité et les points de terminaison annuler pour Windows Defender-protection avancée contre les menaces.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01, Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104944"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="f5b39-105">\_ \_ Classe DEVICETAGGING01 WindowsAdvancedThreatProtection MDM</span><span class="sxs-lookup"><span data-stu-id="f5b39-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="f5b39-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f5b39-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f5b39-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f5b39-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f5b39-108">La \_ classe WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM est utilisée pour intégrer, déterminer l’état de configuration et d’intégrité et les points de terminaison annuler pour Windows Defender-protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="f5b39-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="f5b39-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f5b39-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b39-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5b39-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="f5b39-111">Membres</span><span class="sxs-lookup"><span data-stu-id="f5b39-111">Members</span></span>

<span data-ttu-id="f5b39-112">La **classe \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f5b39-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="f5b39-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5b39-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5b39-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5b39-114">Properties</span></span>

<span data-ttu-id="f5b39-115">La **classe \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f5b39-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f5b39-116">Caractère critique</span><span class="sxs-lookup"><span data-stu-id="f5b39-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b39-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5b39-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f5b39-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5b39-119">Groupe</span><span class="sxs-lookup"><span data-stu-id="f5b39-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b39-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5b39-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f5b39-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f5b39-122">**IdMethod**</span><span class="sxs-lookup"><span data-stu-id="f5b39-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b39-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="f5b39-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f5b39-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f5b39-125">TBD</span><span class="sxs-lookup"><span data-stu-id="f5b39-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="f5b39-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f5b39-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b39-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5b39-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5b39-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5b39-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f5b39-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="f5b39-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b39-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f5b39-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5b39-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5b39-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5b39-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5b39-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5b39-134">Requirements</span></span>



| <span data-ttu-id="f5b39-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5b39-135">Requirement</span></span> | <span data-ttu-id="f5b39-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5b39-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b39-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5b39-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b39-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5b39-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5b39-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5b39-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b39-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5b39-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f5b39-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5b39-141">Namespace</span></span><br/>                | <span data-ttu-id="f5b39-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="f5b39-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="f5b39-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f5b39-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5b39-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5b39-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5b39-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b39-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b39-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b39-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

