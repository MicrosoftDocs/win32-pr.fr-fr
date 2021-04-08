---
title: Classe MDM_DeviceStatus_CellularIdentities01_01
description: La \_ classe MDM DeviceStatus \_ CellularIdentities01 \_ 01 vous permet de demander si l’appareil est conforme à la stratégie de chiffrement d’entreprise.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- Classe MDM_DeviceStatus_CellularIdentities01_01
- Classe MDM_DeviceStatus_CellularIdentities01_01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843965"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="22b45-105">\_Classe DeviceStatus \_ CELLULARIDENTITIES01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="22b45-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="22b45-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="22b45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="22b45-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="22b45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="22b45-108">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** vous permet de demander si l’appareil est conforme à la stratégie de chiffrement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="22b45-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="22b45-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="22b45-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b45-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22b45-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="22b45-111">Membres</span><span class="sxs-lookup"><span data-stu-id="22b45-111">Members</span></span>

<span data-ttu-id="22b45-112">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="22b45-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="22b45-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="22b45-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22b45-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="22b45-114">Properties</span></span>

<span data-ttu-id="22b45-115">La classe **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="22b45-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="22b45-116">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="22b45-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="22b45-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="22b45-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="22b45-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="22b45-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22b45-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22b45-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22b45-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22b45-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="22b45-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="22b45-129">Nœud pour les requêtes sur les cartes SIM.</span><span class="sxs-lookup"><span data-stu-id="22b45-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="22b45-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="22b45-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22b45-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22b45-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="22b45-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="22b45-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="22b45-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="22b45-135">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="22b45-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="22b45-136">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="22b45-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22b45-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="22b45-139">RoamingCompliance</span><span class="sxs-lookup"><span data-stu-id="22b45-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22b45-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="22b45-142">RoamingStatus</span><span class="sxs-lookup"><span data-stu-id="22b45-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="22b45-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22b45-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22b45-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="22b45-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22b45-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22b45-145">Requirements</span></span>



| <span data-ttu-id="22b45-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22b45-146">Requirement</span></span> | <span data-ttu-id="22b45-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="22b45-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b45-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22b45-148">Minimum supported client</span></span><br/> | <span data-ttu-id="22b45-149">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22b45-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22b45-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22b45-150">Minimum supported server</span></span><br/> | <span data-ttu-id="22b45-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="22b45-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="22b45-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22b45-152">Namespace</span></span><br/>                | <span data-ttu-id="22b45-153">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="22b45-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="22b45-154">MOF</span><span class="sxs-lookup"><span data-stu-id="22b45-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22b45-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22b45-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="22b45-156">DLL</span><span class="sxs-lookup"><span data-stu-id="22b45-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22b45-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22b45-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b45-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22b45-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b45-159">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="22b45-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

