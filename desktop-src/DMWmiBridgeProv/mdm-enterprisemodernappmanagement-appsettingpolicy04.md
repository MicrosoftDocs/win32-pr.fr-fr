---
title: Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: La \_ classe EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM spécifie toutes les valeurs de paramètre d’application gérée.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033084"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="4b3db-105">\_ \_ Classe APPSETTINGPOLICY04 EnterpriseModernAppManagement MDM</span><span class="sxs-lookup"><span data-stu-id="4b3db-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="4b3db-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4b3db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4b3db-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="4b3db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4b3db-108">La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** spécifie toutes les valeurs de paramètre d’application gérée.</span><span class="sxs-lookup"><span data-stu-id="4b3db-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="4b3db-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4b3db-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3db-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b3db-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="4b3db-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4b3db-111">Members</span></span>

<span data-ttu-id="4b3db-112">La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4b3db-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="4b3db-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b3db-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b3db-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4b3db-114">Properties</span></span>

<span data-ttu-id="4b3db-115">La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4b3db-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b3db-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4b3db-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b3db-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b3db-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b3db-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4b3db-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4b3db-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="4b3db-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="4b3db-121">Pour cette classe, la chaîne « AppSettingPolicy ».</span><span class="sxs-lookup"><span data-stu-id="4b3db-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="4b3db-122">IsVariableLeaf</span><span class="sxs-lookup"><span data-stu-id="4b3db-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b3db-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4b3db-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b3db-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b3db-125">Ajouté dans Windows 10, version 1511.</span><span class="sxs-lookup"><span data-stu-id="4b3db-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="4b3db-126">Les **SettingValue** et les données représentent une paire clé-valeur à configurer pour l’application.</span><span class="sxs-lookup"><span data-stu-id="4b3db-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="4b3db-127">Le nœud représente le nom de la clé et les données représentent la valeur.</span><span class="sxs-lookup"><span data-stu-id="4b3db-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="4b3db-128">Vous pouvez trouver cette valeur dans LocalSettings dans le conteneur Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="4b3db-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="4b3db-129">Ce paramètre ne fonctionne que pour les applications qui prennent en charge la fonctionnalité et qui sont uniquement prises en charge dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b3db-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="4b3db-130">**ID**</span><span class="sxs-lookup"><span data-stu-id="4b3db-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b3db-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b3db-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4b3db-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4b3db-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4b3db-134">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="4b3db-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="4b3db-135">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*»</span><span class="sxs-lookup"><span data-stu-id="4b3db-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="4b3db-136">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4b3db-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b3db-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b3db-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b3db-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4b3db-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b3db-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b3db-139">Requirements</span></span>



| <span data-ttu-id="4b3db-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b3db-140">Requirement</span></span> | <span data-ttu-id="4b3db-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b3db-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3db-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3db-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3db-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b3db-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b3db-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3db-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3db-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3db-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4b3db-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b3db-146">Namespace</span></span><br/>                | <span data-ttu-id="4b3db-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="4b3db-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4b3db-148">MOF</span><span class="sxs-lookup"><span data-stu-id="4b3db-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b3db-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b3db-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b3db-150">DLL</span><span class="sxs-lookup"><span data-stu-id="4b3db-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b3db-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b3db-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3db-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b3db-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3db-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="4b3db-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

