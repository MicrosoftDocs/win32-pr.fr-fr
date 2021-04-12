---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03 fournit des informations spécifiques sur l’application, telles que le nom, la version et le serveur de publication.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104986"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="cf0bd-105">\_Classe EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM</span><span class="sxs-lookup"><span data-stu-id="cf0bd-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="cf0bd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cf0bd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="cf0bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cf0bd-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** fournit des informations spécifiques sur l’application, telles que le nom, la version et le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="cf0bd-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0bd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf0bd-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="cf0bd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cf0bd-111">Members</span></span>

<span data-ttu-id="cf0bd-112">La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf0bd-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="cf0bd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf0bd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf0bd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf0bd-114">Properties</span></span>

<span data-ttu-id="cf0bd-115">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cf0bd-116">Architecture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="cf0bd-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="cf0bd-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0bd-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf0bd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf0bd-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf0bd-129">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="cf0bd-130">Pour cette classe, la chaîne est l’instance du nom complet du package.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="cf0bd-131">IsBundle</span><span class="sxs-lookup"><span data-stu-id="cf0bd-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-134">IsFramework</span><span class="sxs-lookup"><span data-stu-id="cf0bd-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-137">IsProvisioned</span><span class="sxs-lookup"><span data-stu-id="cf0bd-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-140">Nom</span><span class="sxs-lookup"><span data-stu-id="cf0bd-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-143">PackageStatus</span><span class="sxs-lookup"><span data-stu-id="cf0bd-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0bd-146">**ID**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf0bd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-149">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf0bd-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf0bd-150">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="cf0bd-151">Pour cette classe, la chaîne est « ./Vendor/msft/EnterpriseModernAppManagement/AppManagement/*EnterpriseID* / *PackageFamilyName*»</span><span class="sxs-lookup"><span data-stu-id="cf0bd-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="cf0bd-152">Publisher</span><span class="sxs-lookup"><span data-stu-id="cf0bd-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-155">RequiresReinstall</span><span class="sxs-lookup"><span data-stu-id="cf0bd-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="cf0bd-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-161">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cf0bd-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf0bd-164">Version</span><span class="sxs-lookup"><span data-stu-id="cf0bd-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0bd-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf0bd-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0bd-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf0bd-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf0bd-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf0bd-167">Requirements</span></span>



| <span data-ttu-id="cf0bd-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf0bd-168">Requirement</span></span> | <span data-ttu-id="cf0bd-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf0bd-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0bd-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf0bd-170">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0bd-171">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf0bd-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf0bd-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf0bd-172">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0bd-173">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf0bd-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cf0bd-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf0bd-174">Namespace</span></span><br/>                | <span data-ttu-id="cf0bd-175">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="cf0bd-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cf0bd-176">MOF</span><span class="sxs-lookup"><span data-stu-id="cf0bd-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf0bd-177"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf0bd-178">DLL</span><span class="sxs-lookup"><span data-stu-id="cf0bd-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf0bd-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf0bd-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf0bd-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0bd-181">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="cf0bd-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

