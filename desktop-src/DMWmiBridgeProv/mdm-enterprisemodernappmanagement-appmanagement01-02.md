---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 02 spécifie si vous souhaitez empêcher une application spécifique d’être mise à jour par le biais de mises à jour automatiques.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466203"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="af10c-105">\_Classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 02</span><span class="sxs-lookup"><span data-stu-id="af10c-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="af10c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="af10c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="af10c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="af10c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="af10c-108">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** spécifie si vous souhaitez empêcher une application spécifique d’être mise à jour par le biais de mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="af10c-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="af10c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="af10c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af10c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af10c-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="af10c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="af10c-111">Members</span></span>

<span data-ttu-id="af10c-112">La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="af10c-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="af10c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af10c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af10c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af10c-114">Properties</span></span>

<span data-ttu-id="af10c-115">La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="af10c-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="af10c-116">DoNotUpdate</span><span class="sxs-lookup"><span data-stu-id="af10c-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af10c-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="af10c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="af10c-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="af10c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af10c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="af10c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af10c-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af10c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af10c-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af10c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af10c-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af10c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="af10c-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="af10c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="af10c-124">Pour cette classe, la chaîne est l’instance du nom de la famille de packages.</span><span class="sxs-lookup"><span data-stu-id="af10c-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="af10c-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="af10c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af10c-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af10c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af10c-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af10c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af10c-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af10c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="af10c-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="af10c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="af10c-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*»</span><span class="sxs-lookup"><span data-stu-id="af10c-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af10c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af10c-131">Requirements</span></span>



| <span data-ttu-id="af10c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af10c-132">Requirement</span></span> | <span data-ttu-id="af10c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="af10c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af10c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af10c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="af10c-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af10c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af10c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af10c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="af10c-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="af10c-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="af10c-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af10c-138">Namespace</span></span><br/>                | <span data-ttu-id="af10c-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="af10c-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="af10c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="af10c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af10c-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af10c-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af10c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="af10c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af10c-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af10c-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af10c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af10c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af10c-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="af10c-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

