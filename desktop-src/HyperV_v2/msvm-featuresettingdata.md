---
description: Classe abstraite qui représente les paramètres d’une fonctionnalité spécifique d’un système ou d’un composant.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Classe Msvm_FeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525234"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="12d7d-103">MSVM \_ FeatureSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="12d7d-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="12d7d-104">Classe abstraite qui représente les paramètres d’une fonctionnalité spécifique d’un système ou d’un composant.</span><span class="sxs-lookup"><span data-stu-id="12d7d-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="12d7d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="12d7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d7d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12d7d-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="12d7d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="12d7d-107">Members</span></span>

<span data-ttu-id="12d7d-108">La classe **MSVM \_ FeatureSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="12d7d-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="12d7d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12d7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12d7d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12d7d-110">Properties</span></span>

<span data-ttu-id="12d7d-111">La classe **MSVM \_ FeatureSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="12d7d-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d7d-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="12d7d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d7d-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12d7d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d7d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12d7d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d7d-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12d7d-115">A short description of the object.</span></span> <span data-ttu-id="12d7d-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="12d7d-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="12d7d-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="12d7d-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d7d-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12d7d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d7d-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12d7d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d7d-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="12d7d-120">A description of the object.</span></span> <span data-ttu-id="12d7d-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="12d7d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="12d7d-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="12d7d-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d7d-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12d7d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d7d-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12d7d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d7d-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="12d7d-125">A display name for the object.</span></span> <span data-ttu-id="12d7d-126">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12d7d-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="12d7d-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="12d7d-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d7d-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="12d7d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d7d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="12d7d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d7d-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="12d7d-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="12d7d-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="12d7d-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="12d7d-132">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12d7d-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12d7d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12d7d-133">Requirements</span></span>



| <span data-ttu-id="12d7d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12d7d-134">Requirement</span></span> | <span data-ttu-id="12d7d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="12d7d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d7d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d7d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="12d7d-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12d7d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12d7d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12d7d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="12d7d-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12d7d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12d7d-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="12d7d-140">Namespace</span></span><br/>                | <span data-ttu-id="12d7d-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="12d7d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12d7d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="12d7d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d7d-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12d7d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d7d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="12d7d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d7d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12d7d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

