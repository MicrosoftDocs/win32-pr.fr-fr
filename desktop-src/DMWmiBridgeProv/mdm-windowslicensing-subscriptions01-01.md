---
title: Classe MDM_WindowsLicensing_Subscriptions01_01
description: La \_ classe MDM WindowsLicensing \_ Subscriptions01 \_ 01 est conçue pour les scénarios de gestion des licences liées aux abonnements.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- Classe MDM_WindowsLicensing_Subscriptions01_01
- Classe MDM_WindowsLicensing_Subscriptions01_01, Description
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104938"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="044f9-105">\_Classe WindowsLicensing \_ SUBSCRIPTIONS01 \_ 01 MDM</span><span class="sxs-lookup"><span data-stu-id="044f9-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="044f9-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="044f9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="044f9-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="044f9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="044f9-108">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** est conçue pour les scénarios de gestion des licences liées aux abonnements.</span><span class="sxs-lookup"><span data-stu-id="044f9-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="044f9-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="044f9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="044f9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="044f9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="044f9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="044f9-111">Members</span></span>

<span data-ttu-id="044f9-112">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="044f9-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="044f9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="044f9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="044f9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="044f9-114">Properties</span></span>

<span data-ttu-id="044f9-115">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="044f9-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="044f9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="044f9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="044f9-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="044f9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="044f9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="044f9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="044f9-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="044f9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="044f9-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="044f9-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="044f9-121">Nom</span><span class="sxs-lookup"><span data-stu-id="044f9-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="044f9-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="044f9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="044f9-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="044f9-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="044f9-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="044f9-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="044f9-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="044f9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="044f9-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="044f9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="044f9-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="044f9-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="044f9-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="044f9-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="044f9-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/WindowsLicensing »</span><span class="sxs-lookup"><span data-stu-id="044f9-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="044f9-130">État</span><span class="sxs-lookup"><span data-stu-id="044f9-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="044f9-131">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="044f9-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="044f9-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="044f9-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="044f9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="044f9-133">Requirements</span></span>



| <span data-ttu-id="044f9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="044f9-134">Requirement</span></span> | <span data-ttu-id="044f9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="044f9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="044f9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="044f9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="044f9-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="044f9-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="044f9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="044f9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="044f9-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="044f9-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="044f9-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="044f9-140">Namespace</span></span><br/>                | <span data-ttu-id="044f9-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="044f9-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="044f9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="044f9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="044f9-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="044f9-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="044f9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="044f9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044f9-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044f9-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

