---
title: Classe MDM_ActiveSync_User_ContentTypes04_01
description: La \_ \_ classe User ContentTypes04 01 de MDM ActiveSync \_ \_ définit le type de contenu qui doit être activé ou désactivé individuellement pour la synchronisation.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- Classe MDM_ActiveSync_User_ContentTypes04_01
- Classe MDM_ActiveSync_User_ContentTypes04_01, Description
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512568"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="4f3b4-105">\_ \_ \_ \_ Classe ContentTypes04 01 de l’utilisateur MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="4f3b4-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="4f3b4-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f3b4-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="4f3b4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4f3b4-108">La **classe \_ \_ User \_ ContentTypes04 \_ 01 de MDM ActiveSync** définit le type de contenu qui doit être activé ou désactivé individuellement pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="4f3b4-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3b4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f3b4-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="4f3b4-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4f3b4-111">Members</span></span>

<span data-ttu-id="4f3b4-112">La **classe \_ \_ utilisateur \_ ContentTypes04 \_ 01 de MDM ActiveSync** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f3b4-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="4f3b4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f3b4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f3b4-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f3b4-114">Properties</span></span>

<span data-ttu-id="4f3b4-115">La **classe \_ \_ utilisateur \_ ContentTypes04 \_ 01 de MDM ActiveSync** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4f3b4-116">Enabled</span><span class="sxs-lookup"><span data-stu-id="4f3b4-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f3b4-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f3b4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f3b4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f3b4-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f3b4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f3b4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f3b4-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="4f3b4-124">Nom</span><span class="sxs-lookup"><span data-stu-id="4f3b4-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f3b4-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4f3b4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f3b4-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f3b4-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f3b4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f3b4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f3b4-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f3b4-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f3b4-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="4f3b4-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="4f3b4-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/ActiveSync/Accounts/*GUID*/options »</span><span class="sxs-lookup"><span data-stu-id="4f3b4-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f3b4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f3b4-133">Requirements</span></span>



| <span data-ttu-id="4f3b4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f3b4-134">Requirement</span></span> | <span data-ttu-id="4f3b4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f3b4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3b4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f3b4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4f3b4-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f3b4-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f3b4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f3b4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4f3b4-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f3b4-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4f3b4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f3b4-140">Namespace</span></span><br/>                | <span data-ttu-id="4f3b4-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="4f3b4-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4f3b4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4f3b4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f3b4-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f3b4-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f3b4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4f3b4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f3b4-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f3b4-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f3b4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f3b4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3b4-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="4f3b4-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

