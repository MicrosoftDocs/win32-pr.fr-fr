---
title: Classe MDM_RemoteFind_Location01
description: La \_ \_ classe LOCATION01 RemoteFind MDM récupère les informations d’emplacement pour un appareil particulier.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Classe MDM_RemoteFind_Location01
- Classe MDM_RemoteFind_Location01, Description
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464355"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="b6f47-105">\_ \_ Classe LOCATION01 RemoteFind MDM</span><span class="sxs-lookup"><span data-stu-id="b6f47-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="b6f47-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b6f47-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6f47-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b6f47-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6f47-108">La **classe \_ \_ Location01 RemoteFind MDM** récupère les informations d’emplacement pour un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="b6f47-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="b6f47-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b6f47-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f47-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6f47-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="b6f47-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b6f47-111">Members</span></span>

<span data-ttu-id="b6f47-112">La **classe \_ RemoteFind \_ Location01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6f47-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="b6f47-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6f47-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6f47-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6f47-114">Properties</span></span>

<span data-ttu-id="b6f47-115">La **classe \_ RemoteFind \_ Location01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b6f47-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b6f47-116">Précision</span><span class="sxs-lookup"><span data-stu-id="b6f47-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6f47-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6f47-119">Age</span><span class="sxs-lookup"><span data-stu-id="b6f47-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-120">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b6f47-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6f47-122">Altitude</span><span class="sxs-lookup"><span data-stu-id="b6f47-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-123">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b6f47-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6f47-125">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="b6f47-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6f47-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6f47-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b6f47-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b6f47-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b6f47-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6f47-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6f47-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b6f47-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="b6f47-133">Pour cette classe, la chaîne est « location ».</span><span class="sxs-lookup"><span data-stu-id="b6f47-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="b6f47-134">Latitude</span><span class="sxs-lookup"><span data-stu-id="b6f47-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-135">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b6f47-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6f47-137">Longitude</span><span class="sxs-lookup"><span data-stu-id="b6f47-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-138">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b6f47-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6f47-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6f47-140">**ID**</span><span class="sxs-lookup"><span data-stu-id="b6f47-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6f47-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b6f47-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b6f47-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6f47-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6f47-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6f47-144">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b6f47-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="b6f47-145">Pour cette classe, la chaîne est « ./Vendor/MSFT/RemoteFind »</span><span class="sxs-lookup"><span data-stu-id="b6f47-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6f47-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6f47-146">Requirements</span></span>



| <span data-ttu-id="b6f47-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6f47-147">Requirement</span></span> | <span data-ttu-id="b6f47-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6f47-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f47-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6f47-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f47-150">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6f47-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6f47-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6f47-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f47-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6f47-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b6f47-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6f47-153">Namespace</span></span><br/>                | <span data-ttu-id="b6f47-154">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b6f47-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b6f47-155">MOF</span><span class="sxs-lookup"><span data-stu-id="b6f47-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6f47-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6f47-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6f47-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b6f47-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6f47-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f47-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b6f47-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6f47-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f47-160">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="b6f47-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

