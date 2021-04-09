---
title: Classe MDM_EnterpriseAPN_Settings01
description: La \_ \_ classe SETTINGS01 EnterpriseAPN MDM est utilisée par l’entreprise pour modifier les paramètres globaux du APN.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- Classe MDM_EnterpriseAPN_Settings01
- Classe MDM_EnterpriseAPN_Settings01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104992"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="7fe1e-105">\_ \_ Classe SETTINGS01 EnterpriseAPN MDM</span><span class="sxs-lookup"><span data-stu-id="7fe1e-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="7fe1e-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7fe1e-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7fe1e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7fe1e-108">La **classe \_ \_ Settings01 EnterpriseAPN MDM** est utilisée par l’entreprise pour modifier les paramètres globaux du APN.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="7fe1e-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe1e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fe1e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="7fe1e-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7fe1e-111">Members</span></span>

<span data-ttu-id="7fe1e-112">La **classe \_ EnterpriseAPN \_ Settings01 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fe1e-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="7fe1e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fe1e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fe1e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fe1e-114">Properties</span></span>

<span data-ttu-id="7fe1e-115">La **classe \_ EnterpriseAPN \_ Settings01 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7fe1e-116">AllowUserControl</span><span class="sxs-lookup"><span data-stu-id="7fe1e-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe1e-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7fe1e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7fe1e-119">HideView</span><span class="sxs-lookup"><span data-stu-id="7fe1e-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe1e-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7fe1e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fe1e-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe1e-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe1e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7fe1e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7fe1e-126">Nœud qui contient les paramètres globaux du APN.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="7fe1e-127">**ID**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe1e-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fe1e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fe1e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe1e-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7fe1e-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7fe1e-131">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="7fe1e-132">Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseAPN/Settings »</span><span class="sxs-lookup"><span data-stu-id="7fe1e-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fe1e-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fe1e-133">Requirements</span></span>



| <span data-ttu-id="7fe1e-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fe1e-134">Requirement</span></span> | <span data-ttu-id="7fe1e-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fe1e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe1e-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe1e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe1e-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fe1e-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fe1e-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe1e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe1e-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fe1e-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7fe1e-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7fe1e-140">Namespace</span></span><br/>                | <span data-ttu-id="7fe1e-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7fe1e-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7fe1e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7fe1e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fe1e-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fe1e-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fe1e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe1e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe1e-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fe1e-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

