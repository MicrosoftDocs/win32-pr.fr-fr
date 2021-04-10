---
title: Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 est utilisée pour installer des applications à partir du Windows Store ou d’un emplacement hébergé.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942524"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="e9854-105">\_Classe EnterpriseModernAppManagement \_ APPINSTALLATION01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="e9854-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="e9854-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e9854-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e9854-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e9854-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e9854-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** est utilisée pour installer des applications à partir du Windows Store ou d’un emplacement hébergé.</span><span class="sxs-lookup"><span data-stu-id="e9854-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="e9854-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e9854-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9854-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9854-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="e9854-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e9854-111">Members</span></span>

<span data-ttu-id="e9854-112">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9854-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e9854-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9854-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9854-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9854-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9854-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9854-115">Methods</span></span>

<span data-ttu-id="e9854-116">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e9854-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="e9854-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9854-117">Method</span></span>                                                                                                    | <span data-ttu-id="e9854-118">Description</span><span class="sxs-lookup"><span data-stu-id="e9854-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9854-119">**HostedInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="e9854-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="e9854-120">Méthode permettant d’effectuer l’installation d’un package d’application à partir d’un emplacement hébergé (il peut s’agir d’un lecteur local, d’une source de données UNC ou https).</span><span class="sxs-lookup"><span data-stu-id="e9854-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="e9854-121">**StoreInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="e9854-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="e9854-122">Méthode permettant d’effectuer l’installation d’une application et d’une licence à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e9854-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="e9854-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9854-123">Properties</span></span>

<span data-ttu-id="e9854-124">La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e9854-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9854-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e9854-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9854-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9854-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9854-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9854-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9854-129">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e9854-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="e9854-130">Pour cette classe, la chaîne est « AppInstallation ».</span><span class="sxs-lookup"><span data-stu-id="e9854-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="e9854-131">LastError</span><span class="sxs-lookup"><span data-stu-id="e9854-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9854-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e9854-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e9854-134">LastErrorDesc</span><span class="sxs-lookup"><span data-stu-id="e9854-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9854-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e9854-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e9854-137">**ID**</span><span class="sxs-lookup"><span data-stu-id="e9854-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9854-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9854-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9854-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9854-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9854-141">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e9854-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="e9854-142">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation »</span><span class="sxs-lookup"><span data-stu-id="e9854-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="e9854-143">ProgressStatus</span><span class="sxs-lookup"><span data-stu-id="e9854-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9854-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e9854-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e9854-146">État</span><span class="sxs-lookup"><span data-stu-id="e9854-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9854-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e9854-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9854-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e9854-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9854-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9854-149">Requirements</span></span>



| <span data-ttu-id="e9854-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9854-150">Requirement</span></span> | <span data-ttu-id="e9854-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9854-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9854-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9854-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e9854-153">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9854-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9854-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9854-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e9854-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9854-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e9854-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9854-156">Namespace</span></span><br/>                | <span data-ttu-id="e9854-157">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e9854-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e9854-158">MOF</span><span class="sxs-lookup"><span data-stu-id="e9854-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9854-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9854-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9854-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e9854-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9854-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9854-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9854-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9854-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9854-163">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="e9854-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

