---
title: Classe MDM_Policy_Result01_WiFi02
description: La \_ classe Result01 WiFi02 de la stratégie MDM \_ \_ représente les stratégies Wi-Fi disponibles.
ms.assetid: 074C4428-401D-4564-B7AC-45C2221EEC3A
keywords:
- Classe MDM_Policy_Result01_WiFi02
- Classe MDM_Policy_Result01_WiFi02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WiFi02
- MDM_Policy_Result01_WiFi02.InstanceID
- MDM_Policy_Result01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff9e0349f7a18da3320fab333d5b5fd36715999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941701"
---
# <a name="mdm_policy_result01_wifi02-class"></a><span data-ttu-id="668d2-105">\_Classe WiFi02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="668d2-105">MDM\_Policy\_Result01\_WiFi02 class</span></span>

<span data-ttu-id="668d2-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="668d2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="668d2-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="668d2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="668d2-108">La **classe \_ \_ Result01 \_ WiFi02 de la stratégie MDM** représente les stratégies Wi-Fi disponibles.</span><span class="sxs-lookup"><span data-stu-id="668d2-108">The **MDM\_Policy\_Result01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="668d2-109">Ces stratégies déterminent Wi-Fi configurations autorisées.</span><span class="sxs-lookup"><span data-stu-id="668d2-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="668d2-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="668d2-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="668d2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="668d2-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="668d2-112">Membres</span><span class="sxs-lookup"><span data-stu-id="668d2-112">Members</span></span>

<span data-ttu-id="668d2-113">La **classe \_ \_ Result01 \_ WiFi02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="668d2-113">The **MDM\_Policy\_Result01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="668d2-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="668d2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="668d2-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="668d2-115">Properties</span></span>

<span data-ttu-id="668d2-116">La **classe \_ \_ Result01 \_ WiFi02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="668d2-116">The **MDM\_Policy\_Result01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="668d2-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="668d2-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="668d2-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="668d2-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="668d2-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="668d2-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-124">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="668d2-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="668d2-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-127">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="668d2-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="668d2-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-130">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="668d2-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="668d2-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="668d2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="668d2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668d2-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="668d2-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="668d2-136">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="668d2-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="668d2-137">Pour cette classe, la chaîne est « WiFi ».</span><span class="sxs-lookup"><span data-stu-id="668d2-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="668d2-138">**ID**</span><span class="sxs-lookup"><span data-stu-id="668d2-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="668d2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="668d2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="668d2-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="668d2-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="668d2-142">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="668d2-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="668d2-143">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="668d2-143">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="668d2-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="668d2-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="668d2-145">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="668d2-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="668d2-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="668d2-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="668d2-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="668d2-147">Requirements</span></span>



| <span data-ttu-id="668d2-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="668d2-148">Requirement</span></span> | <span data-ttu-id="668d2-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="668d2-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668d2-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="668d2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="668d2-151">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="668d2-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="668d2-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="668d2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="668d2-153">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="668d2-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="668d2-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="668d2-154">Namespace</span></span><br/>                | <span data-ttu-id="668d2-155">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="668d2-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="668d2-156">MOF</span><span class="sxs-lookup"><span data-stu-id="668d2-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="668d2-157"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="668d2-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="668d2-158">DLL</span><span class="sxs-lookup"><span data-stu-id="668d2-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="668d2-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="668d2-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="668d2-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="668d2-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668d2-161">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="668d2-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

