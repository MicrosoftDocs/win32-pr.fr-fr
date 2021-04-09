---
title: Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: La \_ classe MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 est utilisée pour gérer les licences pour les applications du Windows Store.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033083"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="cb2b5-105">\_Classe EnterpriseModernAppManagement \_ STORELICENSES02 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="cb2b5-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="cb2b5-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cb2b5-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="cb2b5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cb2b5-108">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** est utilisée pour gérer les licences pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="cb2b5-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2b5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb2b5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="cb2b5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cb2b5-111">Members</span></span>

<span data-ttu-id="cb2b5-112">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb2b5-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="cb2b5-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb2b5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb2b5-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb2b5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb2b5-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb2b5-115">Methods</span></span>

<span data-ttu-id="cb2b5-116">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="cb2b5-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb2b5-117">Method</span></span>                                                                                                              | <span data-ttu-id="cb2b5-118">Description</span><span class="sxs-lookup"><span data-stu-id="cb2b5-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="cb2b5-119">**AddLicenseMethod**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="cb2b5-120">Méthode pour ajouter une licence.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="cb2b5-121">**GetLicenseFromStoreMethod**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="cb2b5-122">Méthode permettant d’obtenir une licence du magasin.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb2b5-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb2b5-123">Properties</span></span>

<span data-ttu-id="cb2b5-124">La classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb2b5-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb2b5-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb2b5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb2b5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb2b5-129">Nœud facultatif.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-129">Optional node.</span></span> <span data-ttu-id="cb2b5-130">ID de licence pour une application du Store installée.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-130">License ID for a store installed app.</span></span> <span data-ttu-id="cb2b5-131">L’ID de licence est généralement le PFN de l’application.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="cb2b5-132">Les opérations prises en charge sont ajouter, récupérer et supprimer.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="cb2b5-133">LicenseCategory</span><span class="sxs-lookup"><span data-stu-id="cb2b5-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb2b5-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb2b5-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb2b5-136">LicenseUsage</span><span class="sxs-lookup"><span data-stu-id="cb2b5-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb2b5-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb2b5-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb2b5-139">**ID**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb2b5-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb2b5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-142">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb2b5-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb2b5-143">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="cb2b5-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="cb2b5-144">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses »</span><span class="sxs-lookup"><span data-stu-id="cb2b5-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="cb2b5-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="cb2b5-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb2b5-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cb2b5-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb2b5-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb2b5-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb2b5-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb2b5-148">Requirements</span></span>



| <span data-ttu-id="cb2b5-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb2b5-149">Requirement</span></span> | <span data-ttu-id="cb2b5-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb2b5-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2b5-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2b5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2b5-152">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb2b5-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb2b5-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2b5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2b5-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2b5-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cb2b5-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cb2b5-155">Namespace</span></span><br/>                | <span data-ttu-id="cb2b5-156">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="cb2b5-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cb2b5-157">MOF</span><span class="sxs-lookup"><span data-stu-id="cb2b5-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb2b5-158"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb2b5-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb2b5-159">DLL</span><span class="sxs-lookup"><span data-stu-id="cb2b5-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb2b5-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb2b5-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2b5-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb2b5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2b5-162">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="cb2b5-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

