---
title: Classe MDM_VPNv2_Eap04
description: La \_ classe VPNv2 \_ Eap04 MDM contient les informations XML de configuration requises lorsque le profil natif spécifie l’authentification EAP.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- Classe MDM_VPNv2_Eap04
- Classe MDM_VPNv2_Eap04, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743164"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="df3ee-105">\_ \_ Classe EAP04 VPNv2 MDM</span><span class="sxs-lookup"><span data-stu-id="df3ee-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="df3ee-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="df3ee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="df3ee-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="df3ee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="df3ee-108">La **classe \_ VPNv2 \_ Eap04 MDM** contient les informations XML de configuration requises lorsque le profil natif spécifie l’authentification EAP.</span><span class="sxs-lookup"><span data-stu-id="df3ee-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="df3ee-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="df3ee-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3ee-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df3ee-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="df3ee-111">Membres</span><span class="sxs-lookup"><span data-stu-id="df3ee-111">Members</span></span>

<span data-ttu-id="df3ee-112">La **classe \_ VPNv2 \_ Eap04 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df3ee-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="df3ee-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df3ee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df3ee-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df3ee-114">Properties</span></span>

<span data-ttu-id="df3ee-115">La **classe \_ VPNv2 \_ Eap04 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="df3ee-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="df3ee-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="df3ee-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df3ee-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df3ee-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="df3ee-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df3ee-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df3ee-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df3ee-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df3ee-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df3ee-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df3ee-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df3ee-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="df3ee-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="df3ee-124">Pour cette classe, la chaîne est « EAP ».</span><span class="sxs-lookup"><span data-stu-id="df3ee-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="df3ee-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="df3ee-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df3ee-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df3ee-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df3ee-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="df3ee-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="df3ee-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="df3ee-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="df3ee-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication »</span><span class="sxs-lookup"><span data-stu-id="df3ee-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="df3ee-131">Type</span><span class="sxs-lookup"><span data-stu-id="df3ee-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="df3ee-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="df3ee-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="df3ee-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="df3ee-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df3ee-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df3ee-134">Requirements</span></span>



| <span data-ttu-id="df3ee-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df3ee-135">Requirement</span></span> | <span data-ttu-id="df3ee-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="df3ee-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df3ee-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df3ee-137">Minimum supported client</span></span><br/> | <span data-ttu-id="df3ee-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df3ee-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df3ee-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df3ee-139">Minimum supported server</span></span><br/> | <span data-ttu-id="df3ee-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="df3ee-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="df3ee-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df3ee-141">Namespace</span></span><br/>                | <span data-ttu-id="df3ee-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="df3ee-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="df3ee-143">MOF</span><span class="sxs-lookup"><span data-stu-id="df3ee-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df3ee-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df3ee-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="df3ee-145">DLL</span><span class="sxs-lookup"><span data-stu-id="df3ee-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df3ee-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df3ee-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3ee-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df3ee-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3ee-148">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="df3ee-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

