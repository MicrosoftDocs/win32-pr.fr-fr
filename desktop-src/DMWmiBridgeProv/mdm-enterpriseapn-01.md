---
title: Classe MDM_EnterpriseAPN_01
description: La \_ classe MDM EnterpriseAPN \_ 01 est utilisée par l’entreprise pour approvisionner un APN pour Internet.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- Classe MDM_EnterpriseAPN_01
- Classe MDM_EnterpriseAPN_01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200563"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="1d3a8-105">\_Classe MDM EnterpriseAPN \_ 01</span><span class="sxs-lookup"><span data-stu-id="1d3a8-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="1d3a8-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d3a8-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1d3a8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d3a8-108">La classe **MDM \_ EnterpriseAPN \_ 01** est utilisée par l’entreprise pour approvisionner un APN pour Internet.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="1d3a8-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3a8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d3a8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="1d3a8-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1d3a8-111">Members</span></span>

<span data-ttu-id="1d3a8-112">La classe **MDM \_ EnterpriseAPN \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d3a8-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="1d3a8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d3a8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d3a8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1d3a8-114">Properties</span></span>

<span data-ttu-id="1d3a8-115">La classe **MDM \_ EnterpriseAPN \_ 01** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1d3a8-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="1d3a8-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-119">APNName</span><span class="sxs-lookup"><span data-stu-id="1d3a8-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="1d3a8-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-125">ClassId</span><span class="sxs-lookup"><span data-stu-id="1d3a8-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="1d3a8-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-131">IccId</span><span class="sxs-lookup"><span data-stu-id="1d3a8-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d3a8-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d3a8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d3a8-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d3a8-138">Nom de la connexion tel qu’il est vu par le gestionnaire de connexions Windows.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="1d3a8-139">IPType</span><span class="sxs-lookup"><span data-stu-id="1d3a8-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="1d3a8-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d3a8-145">**ID**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d3a8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-148">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d3a8-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d3a8-149">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="1d3a8-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="1d3a8-150">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseAPN »</span><span class="sxs-lookup"><span data-stu-id="1d3a8-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="1d3a8-151">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="1d3a8-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-154">Itinérance</span><span class="sxs-lookup"><span data-stu-id="1d3a8-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d3a8-157">UserName</span><span class="sxs-lookup"><span data-stu-id="1d3a8-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3a8-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d3a8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d3a8-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1d3a8-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d3a8-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d3a8-160">Requirements</span></span>



| <span data-ttu-id="1d3a8-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d3a8-161">Requirement</span></span> | <span data-ttu-id="1d3a8-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d3a8-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3a8-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d3a8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3a8-164">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d3a8-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d3a8-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d3a8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3a8-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d3a8-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1d3a8-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d3a8-167">Namespace</span></span><br/>                | <span data-ttu-id="1d3a8-168">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1d3a8-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1d3a8-169">MOF</span><span class="sxs-lookup"><span data-stu-id="1d3a8-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d3a8-170"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d3a8-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d3a8-171">DLL</span><span class="sxs-lookup"><span data-stu-id="1d3a8-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d3a8-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d3a8-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3a8-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d3a8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3a8-174">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="1d3a8-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

