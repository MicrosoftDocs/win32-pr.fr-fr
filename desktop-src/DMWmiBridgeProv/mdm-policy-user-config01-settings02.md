---
title: Classe MDM_Policy_User_Config01_Settings02
description: La \_ \_ \_ classe Config01 Settings02 utilisateur de la stratégie MDM \_ configure des calendriers supplémentaires dans la barre des tâches.
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- Classe MDM_Policy_User_Config01_Settings02
- Classe MDM_Policy_User_Config01_Settings02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103864"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="1e136-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Settings02</span><span class="sxs-lookup"><span data-stu-id="1e136-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="1e136-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1e136-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e136-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1e136-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e136-108">La \_ \_ \_ classe Config01 Settings02 utilisateur de la stratégie MDM \_ configure des calendriers supplémentaires dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="1e136-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="1e136-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1e136-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e136-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e136-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="1e136-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1e136-111">Members</span></span>

<span data-ttu-id="1e136-112">La **classe \_ \_ \_ Config01 \_ Settings02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1e136-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="1e136-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e136-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e136-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1e136-114">Properties</span></span>

<span data-ttu-id="1e136-115">La **classe \_ \_ \_ Config01 \_ Settings02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1e136-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1e136-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="1e136-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e136-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="1e136-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e136-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1e136-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e136-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e136-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e136-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e136-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e136-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e136-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e136-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e136-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e136-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="1e136-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e136-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1e136-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e136-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1e136-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e136-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e136-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e136-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e136-127">Requirements</span></span>



| <span data-ttu-id="1e136-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e136-128">Requirement</span></span> | <span data-ttu-id="1e136-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e136-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e136-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e136-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1e136-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e136-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e136-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e136-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1e136-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e136-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e136-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e136-134">Namespace</span></span><br/>                | <span data-ttu-id="1e136-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="1e136-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e136-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1e136-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e136-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e136-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e136-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1e136-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e136-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e136-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

