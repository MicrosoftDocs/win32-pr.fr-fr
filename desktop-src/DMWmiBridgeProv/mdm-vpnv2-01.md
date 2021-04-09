---
title: Classe MDM_VPNv2_01
description: La \_ classe MDM VPNv2 \_ 01 autorise la configuration du profil VPN de l’appareil.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- Classe MDM_VPNv2_01
- Classe MDM_VPNv2_01, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942288"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="fa2dd-105">\_Classe MDM VPNv2 \_ 01</span><span class="sxs-lookup"><span data-stu-id="fa2dd-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="fa2dd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fa2dd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fa2dd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fa2dd-108">La classe **MDM \_ VPNv2 \_ 01** autorise la configuration du profil VPN de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="fa2dd-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2dd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa2dd-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="fa2dd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fa2dd-111">Members</span></span>

<span data-ttu-id="fa2dd-112">La classe **MDM \_ VPNv2 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fa2dd-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fa2dd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa2dd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa2dd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa2dd-114">Properties</span></span>

<span data-ttu-id="fa2dd-115">La classe **MDM \_ VPNv2 \_ 01** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fa2dd-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="fa2dd-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa2dd-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="fa2dd-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa2dd-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="fa2dd-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa2dd-125">EdpModeId</span><span class="sxs-lookup"><span data-stu-id="fa2dd-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa2dd-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa2dd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa2dd-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa2dd-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="fa2dd-133">Pour cette classe, la chaîne est le nom du profil VPN.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="fa2dd-134">Verrouillage</span><span class="sxs-lookup"><span data-stu-id="fa2dd-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa2dd-137">**ID**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa2dd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa2dd-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa2dd-141">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fa2dd-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="fa2dd-142">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2 »</span><span class="sxs-lookup"><span data-stu-id="fa2dd-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="fa2dd-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="fa2dd-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa2dd-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="fa2dd-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa2dd-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="fa2dd-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa2dd-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fa2dd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa2dd-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fa2dd-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa2dd-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa2dd-152">Requirements</span></span>



| <span data-ttu-id="fa2dd-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa2dd-153">Requirement</span></span> | <span data-ttu-id="fa2dd-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa2dd-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2dd-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa2dd-155">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2dd-156">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa2dd-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa2dd-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa2dd-157">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2dd-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa2dd-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fa2dd-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa2dd-159">Namespace</span></span><br/>                | <span data-ttu-id="fa2dd-160">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fa2dd-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fa2dd-161">MOF</span><span class="sxs-lookup"><span data-stu-id="fa2dd-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa2dd-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa2dd-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa2dd-163">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2dd-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2dd-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2dd-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa2dd-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa2dd-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2dd-166">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="fa2dd-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

