---
description: Cette classe est déconseillée. Au lieu de cela, nous vous recommandons de dériver de la \_ classe de service CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541958"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="d8d11-104">\_Classe CIM NetworkService</span><span class="sxs-lookup"><span data-stu-id="d8d11-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="d8d11-105">Cette classe est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d8d11-105">This class is deprecated.</span></span> <span data-ttu-id="d8d11-106">Au lieu de cela, nous vous recommandons de dériver de la classe de [**\_ service CIM**](cim-service.md) .</span><span class="sxs-lookup"><span data-stu-id="d8d11-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8d11-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="d8d11-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d8d11-108">Members</span></span>

<span data-ttu-id="d8d11-109">La classe **CIM \_ NetworkService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8d11-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="d8d11-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8d11-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8d11-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8d11-111">Properties</span></span>

<span data-ttu-id="d8d11-112">La classe **CIM \_ NetworkService** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8d11-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8d11-113">**Mots clés**</span><span class="sxs-lookup"><span data-stu-id="d8d11-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d11-114">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8d11-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8d11-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-116">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="d8d11-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="d8d11-117">Cette propriété est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8d11-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="d8d11-118">Description déconseillée : un tableau de mots clés qui peuvent être utilisés dans les requêtes.</span><span class="sxs-lookup"><span data-stu-id="d8d11-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8d11-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="d8d11-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d11-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8d11-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8d11-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-122">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")</span><span class="sxs-lookup"><span data-stu-id="d8d11-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="d8d11-123">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d8d11-123">This property is deprecated.</span></span> <span data-ttu-id="d8d11-124">Au lieu de cela, nous vous recommandons la classe **CIM \_ ServiceAccessURI** .</span><span class="sxs-lookup"><span data-stu-id="d8d11-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="d8d11-125">Description déconseillée : URL qui fournit le protocole, l’emplacement réseau et d’autres informations spécifiques au service nécessaires pour accéder au service.</span><span class="sxs-lookup"><span data-stu-id="d8d11-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8d11-126">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="d8d11-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d11-127">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8d11-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8d11-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-129">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="d8d11-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="d8d11-130">Cette propriété est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8d11-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="d8d11-131">Description déconseillée : conditions préalables qui doivent être remplies pour que ce service démarre correctement.</span><span class="sxs-lookup"><span data-stu-id="d8d11-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="d8d11-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="d8d11-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d11-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d8d11-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8d11-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8d11-135">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="d8d11-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="d8d11-136">Cette propriété est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8d11-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="d8d11-137">Description déconseillée : les paramètres qui doivent être fournis à la méthode **StartService** pour que ce service démarre correctement.</span><span class="sxs-lookup"><span data-stu-id="d8d11-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8d11-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8d11-138">Requirements</span></span>



| <span data-ttu-id="d8d11-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8d11-139">Requirement</span></span> | <span data-ttu-id="d8d11-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8d11-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d11-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8d11-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d11-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8d11-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d8d11-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8d11-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d11-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8d11-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d8d11-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8d11-145">Namespace</span></span><br/>                | <span data-ttu-id="d8d11-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8d11-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8d11-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d8d11-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8d11-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8d11-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8d11-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d8d11-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8d11-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8d11-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8d11-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8d11-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d11-152">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="d8d11-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

