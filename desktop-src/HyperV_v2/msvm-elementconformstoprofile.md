---
description: Définit les profils enregistrés conformes au système référencé.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Classe Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843280"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="c208d-103">MSVM \_ ElementConformsToProfile, classe</span><span class="sxs-lookup"><span data-stu-id="c208d-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="c208d-104">Définit les profils enregistrés conformes au système référencé.</span><span class="sxs-lookup"><span data-stu-id="c208d-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="c208d-105">Cette association peut s’appliquer à n’importe quel élément géré.</span><span class="sxs-lookup"><span data-stu-id="c208d-105">This association may apply to any managed element.</span></span> <span data-ttu-id="c208d-106">Une utilisation typique l’applique à une instance de niveau supérieur, telle qu’un système, un espace de noms ou un service.</span><span class="sxs-lookup"><span data-stu-id="c208d-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="c208d-107">Lorsqu’ils sont appliqués à une instance de niveau supérieur, tous les éléments constitutifs doivent se comporter de manière appropriée pour la prise en charge de la conformité de l’élément managé au profil inscrit nommé.</span><span class="sxs-lookup"><span data-stu-id="c208d-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="c208d-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c208d-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c208d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c208d-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="c208d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c208d-110">Members</span></span>

<span data-ttu-id="c208d-111">La classe **MSVM \_ ElementConformsToProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c208d-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="c208d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c208d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c208d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c208d-113">Properties</span></span>

<span data-ttu-id="c208d-114">La classe **MSVM \_ ElementConformsToProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c208d-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c208d-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="c208d-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c208d-116">Type de données : **[ **MSVM \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="c208d-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c208d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c208d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c208d-118">Qualificateurs : [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c208d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c208d-119">Référence à une instance de la classe [**MSVM \_ RegisteredProfile**](msvm-registeredprofile.md) qui représente le profil inscrit auquel le système est conforme.</span><span class="sxs-lookup"><span data-stu-id="c208d-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="c208d-120">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="c208d-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c208d-121">Type de données : **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="c208d-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c208d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c208d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c208d-123">Qualificateurs : [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c208d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c208d-124">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système conforme au profil inscrit.</span><span class="sxs-lookup"><span data-stu-id="c208d-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c208d-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c208d-125">Requirements</span></span>



| <span data-ttu-id="c208d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c208d-126">Requirement</span></span> | <span data-ttu-id="c208d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c208d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c208d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c208d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c208d-129">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c208d-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c208d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c208d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c208d-131">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c208d-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c208d-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c208d-132">Namespace</span></span><br/>                | <span data-ttu-id="c208d-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c208d-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c208d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c208d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c208d-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c208d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c208d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c208d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c208d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c208d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

