---
description: Sert de classe parente pour les classes d’inscription de différents types de fournisseurs.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Classe __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115655"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="c18a0-103">\_\_ProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="c18a0-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="c18a0-104">La classe système abstraite **\_ \_ ProviderRegistration** sert de classe parente pour les classes d’inscription de différents types de fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="c18a0-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="c18a0-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c18a0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c18a0-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c18a0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c18a0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c18a0-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="c18a0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c18a0-108">Members</span></span>

<span data-ttu-id="c18a0-109">La classe **\_ \_ ProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c18a0-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c18a0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c18a0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c18a0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c18a0-111">Properties</span></span>

<span data-ttu-id="c18a0-112">La classe **\_ \_ ProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c18a0-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c18a0-113">**moteur**</span><span class="sxs-lookup"><span data-stu-id="c18a0-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c18a0-114">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="c18a0-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="c18a0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c18a0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c18a0-116">Référence à une instance du [**\_ \_ fournisseur**](--provider.md) représentant le chemin d’accès de l’objet au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c18a0-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c18a0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c18a0-117">Remarks</span></span>

<span data-ttu-id="c18a0-118">La classe **\_ \_ ProviderRegistration** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c18a0-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="c18a0-119">Les instances de la classe système **\_ \_ ProviderRegistration** ne sont jamais créées.</span><span class="sxs-lookup"><span data-stu-id="c18a0-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="c18a0-120">Les classes que les fournisseurs utilisent pour créer des instances pour l’inscription dérivent directement ou indirectement de cette classe.</span><span class="sxs-lookup"><span data-stu-id="c18a0-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="c18a0-121">Il s'agit des classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c18a0-121">These classes are:</span></span>

[<span data-ttu-id="c18a0-122">**\_\_ClassProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="c18a0-123">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="c18a0-124">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="c18a0-125">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="c18a0-126">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="c18a0-127">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="c18a0-128">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c18a0-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="c18a0-129">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et en l’inscrivant.</span><span class="sxs-lookup"><span data-stu-id="c18a0-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c18a0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c18a0-130">Requirements</span></span>



| <span data-ttu-id="c18a0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c18a0-131">Requirement</span></span> | <span data-ttu-id="c18a0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c18a0-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c18a0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c18a0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c18a0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c18a0-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c18a0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c18a0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c18a0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c18a0-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c18a0-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c18a0-137">Namespace</span></span><br/>                | <span data-ttu-id="c18a0-138">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="c18a0-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c18a0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c18a0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c18a0-140">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="c18a0-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="c18a0-141">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="c18a0-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c18a0-142">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="c18a0-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

