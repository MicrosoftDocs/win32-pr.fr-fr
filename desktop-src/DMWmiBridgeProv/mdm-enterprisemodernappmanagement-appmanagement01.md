---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01
description: La \_ \_ classe AppManagement01 MDM EnterpriseModernAppManagement démarre l’analyse Windows Update et signale la dernière erreur d’analyse.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200561"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="a35e3-105">\_ \_ Classe APPMANAGEMENT01 EnterpriseModernAppManagement MDM</span><span class="sxs-lookup"><span data-stu-id="a35e3-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="a35e3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a35e3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a35e3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a35e3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a35e3-108">La **classe \_ \_ AppManagement01 MDM EnterpriseModernAppManagement** démarre l’analyse Windows Update et signale la dernière erreur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a35e3-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="a35e3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a35e3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35e3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a35e3-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="a35e3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a35e3-111">Members</span></span>

<span data-ttu-id="a35e3-112">La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a35e3-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="a35e3-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a35e3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a35e3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a35e3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a35e3-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a35e3-115">Methods</span></span>

<span data-ttu-id="a35e3-116">La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 MDM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a35e3-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="a35e3-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="a35e3-117">Method</span></span>                                                                                               | <span data-ttu-id="a35e3-118">Description</span><span class="sxs-lookup"><span data-stu-id="a35e3-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="a35e3-119">**RemovePackageMethod**</span><span class="sxs-lookup"><span data-stu-id="a35e3-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="a35e3-120">Méthode de suppression des packages.</span><span class="sxs-lookup"><span data-stu-id="a35e3-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="a35e3-121">**UpdateScanMethod**</span><span class="sxs-lookup"><span data-stu-id="a35e3-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="a35e3-122">Méthode de démarrage de l’analyse Windows Update.</span><span class="sxs-lookup"><span data-stu-id="a35e3-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a35e3-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a35e3-123">Properties</span></span>

<span data-ttu-id="a35e3-124">La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a35e3-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a35e3-125">AppInventoryQuery</span><span class="sxs-lookup"><span data-stu-id="a35e3-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a35e3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a35e3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a35e3-128">AppInventoryResults</span><span class="sxs-lookup"><span data-stu-id="a35e3-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a35e3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a35e3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a35e3-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a35e3-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a35e3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a35e3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a35e3-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a35e3-135">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a35e3-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="a35e3-136">Pour cette classe, la chaîne est « AppManagement ».</span><span class="sxs-lookup"><span data-stu-id="a35e3-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="a35e3-137">LastScanError</span><span class="sxs-lookup"><span data-stu-id="a35e3-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="a35e3-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a35e3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a35e3-140">**ID**</span><span class="sxs-lookup"><span data-stu-id="a35e3-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a35e3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a35e3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a35e3-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a35e3-144">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a35e3-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="a35e3-145">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/ »</span><span class="sxs-lookup"><span data-stu-id="a35e3-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="a35e3-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="a35e3-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35e3-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a35e3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35e3-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a35e3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a35e3-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a35e3-149">Requirements</span></span>



| <span data-ttu-id="a35e3-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a35e3-150">Requirement</span></span> | <span data-ttu-id="a35e3-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="a35e3-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a35e3-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a35e3-153">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a35e3-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a35e3-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a35e3-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a35e3-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a35e3-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a35e3-156">Namespace</span></span><br/>                | <span data-ttu-id="a35e3-157">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a35e3-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a35e3-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a35e3-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a35e3-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a35e3-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a35e3-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a35e3-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35e3-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a35e3-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35e3-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a35e3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35e3-163">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="a35e3-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

