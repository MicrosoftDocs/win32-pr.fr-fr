---
description: Représente un ensemble de composants qui fonctionnent comme une entité de niveau supérieur unique.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: Classe CIM_System (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527837"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="da008-103">Classe CIM_System (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="da008-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="da008-104">Représente un ensemble de composants qui fonctionnent comme une entité de niveau supérieur unique.</span><span class="sxs-lookup"><span data-stu-id="da008-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="da008-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da008-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="da008-106">Membres</span><span class="sxs-lookup"><span data-stu-id="da008-106">Members</span></span>

<span data-ttu-id="da008-107">La **classe \_ système CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="da008-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="da008-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="da008-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da008-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="da008-109">Properties</span></span>

<span data-ttu-id="da008-110">La **classe \_ système CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="da008-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da008-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da008-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da008-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da008-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da008-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da008-114">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da008-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da008-115">Nom de classe utilisé pour créer une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="da008-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="da008-116">**CreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="da008-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="da008-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="da008-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-118">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="da008-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da008-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da008-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da008-120">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ système CIM**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="da008-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="da008-121">Tableau qui contient les descriptions des valeurs de la propriété **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="da008-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="da008-122">Les éléments de tableau dans **IdentifyingDescriptions** correspondent aux éléments de la propriété **IdentifyingDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="da008-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="da008-123">**Nom**</span><span class="sxs-lookup"><span data-stu-id="da008-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da008-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da008-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da008-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da008-126">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da008-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da008-127">Clé de cette instance dans un environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="da008-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="da008-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="da008-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da008-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da008-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da008-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da008-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da008-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da008-132">Convention d’affectation de noms utilisée par la propriété Name pour garantir l’unicité des valeurs de **nom** .</span><span class="sxs-lookup"><span data-stu-id="da008-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="da008-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="da008-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-134">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="da008-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da008-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da008-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da008-136">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="da008-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="da008-137">Tableau qui contient un ensemble de données supplémentaires, au-delà des informations sur le nom du système, qui peuvent être utilisées pour identifier un système informatique.</span><span class="sxs-lookup"><span data-stu-id="da008-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="da008-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="da008-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da008-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da008-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="da008-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="da008-141">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="da008-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="da008-142">Chaîne qui fournit des informations sur la façon dont le propriétaire principal du système est accessible (par exemple, numéro de téléphone, adresse de messagerie, etc.).</span><span class="sxs-lookup"><span data-stu-id="da008-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="da008-143">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="da008-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da008-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da008-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="da008-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="da008-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="da008-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="da008-147">Nom de l’utilisateur principal du système.</span><span class="sxs-lookup"><span data-stu-id="da008-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="da008-148">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="da008-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da008-149">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="da008-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da008-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="da008-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="da008-151">Tableau qui contient les rôles exécutés par le système dans un environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="da008-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da008-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da008-152">Requirements</span></span>



| <span data-ttu-id="da008-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da008-153">Requirement</span></span> | <span data-ttu-id="da008-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="da008-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da008-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da008-155">Minimum supported client</span></span><br/> | <span data-ttu-id="da008-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="da008-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="da008-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da008-157">Minimum supported server</span></span><br/> | <span data-ttu-id="da008-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da008-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="da008-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da008-159">Namespace</span></span><br/>                | <span data-ttu-id="da008-160">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="da008-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="da008-161">MOF</span><span class="sxs-lookup"><span data-stu-id="da008-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da008-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da008-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da008-163">DLL</span><span class="sxs-lookup"><span data-stu-id="da008-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da008-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da008-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da008-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da008-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da008-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="da008-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

