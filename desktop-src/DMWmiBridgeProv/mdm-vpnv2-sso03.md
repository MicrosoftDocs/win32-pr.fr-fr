---
title: Classe MDM_VPNv2_Sso03
description: La \_ \_ classe Sso03 MDM VPNv2 peut être utilisée pour sélectionner un certificat différent du certificat d’authentification VPN pour l’authentification Kerberos en cas de conformité de l’appareil.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- Classe MDM_VPNv2_Sso03
- Classe MDM_VPNv2_Sso03, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942520"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="ecaad-105">\_ \_ Classe SSO03 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="ecaad-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="ecaad-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ecaad-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ecaad-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="ecaad-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ecaad-108">La **classe \_ \_ Sso03 MDM VPNv2** peut être utilisée pour sélectionner un certificat différent du certificat d’authentification VPN pour l’authentification Kerberos en cas de conformité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ecaad-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="ecaad-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ecaad-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaad-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecaad-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="ecaad-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ecaad-111">Members</span></span>

<span data-ttu-id="ecaad-112">La **classe \_ VPNv2 \_ Sso03 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ecaad-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="ecaad-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecaad-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecaad-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecaad-114">Properties</span></span>

<span data-ttu-id="ecaad-115">La **classe \_ VPNv2 \_ Sso03 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ecaad-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ecaad-116">Extension</span><span class="sxs-lookup"><span data-stu-id="ecaad-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecaad-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecaad-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecaad-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ecaad-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="ecaad-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecaad-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ecaad-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecaad-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecaad-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ecaad-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecaad-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecaad-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecaad-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecaad-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecaad-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ecaad-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="ecaad-127">IssuerHash</span><span class="sxs-lookup"><span data-stu-id="ecaad-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecaad-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecaad-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ecaad-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ecaad-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="ecaad-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecaad-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ecaad-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ecaad-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ecaad-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ecaad-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ecaad-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ecaad-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="ecaad-135">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance »</span><span class="sxs-lookup"><span data-stu-id="ecaad-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecaad-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecaad-136">Requirements</span></span>



| <span data-ttu-id="ecaad-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecaad-137">Requirement</span></span> | <span data-ttu-id="ecaad-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecaad-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecaad-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecaad-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ecaad-140">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecaad-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecaad-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecaad-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ecaad-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecaad-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ecaad-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ecaad-143">Namespace</span></span><br/>                | <span data-ttu-id="ecaad-144">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="ecaad-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ecaad-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ecaad-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecaad-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecaad-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecaad-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ecaad-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecaad-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecaad-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecaad-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecaad-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecaad-150">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="ecaad-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

