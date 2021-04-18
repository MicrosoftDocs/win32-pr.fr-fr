---
title: Classe MDM_Policy_User_Config01_Notifications02
description: La \_ classe Notifications02 de la stratégie MDM \_ User \_ Config01 \_ représente les stratégies de notification disponibles.
ms.assetid: da70b3b4-e8ed-4784-ad6b-52e152a8b78f
keywords:
- Classe MDM_Policy_User_Config01_Notifications02
- Classe MDM_Policy_User_Config01_Notifications02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02.InstanceID
- MDM_Policy_User_Config01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c85dcd9a622d29baf6d7c8f28d9e72b68998ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103873"
---
# <a name="mdm_policy_user_config01_notifications02-class"></a><span data-ttu-id="bafb1-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Notifications02</span><span class="sxs-lookup"><span data-stu-id="bafb1-105">MDM\_Policy\_User\_Config01\_Notifications02 class</span></span>

<span data-ttu-id="bafb1-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="bafb1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bafb1-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="bafb1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bafb1-108">La classe Notifications02 de la **\_ stratégie MDM \_ User \_ Config01 \_** représente les stratégies de notification disponibles.</span><span class="sxs-lookup"><span data-stu-id="bafb1-108">The **MDM\_Policy\_User\_Config01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="bafb1-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bafb1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafb1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bafb1-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="bafb1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bafb1-111">Members</span></span>

<span data-ttu-id="bafb1-112">La **classe \_ \_ \_ Config01 \_ Notifications02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bafb1-112">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="bafb1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bafb1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bafb1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bafb1-114">Properties</span></span>

<span data-ttu-id="bafb1-115">La **classe \_ \_ \_ Config01 \_ Notifications02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bafb1-115">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bafb1-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="bafb1-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bafb1-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="bafb1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bafb1-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bafb1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bafb1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bafb1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bafb1-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bafb1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bafb1-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bafb1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bafb1-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bafb1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bafb1-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bafb1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="bafb1-124">Pour cette classe, la chaîne est « notifications ».</span><span class="sxs-lookup"><span data-stu-id="bafb1-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="bafb1-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="bafb1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bafb1-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bafb1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bafb1-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bafb1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bafb1-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bafb1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bafb1-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="bafb1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="bafb1-130">Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="bafb1-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bafb1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bafb1-131">Requirements</span></span>



| <span data-ttu-id="bafb1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bafb1-132">Requirement</span></span> | <span data-ttu-id="bafb1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bafb1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bafb1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bafb1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bafb1-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bafb1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bafb1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bafb1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bafb1-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bafb1-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="bafb1-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bafb1-138">Namespace</span></span><br/>                | <span data-ttu-id="bafb1-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="bafb1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="bafb1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bafb1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bafb1-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bafb1-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="bafb1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bafb1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bafb1-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="bafb1-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

