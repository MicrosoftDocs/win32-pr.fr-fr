---
title: Classe MDM_VPNv2_APNBinding02
description: Réservé pour une utilisation ultérieure. | Classe MDM_VPNv2_APNBinding02
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- Classe MDM_VPNv2_APNBinding02
- Classe MDM_VPNv2_APNBinding02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321937"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="8bcf7-106">\_ \_ Classe APNBINDING02 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="8bcf7-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="8bcf7-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8bcf7-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8bcf7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8bcf7-109">Réservé pour un usage ultérieur</span><span class="sxs-lookup"><span data-stu-id="8bcf7-109">Reserved for Future Use</span></span>

<span data-ttu-id="8bcf7-110">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcf7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bcf7-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="8bcf7-112">Membres</span><span class="sxs-lookup"><span data-stu-id="8bcf7-112">Members</span></span>

<span data-ttu-id="8bcf7-113">La **classe \_ VPNv2 \_ APNBinding02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8bcf7-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="8bcf7-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bcf7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bcf7-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bcf7-115">Properties</span></span>

<span data-ttu-id="8bcf7-116">La **classe \_ VPNv2 \_ APNBinding02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf7-117">AccessPointName</span><span class="sxs-lookup"><span data-stu-id="8bcf7-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8bcf7-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8bcf7-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bcf7-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bcf7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8bcf7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8bcf7-127">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="8bcf7-128">IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="8bcf7-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bcf7-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bcf7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8bcf7-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8bcf7-135">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="8bcf7-136">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="8bcf7-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8bcf7-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="8bcf7-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8bcf7-142">UserName</span><span class="sxs-lookup"><span data-stu-id="8bcf7-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcf7-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcf7-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8bcf7-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bcf7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bcf7-145">Requirements</span></span>



| <span data-ttu-id="8bcf7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bcf7-146">Requirement</span></span> | <span data-ttu-id="8bcf7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bcf7-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcf7-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bcf7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcf7-149">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bcf7-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bcf7-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bcf7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcf7-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bcf7-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8bcf7-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8bcf7-152">Namespace</span></span><br/>                | <span data-ttu-id="8bcf7-153">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8bcf7-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8bcf7-154">MOF</span><span class="sxs-lookup"><span data-stu-id="8bcf7-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bcf7-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bcf7-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bcf7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8bcf7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bcf7-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bcf7-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bcf7-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bcf7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf7-159">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="8bcf7-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

