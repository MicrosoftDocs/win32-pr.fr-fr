---
title: Classe MDM_Policy_Config01_ActiveXControls02
description: Ce paramètre de stratégie détermine les sites d’installation ActiveX que les utilisateurs standard de votre organisation peuvent utiliser pour installer des contrôles ActiveX sur leurs ordinateurs.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- Classe MDM_Policy_Config01_ActiveXControls02
- Classe MDM_Policy_Config01_ActiveXControls02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512566"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="6aa52-105">\_Classe ActiveXControls02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="6aa52-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="6aa52-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="6aa52-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6aa52-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="6aa52-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6aa52-108">Ce paramètre de stratégie détermine les sites d’installation ActiveX que les utilisateurs standard de votre organisation peuvent utiliser pour installer des contrôles ActiveX sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6aa52-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="6aa52-109">Lorsque ce paramètre est activé, l’administrateur peut créer une liste des sites d’installation ActiveX approuvés spécifiés par l’URL de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="6aa52-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="6aa52-110">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6aa52-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa52-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aa52-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="6aa52-112">Membres</span><span class="sxs-lookup"><span data-stu-id="6aa52-112">Members</span></span>

<span data-ttu-id="6aa52-113">La **classe \_ \_ Config01 \_ ActiveXControls02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6aa52-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="6aa52-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6aa52-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6aa52-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6aa52-115">Properties</span></span>

<span data-ttu-id="6aa52-116">La **classe \_ \_ Config01 \_ ActiveXControls02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6aa52-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6aa52-117">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="6aa52-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa52-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6aa52-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa52-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6aa52-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6aa52-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6aa52-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa52-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6aa52-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa52-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6aa52-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aa52-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6aa52-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6aa52-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="6aa52-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aa52-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6aa52-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aa52-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6aa52-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aa52-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6aa52-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6aa52-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6aa52-128">Requirements</span></span>



| <span data-ttu-id="6aa52-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6aa52-129">Requirement</span></span> | <span data-ttu-id="6aa52-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6aa52-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa52-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa52-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa52-132">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6aa52-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6aa52-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa52-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa52-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa52-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6aa52-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6aa52-135">Namespace</span></span><br/>                | <span data-ttu-id="6aa52-136">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="6aa52-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6aa52-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6aa52-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6aa52-138"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6aa52-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6aa52-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa52-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa52-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa52-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

