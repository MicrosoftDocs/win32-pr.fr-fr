---
description: Inscrit les fournisseurs de consommateur d’événements avec WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867357"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="29360-103">\_\_EventConsumerProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="29360-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="29360-104">La classe système **\_ \_ EventConsumerProviderRegistration** enregistre les fournisseurs de consommateur d’événements avec WMI.</span><span class="sxs-lookup"><span data-stu-id="29360-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="29360-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="29360-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29360-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="29360-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29360-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29360-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="29360-108">Membres</span><span class="sxs-lookup"><span data-stu-id="29360-108">Members</span></span>

<span data-ttu-id="29360-109">La classe **\_ \_ EventConsumerProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29360-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="29360-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29360-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29360-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29360-111">Properties</span></span>

<span data-ttu-id="29360-112">La classe **\_ \_ EventConsumerProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="29360-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29360-113">**ConsumerClassNames**</span><span class="sxs-lookup"><span data-stu-id="29360-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="29360-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29360-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="29360-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="29360-116">Tableau de noms des classes de consommateur logiques prises en charge par le fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="29360-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="29360-117">**moteur**</span><span class="sxs-lookup"><span data-stu-id="29360-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29360-118">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="29360-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="29360-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29360-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29360-120">Chemin d’accès de l’objet au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="29360-120">Object path to the provider.</span></span> <span data-ttu-id="29360-121">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29360-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29360-122">Notes</span><span class="sxs-lookup"><span data-stu-id="29360-122">Remarks</span></span>

<span data-ttu-id="29360-123">La classe **\_ \_ EventConsumerProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="29360-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29360-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29360-124">Requirements</span></span>



| <span data-ttu-id="29360-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29360-125">Requirement</span></span> | <span data-ttu-id="29360-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="29360-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="29360-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29360-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29360-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29360-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="29360-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29360-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29360-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29360-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="29360-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29360-131">Namespace</span></span><br/>                | <span data-ttu-id="29360-132">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="29360-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="29360-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29360-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29360-134">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="29360-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="29360-135">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="29360-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="29360-136">Inscription d’un fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="29360-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="29360-137">Écriture d’un fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="29360-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

