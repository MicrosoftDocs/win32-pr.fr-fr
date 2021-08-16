---
description: Une classe d’affichage Union est une Union logique des instances de la classe source. Une classe d’affichage Union inclut toutes les instances des classes sources, sauf si vous limitez les instances en incluant une clause WHERE sur la requête source.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Création d’une classe d’affichage Union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612389"
---
# <a name="creating-a-union-view-class"></a>Création d’une classe d’affichage Union

Une classe d’affichage Union est une Union logique des instances de la classe source. Une classe d’affichage Union inclut toutes les instances des classes sources, sauf si vous limitez les instances en incluant une clause WHERE sur la requête source.

Les classes d’affichage d’Union sont utiles lorsque vous souhaitez afficher des instances de classes similaires ou identiques qui se trouvent dans des espaces de noms différents ou sur des ordinateurs différents. Par exemple, vous pouvez créer une classe Union qui contient des instances de lecteurs de disque différents à surveiller.

Vous pouvez également baser les propriétés d’une classe d’affichage Union sur les propriétés qui ne sont pas présentes dans toutes les instances de la classe source. Si les instances de la classe source n’ont pas la même propriété, les propriétés des instances de la classe Union ont la valeur **null**. Par exemple, si un lecteur de disque dur a une propriété **Temperature** mais qu’un autre ne le fait pas, vous pouvez toujours créer une Union entre les deux.

La procédure suivante décrit comment créer une classe d’affichage d’Union.

**Pour créer une classe d’affichage Union**

1.  Commencez votre définition de classe par le qualificateur de chaîne d' [**Union**](qualifiers-specific-to-the-view-provider.md) .

    Les qualificateurs [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** et **Union** s’excluent mutuellement.

2.  Créez les requêtes qui définissent les classes sources utilisées dans la classe de vue avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .
3.  Définissez les noms et l’emplacement des espaces de noms dans lesquels les classes sources sont situées avec le qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Définissez les propriétés qui mappent aux propriétés dans les classes sources avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .

    Si nécessaire, vous pouvez marquer l’une des propriétés comme appartenant à une classe source à l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Définissez les propriétés de clé des classes sources de votre classe d’affichage Union.

    Chaque classe source doit avoir le même nombre de propriétés de clé correspondant à [**CimType**](swbemproperty-cimtype.md). En outre, les clés de votre classe d’affichage d’Union doivent identifier toutes les instances de la source de manière unique. Dans certains cas, vous devrez peut-être spécifier des propriétés système pour vous assurer que les instances sont uniques. Par exemple, si vous créez une vue à partir de l’Union de deux classes identiques dans deux espaces de noms différents, vous pouvez inclure la propriété d' [**\_ \_ espace de noms**](--namespace.md) en tant que clé dans la classe de vue pour différencier les deux instances. Si vous utilisez deux classes similaires du même espace de noms pour créer une vue, vous pouvez utiliser la propriété de la **\_ \_ classe** pour faire la distinction entre les deux. Renommez les propriétés système dans la vue afin d’éviter un conflit avec les propriétés système de la classe d’affichage.

6.  Définissez les méthodes souhaitées à l’aide du qualificateur [**MethodSource**](qualifiers-specific-to-the-view-provider.md) .

    Contrairement aux autres classes d’affichage, vous pouvez créer des méthodes pour modifier une vue d’Union.

L’exemple de code suivant décrit une classe d’affichage Union.

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



