---
description: Classe abstraite qui représente les paramètres d’une instance donnée d’une fonctionnalité de commutateur Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Classe Msvm_EthernetSwitchFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535082"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="b7ffb-103">MSVM \_ EthernetSwitchFeatureSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="b7ffb-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="b7ffb-104">Classe abstraite qui représente les paramètres d’une instance donnée d’une fonctionnalité de commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="b7ffb-105">La classe de gestion des paramètres des fonctionnalités du commutateur Ethernet doit dériver de cette classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="b7ffb-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ffb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7ffb-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="b7ffb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b7ffb-108">Members</span></span>

<span data-ttu-id="b7ffb-109">La classe **MSVM \_ EthernetSwitchFeatureSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7ffb-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b7ffb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7ffb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7ffb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7ffb-111">Properties</span></span>

<span data-ttu-id="b7ffb-112">La classe **MSVM \_ EthernetSwitchFeatureSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7ffb-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7ffb-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7ffb-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7ffb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7ffb-116">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-116">A short description of the object.</span></span> <span data-ttu-id="b7ffb-117">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7ffb-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7ffb-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7ffb-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7ffb-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7ffb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7ffb-121">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="b7ffb-121">A description of the object.</span></span> <span data-ttu-id="b7ffb-122">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b7ffb-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b7ffb-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7ffb-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7ffb-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7ffb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7ffb-126">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-126">A display name for the object.</span></span> <span data-ttu-id="b7ffb-127">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7ffb-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b7ffb-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7ffb-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7ffb-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7ffb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7ffb-131">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b7ffb-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b7ffb-132">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b7ffb-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b7ffb-133">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7ffb-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7ffb-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7ffb-134">Requirements</span></span>



| <span data-ttu-id="b7ffb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7ffb-135">Requirement</span></span> | <span data-ttu-id="b7ffb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7ffb-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ffb-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ffb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ffb-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ffb-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b7ffb-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ffb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ffb-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ffb-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7ffb-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7ffb-141">Namespace</span></span><br/>                | <span data-ttu-id="b7ffb-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b7ffb-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b7ffb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b7ffb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7ffb-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7ffb-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7ffb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b7ffb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7ffb-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7ffb-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

