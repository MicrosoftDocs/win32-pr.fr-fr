---
title: Classe MDM_VPNv2_PluginProfile02
description: La \_ classe VPNv2 \_ PlugInProfile02 MDM décrit les informations nécessaires à l’utilisation d’un plug-in VPN basé sur Windows Store.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- Classe MDM_VPNv2_PluginProfile02
- Classe MDM_VPNv2_PluginProfile02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942139"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="cf4e7-105">\_ \_ Classe PLUGINPROFILE02 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="cf4e7-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="cf4e7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cf4e7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="cf4e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cf4e7-108">La **classe \_ VPNv2 \_ PlugInProfile02 MDM** décrit les informations nécessaires à l’utilisation d’un plug-in VPN basé sur Windows Store.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="cf4e7-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4e7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf4e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="cf4e7-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cf4e7-111">Members</span></span>

<span data-ttu-id="cf4e7-112">La **classe \_ VPNv2 \_ PluginProfile02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf4e7-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="cf4e7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf4e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf4e7-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf4e7-114">Properties</span></span>

<span data-ttu-id="cf4e7-115">La **classe \_ VPNv2 \_ PluginProfile02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cf4e7-116">CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf4e7-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf4e7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf4e7-119">CustomStoreUrl</span><span class="sxs-lookup"><span data-stu-id="cf4e7-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf4e7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf4e7-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf4e7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf4e7-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf4e7-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="cf4e7-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf4e7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf4e7-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf4e7-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="cf4e7-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="cf4e7-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»</span><span class="sxs-lookup"><span data-stu-id="cf4e7-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="cf4e7-133">PluginPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="cf4e7-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf4e7-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cf4e7-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="cf4e7-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4e7-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4e7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4e7-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cf4e7-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf4e7-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf4e7-139">Requirements</span></span>



| <span data-ttu-id="cf4e7-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf4e7-140">Requirement</span></span> | <span data-ttu-id="cf4e7-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf4e7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4e7-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4e7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4e7-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf4e7-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf4e7-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4e7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4e7-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4e7-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cf4e7-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf4e7-146">Namespace</span></span><br/>                | <span data-ttu-id="cf4e7-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="cf4e7-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cf4e7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="cf4e7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf4e7-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf4e7-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf4e7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cf4e7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf4e7-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf4e7-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4e7-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf4e7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4e7-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="cf4e7-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

