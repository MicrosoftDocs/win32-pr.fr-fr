---
title: Classe MDM_VPNv2_Certificate04
description: Réservé pour une utilisation ultérieure.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- Classe MDM_VPNv2_Certificate04
- Classe MDM_VPNv2_Certificate04, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942142"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="eb34a-105">\_ \_ Classe CERTIFICATE04 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="eb34a-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="eb34a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="eb34a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb34a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="eb34a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb34a-108">Réservé pour un usage ultérieur</span><span class="sxs-lookup"><span data-stu-id="eb34a-108">Reserved for future Use</span></span>

<span data-ttu-id="eb34a-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eb34a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb34a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb34a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="eb34a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="eb34a-111">Members</span></span>

<span data-ttu-id="eb34a-112">La **classe \_ VPNv2 \_ Certificate04 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb34a-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="eb34a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb34a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb34a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb34a-114">Properties</span></span>

<span data-ttu-id="eb34a-115">La **classe \_ VPNv2 \_ Certificate04 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="eb34a-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eb34a-116">Extension</span><span class="sxs-lookup"><span data-stu-id="eb34a-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb34a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb34a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb34a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb34a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb34a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb34a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb34a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb34a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb34a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb34a-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb34a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="eb34a-124">Pour cette classe, la chaîne est « EAP ».</span><span class="sxs-lookup"><span data-stu-id="eb34a-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="eb34a-125">Émetteur</span><span class="sxs-lookup"><span data-stu-id="eb34a-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb34a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb34a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb34a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb34a-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="eb34a-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb34a-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb34a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eb34a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb34a-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb34a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb34a-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="eb34a-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="eb34a-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication »</span><span class="sxs-lookup"><span data-stu-id="eb34a-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb34a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb34a-134">Requirements</span></span>



| <span data-ttu-id="eb34a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb34a-135">Requirement</span></span> | <span data-ttu-id="eb34a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb34a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb34a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb34a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eb34a-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb34a-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb34a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb34a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eb34a-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb34a-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eb34a-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb34a-141">Namespace</span></span><br/>                | <span data-ttu-id="eb34a-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="eb34a-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eb34a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="eb34a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb34a-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb34a-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb34a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="eb34a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb34a-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb34a-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb34a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb34a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb34a-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="eb34a-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

