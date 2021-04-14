---
title: Classe MDM_Policy_User_Config01_AttachmentManager02
description: La \_ \_ classe Config01 AttachmentManager02 utilisateur de la stratégie MDM \_ \_ représente les stratégies du gestionnaire de pièces jointes disponibles.
ms.assetid: b20ec516-cdc9-4aeb-802d-97cd8423eceb
keywords:
- Classe MDM_Policy_User_Config01_AttachmentManager02
- Classe MDM_Policy_User_Config01_AttachmentManager02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_AttachmentManager02
- MDM_Policy_User_Config01_AttachmentManager02.InstanceID
- MDM_Policy_User_Config01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127fc3770f6ba605bd8e1efdd82314231ab27f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509010"
---
# <a name="mdm_policy_user_config01_attachmentmanager02-class"></a><span data-ttu-id="a6146-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ AttachmentManager02</span><span class="sxs-lookup"><span data-stu-id="a6146-105">MDM\_Policy\_User\_Config01\_AttachmentManager02 class</span></span>

<span data-ttu-id="a6146-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a6146-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a6146-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a6146-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a6146-108">La \_ \_ classe Config01 AttachmentManager02 utilisateur de la stratégie MDM \_ \_ représente les stratégies du gestionnaire de pièces jointes disponibles.</span><span class="sxs-lookup"><span data-stu-id="a6146-108">The MDM\_Policy\_User\_Config01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="a6146-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a6146-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6146-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6146-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="a6146-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a6146-111">Members</span></span>

<span data-ttu-id="a6146-112">La **classe \_ \_ \_ Config01 \_ AttachmentManager02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6146-112">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="a6146-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6146-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6146-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6146-114">Properties</span></span>

<span data-ttu-id="a6146-115">La **classe \_ \_ \_ Config01 \_ AttachmentManager02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a6146-115">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a6146-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="a6146-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6146-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6146-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6146-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a6146-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a6146-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="a6146-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6146-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6146-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6146-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a6146-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6146-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6146-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6146-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6146-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6146-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6146-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6146-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6146-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a6146-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="a6146-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6146-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6146-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6146-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a6146-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6146-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="a6146-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6146-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6146-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6146-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6146-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6146-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6146-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6146-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6146-133">Requirements</span></span>



| <span data-ttu-id="a6146-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6146-134">Requirement</span></span> | <span data-ttu-id="a6146-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6146-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6146-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6146-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a6146-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6146-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6146-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6146-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a6146-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6146-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a6146-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a6146-140">Namespace</span></span><br/>                | <span data-ttu-id="a6146-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a6146-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a6146-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a6146-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6146-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6146-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6146-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a6146-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6146-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6146-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

