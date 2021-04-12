---
description: Classe de base abstraite pour les classes qui représentent les paramètres d’une fonctionnalité de port commuté Ethernet.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Classe Msvm_EthernetSwitchPortFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319401"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="ca52c-103">MSVM \_ EthernetSwitchPortFeatureSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ca52c-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="ca52c-104">Classe de base abstraite pour les classes qui représentent les paramètres d’une fonctionnalité de port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ca52c-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="ca52c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ca52c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca52c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca52c-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="ca52c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ca52c-107">Members</span></span>

<span data-ttu-id="ca52c-108">La classe **MSVM \_ EthernetSwitchPortFeatureSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ca52c-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ca52c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca52c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca52c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca52c-110">Properties</span></span>

<span data-ttu-id="ca52c-111">La classe **MSVM \_ EthernetSwitchPortFeatureSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca52c-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca52c-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ca52c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca52c-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca52c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca52c-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca52c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca52c-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca52c-115">A short description of the object.</span></span> <span data-ttu-id="ca52c-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca52c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca52c-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="ca52c-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca52c-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca52c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca52c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca52c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca52c-120">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ca52c-120">A description of the object.</span></span> <span data-ttu-id="ca52c-121">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca52c-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca52c-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ca52c-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca52c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca52c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca52c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca52c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca52c-125">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca52c-125">A display name for the object.</span></span> <span data-ttu-id="ca52c-126">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca52c-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ca52c-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca52c-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca52c-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca52c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca52c-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca52c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca52c-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ca52c-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca52c-131">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ca52c-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ca52c-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca52c-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca52c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca52c-133">Requirements</span></span>



| <span data-ttu-id="ca52c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca52c-134">Requirement</span></span> | <span data-ttu-id="ca52c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca52c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca52c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca52c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ca52c-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca52c-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca52c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca52c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ca52c-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca52c-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca52c-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca52c-140">Namespace</span></span><br/>                | <span data-ttu-id="ca52c-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca52c-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca52c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ca52c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca52c-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca52c-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca52c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ca52c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca52c-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca52c-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

