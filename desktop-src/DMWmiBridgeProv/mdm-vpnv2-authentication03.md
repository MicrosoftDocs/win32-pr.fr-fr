---
title: Classe MDM_VPNv2_Authentication03
description: La \_ \_ classe Authentication03 MDM VPNv2 contient des informations d’authentification pour le profil VPN natif.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- Classe MDM_VPNv2_Authentication03
- Classe MDM_VPNv2_Authentication03, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032878"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="195e0-105">\_ \_ Classe AUTHENTICATION03 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="195e0-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="195e0-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="195e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="195e0-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="195e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="195e0-108">La [**classe \_ \_ Authentication03 MDM VPNv2**](mdm-vpnv2-01.md) contient des informations d’authentification pour le profil VPN natif.</span><span class="sxs-lookup"><span data-stu-id="195e0-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="195e0-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="195e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="195e0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="195e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="195e0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="195e0-111">Members</span></span>

<span data-ttu-id="195e0-112">La **classe \_ VPNv2 \_ Authentication03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="195e0-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="195e0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="195e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="195e0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="195e0-114">Properties</span></span>

<span data-ttu-id="195e0-115">La **classe \_ VPNv2 \_ Authentication03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="195e0-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="195e0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="195e0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="195e0-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="195e0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="195e0-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="195e0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="195e0-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="195e0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="195e0-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="195e0-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="195e0-121">MachineMethod</span><span class="sxs-lookup"><span data-stu-id="195e0-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="195e0-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="195e0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="195e0-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="195e0-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="195e0-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="195e0-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="195e0-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="195e0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="195e0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="195e0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="195e0-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="195e0-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="195e0-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="195e0-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="195e0-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile »</span><span class="sxs-lookup"><span data-stu-id="195e0-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="195e0-130">UserMethod</span><span class="sxs-lookup"><span data-stu-id="195e0-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="195e0-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="195e0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="195e0-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="195e0-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="195e0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="195e0-133">Requirements</span></span>



| <span data-ttu-id="195e0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="195e0-134">Requirement</span></span> | <span data-ttu-id="195e0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="195e0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="195e0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="195e0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="195e0-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="195e0-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="195e0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="195e0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="195e0-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="195e0-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="195e0-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="195e0-140">Namespace</span></span><br/>                | <span data-ttu-id="195e0-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="195e0-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="195e0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="195e0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="195e0-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="195e0-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="195e0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="195e0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="195e0-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="195e0-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195e0-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="195e0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195e0-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="195e0-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

