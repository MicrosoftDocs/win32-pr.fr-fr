---
title: Classe MDM_DeviceStatus_NetworkIdentifiers01_01
description: La \_ classe MDM DeviceStatus \_ NetworkIdentifiers01 \_ 01 vous permet d’interroger un appareil à la recherche de propriétés réseau.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01
- Classe MDM_DeviceStatus_NetworkIdentifiers01_01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530c301894d957c9a9a2db374f35cf7c1bcb5063
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033087"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a><span data-ttu-id="06fdd-105">\_Classe DeviceStatus \_ NETWORKIDENTIFIERS01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="06fdd-105">MDM\_DeviceStatus\_NetworkIdentifiers01\_01 class</span></span>

<span data-ttu-id="06fdd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="06fdd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="06fdd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="06fdd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="06fdd-108">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** vous permet d’interroger un appareil à la recherche de propriétés réseau.</span><span class="sxs-lookup"><span data-stu-id="06fdd-108">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class allows you to query a device for network properties.</span></span>

<span data-ttu-id="06fdd-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="06fdd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fdd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06fdd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a><span data-ttu-id="06fdd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="06fdd-111">Members</span></span>

<span data-ttu-id="06fdd-112">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="06fdd-112">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="06fdd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06fdd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06fdd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06fdd-114">Properties</span></span>

<span data-ttu-id="06fdd-115">La classe **MDM \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="06fdd-115">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06fdd-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06fdd-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06fdd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06fdd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06fdd-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="06fdd-120">Nœud pour les requêtes sur les propriétés du réseau et de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="06fdd-120">Node for queries on network and device properties.</span></span>

</dd> <dt>

[<span data-ttu-id="06fdd-121">IPAddressV4</span><span class="sxs-lookup"><span data-stu-id="06fdd-121">IPAddressV4</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06fdd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="06fdd-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="06fdd-124">IPAddressV6</span><span class="sxs-lookup"><span data-stu-id="06fdd-124">IPAddressV6</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06fdd-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="06fdd-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="06fdd-127">IsConnected</span><span class="sxs-lookup"><span data-stu-id="06fdd-127">IsConnected</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="06fdd-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="06fdd-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06fdd-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="06fdd-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06fdd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06fdd-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06fdd-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="06fdd-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="06fdd-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="06fdd-135">Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »</span><span class="sxs-lookup"><span data-stu-id="06fdd-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="06fdd-136">Type</span><span class="sxs-lookup"><span data-stu-id="06fdd-136">Type</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06fdd-137">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="06fdd-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="06fdd-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="06fdd-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06fdd-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06fdd-139">Requirements</span></span>



| <span data-ttu-id="06fdd-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06fdd-140">Requirement</span></span> | <span data-ttu-id="06fdd-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="06fdd-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fdd-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06fdd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="06fdd-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06fdd-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06fdd-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06fdd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="06fdd-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06fdd-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="06fdd-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="06fdd-146">Namespace</span></span><br/>                | <span data-ttu-id="06fdd-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="06fdd-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="06fdd-148">MOF</span><span class="sxs-lookup"><span data-stu-id="06fdd-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06fdd-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06fdd-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="06fdd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="06fdd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06fdd-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06fdd-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fdd-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06fdd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fdd-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="06fdd-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

