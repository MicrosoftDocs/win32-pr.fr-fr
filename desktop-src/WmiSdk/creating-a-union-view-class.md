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
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528326"
---
# <a name="creating-a-union-view-class"></a><span data-ttu-id="d06d2-104">Création d’une classe d’affichage Union</span><span class="sxs-lookup"><span data-stu-id="d06d2-104">Creating a Union View Class</span></span>

<span data-ttu-id="d06d2-105">Une classe d’affichage Union est une Union logique des instances de la classe source.</span><span class="sxs-lookup"><span data-stu-id="d06d2-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="d06d2-106">Une classe d’affichage Union inclut toutes les instances des classes sources, sauf si vous limitez les instances en incluant une clause WHERE sur la requête source.</span><span class="sxs-lookup"><span data-stu-id="d06d2-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="d06d2-107">Les classes d’affichage d’Union sont utiles lorsque vous souhaitez afficher des instances de classes similaires ou identiques qui se trouvent dans des espaces de noms différents ou sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="d06d2-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="d06d2-108">Par exemple, vous pouvez créer une classe Union qui contient des instances de lecteurs de disque différents à surveiller.</span><span class="sxs-lookup"><span data-stu-id="d06d2-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="d06d2-109">Vous pouvez également baser les propriétés d’une classe d’affichage Union sur les propriétés qui ne sont pas présentes dans toutes les instances de la classe source.</span><span class="sxs-lookup"><span data-stu-id="d06d2-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="d06d2-110">Si les instances de la classe source n’ont pas la même propriété, les propriétés des instances de la classe Union ont la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d06d2-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="d06d2-111">Par exemple, si un lecteur de disque dur a une propriété **Temperature** mais qu’un autre ne le fait pas, vous pouvez toujours créer une Union entre les deux.</span><span class="sxs-lookup"><span data-stu-id="d06d2-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="d06d2-112">La procédure suivante décrit comment créer une classe d’affichage d’Union.</span><span class="sxs-lookup"><span data-stu-id="d06d2-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="d06d2-113">**Pour créer une classe d’affichage Union**</span><span class="sxs-lookup"><span data-stu-id="d06d2-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="d06d2-114">Commencez votre définition de classe par le qualificateur de chaîne d' [**Union**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="d06d2-115">Les qualificateurs [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** et **Union** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="d06d2-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="d06d2-116">Créez les requêtes qui définissent les classes sources utilisées dans la classe de vue avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="d06d2-117">Définissez les noms et l’emplacement des espaces de noms dans lesquels les classes sources sont situées avec le qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="d06d2-118">Définissez les propriétés qui mappent aux propriétés dans les classes sources avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="d06d2-119">Si nécessaire, vous pouvez marquer l’une des propriétés comme appartenant à une classe source à l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="d06d2-120">Définissez les propriétés de clé des classes sources de votre classe d’affichage Union.</span><span class="sxs-lookup"><span data-stu-id="d06d2-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="d06d2-121">Chaque classe source doit avoir le même nombre de propriétés de clé correspondant à [**CimType**](swbemproperty-cimtype.md).</span><span class="sxs-lookup"><span data-stu-id="d06d2-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="d06d2-122">En outre, les clés de votre classe d’affichage d’Union doivent identifier toutes les instances de la source de manière unique.</span><span class="sxs-lookup"><span data-stu-id="d06d2-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="d06d2-123">Dans certains cas, vous devrez peut-être spécifier des propriétés système pour vous assurer que les instances sont uniques.</span><span class="sxs-lookup"><span data-stu-id="d06d2-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="d06d2-124">Par exemple, si vous créez une vue à partir de l’Union de deux classes identiques dans deux espaces de noms différents, vous pouvez inclure la propriété d' [**\_ \_ espace de noms**](--namespace.md) en tant que clé dans la classe de vue pour différencier les deux instances.</span><span class="sxs-lookup"><span data-stu-id="d06d2-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="d06d2-125">Si vous utilisez deux classes similaires du même espace de noms pour créer une vue, vous pouvez utiliser la propriété de la **\_ \_ classe** pour faire la distinction entre les deux.</span><span class="sxs-lookup"><span data-stu-id="d06d2-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="d06d2-126">Renommez les propriétés système dans la vue afin d’éviter un conflit avec les propriétés système de la classe d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d06d2-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="d06d2-127">Définissez les méthodes souhaitées à l’aide du qualificateur [**MethodSource**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="d06d2-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="d06d2-128">Contrairement aux autres classes d’affichage, vous pouvez créer des méthodes pour modifier une vue d’Union.</span><span class="sxs-lookup"><span data-stu-id="d06d2-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="d06d2-129">L’exemple de code suivant décrit une classe d’affichage Union.</span><span class="sxs-lookup"><span data-stu-id="d06d2-129">The following code example describes a union view class.</span></span>

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

 

 



