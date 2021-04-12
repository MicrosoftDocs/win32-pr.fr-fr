---
description: Une classe d’affichage d’association vous permet d’utiliser des ASSOCIateurs de requêtes sur des classes qui résident dans des espaces de noms différents.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associer des instances entre des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319466"
---
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="988dd-103">Associer des instances entre des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="988dd-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="988dd-104">Une classe d’affichage d’association vous permet d’utiliser [des associateurs de](associators-of-statement.md) requêtes sur des classes qui résident dans des espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="988dd-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="988dd-105">La procédure suivante décrit comment associer des instances entre des espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="988dd-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="988dd-106">**Pour associer des instances entre des espaces de noms**</span><span class="sxs-lookup"><span data-stu-id="988dd-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="988dd-107">Commencez votre définition de classe par le qualificateur de chaîne d' [**Association**](meta-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="988dd-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="988dd-108">Les qualificateurs **JoinOn**, [**Association**](meta-qualifiers.md)et **Union** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="988dd-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="988dd-109">Créez les requêtes qui définissent les instances source utilisées dans la classe de vue avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="988dd-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="988dd-110">Définissez les noms et l’emplacement des espaces de noms dans lesquels se trouvent les instances source avec le qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="988dd-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="988dd-111">Définissez les propriétés souhaitées dans votre classe de vue d’association avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="988dd-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="988dd-112">Si nécessaire, vous pouvez marquer l’une des propriétés comme appartenant à une classe source à l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="988dd-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="988dd-113">Baliser toutes les propriétés pertinentes avec le qualificateur **direct** .</span><span class="sxs-lookup"><span data-stu-id="988dd-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="988dd-114">Le qualificateur **direct** empêche le fournisseur d’affichage de mapper la référence d’association avec balises à une référence de vue.</span><span class="sxs-lookup"><span data-stu-id="988dd-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="988dd-115">Les exemples de code suivants montrent comment créer des classes d’affichage d’association.</span><span class="sxs-lookup"><span data-stu-id="988dd-115">The following code examples show how to create association view classes.</span></span>

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



