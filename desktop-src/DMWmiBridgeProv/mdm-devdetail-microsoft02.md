---
title: Classe MDM_DevDetail_Microsoft02
description: La \_ classe DevDetail \_ Microsoft02 MDM gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- Classe MDM_DevDetail_Microsoft02
- Classe MDM_DevDetail_Microsoft02, Description
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942530"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="c46c1-105">\_ \_ Classe MICROSOFT02 DevDetail MDM</span><span class="sxs-lookup"><span data-stu-id="c46c1-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="c46c1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c46c1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c46c1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c46c1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c46c1-108">La **classe \_ DevDetail \_ Microsoft02 MDM** gère l’objet de gestion qui fournit des paramètres spécifiques au périphérique au serveur de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="c46c1-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="c46c1-109">Ces paramètres d’appareil ne sont pas envoyés automatiquement du client au serveur, mais ils peuvent être interrogés par des serveurs à l’aide de commandes de DM OMA.</span><span class="sxs-lookup"><span data-stu-id="c46c1-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="c46c1-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c46c1-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46c1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c46c1-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="c46c1-112">Membres</span><span class="sxs-lookup"><span data-stu-id="c46c1-112">Members</span></span>

<span data-ttu-id="c46c1-113">La **classe \_ DevDetail \_ Microsoft02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c46c1-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="c46c1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c46c1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c46c1-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c46c1-115">Properties</span></span>

<span data-ttu-id="c46c1-116">La **classe \_ DevDetail \_ Microsoft02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c46c1-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c46c1-117">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="c46c1-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c46c1-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="c46c1-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c46c1-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c46c1-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c46c1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c46c1-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c46c1-127">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c46c1-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="c46c1-128">Pour cette classe, la chaîne est « Microsoft »</span><span class="sxs-lookup"><span data-stu-id="c46c1-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="c46c1-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="c46c1-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c46c1-132">MobileID</span><span class="sxs-lookup"><span data-stu-id="c46c1-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c46c1-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="c46c1-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c46c1-138">**ID**</span><span class="sxs-lookup"><span data-stu-id="c46c1-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c46c1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c46c1-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c46c1-142">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="c46c1-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="c46c1-143">Pour cette classe, la chaîne est « ./DevDetail/Ext »</span><span class="sxs-lookup"><span data-stu-id="c46c1-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="c46c1-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c46c1-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-145">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c46c1-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c46c1-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="c46c1-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-148">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c46c1-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c46c1-150">RadioSwV</span><span class="sxs-lookup"><span data-stu-id="c46c1-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c46c1-153">Retourne le numéro de version du logiciel de la pile radio.</span><span class="sxs-lookup"><span data-stu-id="c46c1-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="c46c1-154">Résolution :</span><span class="sxs-lookup"><span data-stu-id="c46c1-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c46c1-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c46c1-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c46c1-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c46c1-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c46c1-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c46c1-157">Requirements</span></span>



| <span data-ttu-id="c46c1-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c46c1-158">Requirement</span></span> | <span data-ttu-id="c46c1-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="c46c1-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46c1-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c46c1-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c46c1-161">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c46c1-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c46c1-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c46c1-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c46c1-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c46c1-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c46c1-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c46c1-164">Namespace</span></span><br/>                | <span data-ttu-id="c46c1-165">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c46c1-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c46c1-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c46c1-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c46c1-167"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c46c1-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c46c1-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c46c1-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c46c1-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c46c1-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46c1-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c46c1-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46c1-171">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="c46c1-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

