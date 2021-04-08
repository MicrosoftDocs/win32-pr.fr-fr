---
title: Classe MDM_DevDetail_Ext01
description: La \_ classe DevDetail \_ Ext01 MDM gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- Classe MDM_DevDetail_Ext01
- Classe MDM_DevDetail_Ext01, Description
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742636"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="e737e-105">\_ \_ Classe EXT01 DevDetail MDM</span><span class="sxs-lookup"><span data-stu-id="e737e-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="e737e-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e737e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e737e-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e737e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e737e-108">La **classe \_ DevDetail \_ Ext01 MDM** gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="e737e-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="e737e-109">Ces paramètres d’appareil ne sont pas envoyés automatiquement du client au serveur, mais ils peuvent être interrogés par des serveurs à l’aide de commandes de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="e737e-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="e737e-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e737e-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e737e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e737e-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="e737e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="e737e-112">Members</span></span>

<span data-ttu-id="e737e-113">La **classe \_ DevDetail \_ Ext01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e737e-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="e737e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e737e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e737e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e737e-115">Properties</span></span>

<span data-ttu-id="e737e-116">La **classe \_ DevDetail \_ Ext01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e737e-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e737e-117">DeviceHardwareData</span><span class="sxs-lookup"><span data-stu-id="e737e-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e737e-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e737e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e737e-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e737e-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e737e-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e737e-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e737e-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e737e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e737e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e737e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e737e-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e737e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e737e-124">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e737e-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="e737e-125">Pour cette classe, la chaîne est « ext ».</span><span class="sxs-lookup"><span data-stu-id="e737e-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="e737e-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="e737e-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e737e-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e737e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e737e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e737e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e737e-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e737e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e737e-130">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e737e-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="e737e-131">Pour cette classe, la chaîne est « ./DevDetail/ »</span><span class="sxs-lookup"><span data-stu-id="e737e-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="e737e-132">WLANMACAddress</span><span class="sxs-lookup"><span data-stu-id="e737e-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e737e-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e737e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e737e-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e737e-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e737e-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e737e-135">Requirements</span></span>



| <span data-ttu-id="e737e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e737e-136">Requirement</span></span> | <span data-ttu-id="e737e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e737e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e737e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e737e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e737e-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e737e-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e737e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e737e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e737e-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e737e-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e737e-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e737e-142">Namespace</span></span><br/>                | <span data-ttu-id="e737e-143">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e737e-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e737e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e737e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e737e-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e737e-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e737e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e737e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e737e-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e737e-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e737e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e737e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e737e-149">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="e737e-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

