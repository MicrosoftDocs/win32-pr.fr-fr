---
description: Une classe d’affichage d’association vous permet d’utiliser des ASSOCIateurs de requêtes sur des classes qui résident dans des espaces de noms différents.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associer des instances entre des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557017"
---
# <a name="associating-instances-between-namespaces"></a>Associer des instances entre des espaces de noms

Une classe d’affichage d’association vous permet d’utiliser [des associateurs de](associators-of-statement.md) requêtes sur des classes qui résident dans des espaces de noms différents.

La procédure suivante décrit comment associer des instances entre des espaces de noms.

**Pour associer des instances entre des espaces de noms**

1.  Commencez votre définition de classe par le qualificateur de chaîne d' [**Association**](meta-qualifiers.md) .

    Les qualificateurs **JoinOn**, [**Association**](meta-qualifiers.md)et **Union** s’excluent mutuellement.

2.  Créez les requêtes qui définissent les instances source utilisées dans la classe de vue avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .
3.  Définissez les noms et l’emplacement des espaces de noms dans lesquels se trouvent les instances source avec le qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Définissez les propriétés souhaitées dans votre classe de vue d’association avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .

    Si nécessaire, vous pouvez marquer l’une des propriétés comme appartenant à une classe source à l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Baliser toutes les propriétés pertinentes avec le qualificateur **direct** .

    Le qualificateur **direct** empêche le fournisseur d’affichage de mapper la référence d’association avec balises à une référence de vue.

Les exemples de code suivants montrent comment créer des classes d’affichage d’association.

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

 

 



