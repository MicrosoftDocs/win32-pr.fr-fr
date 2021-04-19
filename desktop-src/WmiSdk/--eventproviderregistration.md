---
description: Utilisé pour inscrire des fournisseurs d’événements avec Windows Management Instrumentation (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538912"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="223d5-103">\_\_EventProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="223d5-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="223d5-104">La classe système **\_ \_ EventProviderRegistration** est utilisée pour enregistrer des fournisseurs d’événements avec Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="223d5-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="223d5-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="223d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="223d5-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="223d5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="223d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="223d5-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="223d5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="223d5-108">Members</span></span>

<span data-ttu-id="223d5-109">La classe **\_ \_ EventProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="223d5-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="223d5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="223d5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="223d5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="223d5-111">Properties</span></span>

<span data-ttu-id="223d5-112">La classe **\_ \_ EventProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="223d5-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="223d5-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="223d5-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="223d5-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="223d5-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="223d5-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="223d5-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="223d5-116">Une ou plusieurs requêtes WQL (Windows Management Instrumentation Query Language) qui décrivent les événements pris en charge par le fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="223d5-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="223d5-117">**moteur**</span><span class="sxs-lookup"><span data-stu-id="223d5-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="223d5-118">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="223d5-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="223d5-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="223d5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="223d5-120">Chemin d’accès de l’objet au fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="223d5-120">Object path to the event provider.</span></span> <span data-ttu-id="223d5-121">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="223d5-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="223d5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="223d5-122">Remarks</span></span>

<span data-ttu-id="223d5-123">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur d’événements en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="223d5-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="223d5-124">La classe **\_ \_ EventProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="223d5-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="223d5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="223d5-125">Requirements</span></span>



| <span data-ttu-id="223d5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="223d5-126">Requirement</span></span> | <span data-ttu-id="223d5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="223d5-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="223d5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="223d5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="223d5-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="223d5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="223d5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="223d5-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="223d5-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="223d5-132">Namespace</span></span><br/>                | <span data-ttu-id="223d5-133">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="223d5-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="223d5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="223d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223d5-135">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="223d5-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="223d5-136">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="223d5-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="223d5-137">Inscription d’un fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="223d5-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="223d5-138">Écriture d’un fournisseur d’événements</span><span class="sxs-lookup"><span data-stu-id="223d5-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

