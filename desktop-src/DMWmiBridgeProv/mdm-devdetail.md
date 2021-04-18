---
title: Classe MDM_DevDetail
description: La \_ classe MDM DevDetail gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- Classe MDM_DevDetail
- Classe MDM_DevDetail, Description
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512182"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="aa6d7-105">\_Classe DEVDETAIL MDM</span><span class="sxs-lookup"><span data-stu-id="aa6d7-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="aa6d7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aa6d7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="aa6d7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aa6d7-108">La classe **MDM \_ DevDetail** gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="aa6d7-109">Ces paramètres d’appareil ne sont pas envoyés automatiquement du client au serveur, mais ils peuvent être interrogés par des serveurs à l’aide de commandes de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="aa6d7-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6d7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa6d7-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="aa6d7-112">Membres</span><span class="sxs-lookup"><span data-stu-id="aa6d7-112">Members</span></span>

<span data-ttu-id="aa6d7-113">La **classe \_ DevDetail MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aa6d7-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="aa6d7-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa6d7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa6d7-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa6d7-115">Properties</span></span>

<span data-ttu-id="aa6d7-116">La **classe \_ DevDetail MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aa6d7-117">DevTyp</span><span class="sxs-lookup"><span data-stu-id="aa6d7-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa6d7-120">FwV</span><span class="sxs-lookup"><span data-stu-id="aa6d7-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa6d7-123">HwV</span><span class="sxs-lookup"><span data-stu-id="aa6d7-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aa6d7-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa6d7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa6d7-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa6d7-130">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="aa6d7-131">Pour cette classe, la chaîne est « DevDetail ».</span><span class="sxs-lookup"><span data-stu-id="aa6d7-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="aa6d7-132">LrgObj</span><span class="sxs-lookup"><span data-stu-id="aa6d7-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa6d7-135">FABRICANT</span><span class="sxs-lookup"><span data-stu-id="aa6d7-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aa6d7-138">**ID**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="aa6d7-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa6d7-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa6d7-142">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="aa6d7-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="aa6d7-143">SwV</span><span class="sxs-lookup"><span data-stu-id="aa6d7-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa6d7-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa6d7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa6d7-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="aa6d7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa6d7-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa6d7-146">Requirements</span></span>



| <span data-ttu-id="aa6d7-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa6d7-147">Requirement</span></span> | <span data-ttu-id="aa6d7-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa6d7-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6d7-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa6d7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6d7-150">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa6d7-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa6d7-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa6d7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6d7-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa6d7-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aa6d7-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aa6d7-153">Namespace</span></span><br/>                | <span data-ttu-id="aa6d7-154">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="aa6d7-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aa6d7-155">MOF</span><span class="sxs-lookup"><span data-stu-id="aa6d7-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa6d7-156"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa6d7-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa6d7-157">DLL</span><span class="sxs-lookup"><span data-stu-id="aa6d7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa6d7-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6d7-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa6d7-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa6d7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6d7-160">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="aa6d7-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

