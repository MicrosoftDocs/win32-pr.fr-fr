---
description: Un alias dans WMI est une référence symbolique dans une classe ou une instance de classe située ailleurs dans un fichier format MOF (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Création d’un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517009"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="59db4-103">Création d’un alias WMI</span><span class="sxs-lookup"><span data-stu-id="59db4-103">Creating a WMI Alias</span></span>

<span data-ttu-id="59db4-104">Un [*alias*](gloss-a.md) dans WMI est une référence symbolique dans une classe ou une instance de classe située ailleurs dans un fichier format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="59db4-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="59db4-105">Le compilateur MOF utilise des alias pour établir des références entre les classes et les instances.</span><span class="sxs-lookup"><span data-stu-id="59db4-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="59db4-106">Le compilateur résout les alias des classes auxquelles ils font référence. par conséquent, les noms d’alias ne sont pas disponibles dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="59db4-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="59db4-107">Par conséquent, les applications clientes ne peuvent pas faire référence à des classes à l’aide d’alias.</span><span class="sxs-lookup"><span data-stu-id="59db4-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="59db4-108">WMI prend en charge les alias de référence en avant, mais pas les alias circulaires.</span><span class="sxs-lookup"><span data-stu-id="59db4-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="59db4-109">Un alias a uniquement une portée dans le fichier MOF dans lequel vous déclarez l’alias.</span><span class="sxs-lookup"><span data-stu-id="59db4-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="59db4-110">Par conséquent, vous utilisez généralement un alias comme raccourci vers un long chemin d’accès d’objet.</span><span class="sxs-lookup"><span data-stu-id="59db4-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="59db4-111">**Pour définir un alias**</span><span class="sxs-lookup"><span data-stu-id="59db4-111">**To define an alias**</span></span>

1.  <span data-ttu-id="59db4-112">Ajoutez l’expression « As $*aliasname*» à la déclaration de classe ou d’instance.</span><span class="sxs-lookup"><span data-stu-id="59db4-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="59db4-113">Les noms d’alias suivent les mêmes règles que les noms d’instance et de classe, sauf que les noms d’alias doivent commencer par un signe dollar ($).</span><span class="sxs-lookup"><span data-stu-id="59db4-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="59db4-114">Les traits de soulignement peuvent apparaître dans un nom d’alias à la suite du caractère initial.</span><span class="sxs-lookup"><span data-stu-id="59db4-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="59db4-115">L’exemple de code suivant décrit comment utiliser un alias dans une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="59db4-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="59db4-116">Les exemples de code suivants décrivent comment utiliser un alias comme référence symbolique à un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="59db4-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="59db4-117">Ces exemples déclarent deux classes pour décrire un disque : la classe Disk pour indiquer la lettre de lecteur et la classe DiskRef pour indiquer le chemin d’accès au disque.</span><span class="sxs-lookup"><span data-stu-id="59db4-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="59db4-118">Un alias est défini pour l’instance de classe de disque.</span><span class="sxs-lookup"><span data-stu-id="59db4-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="59db4-119">Cet alias est utilisé comme valeur pour la propriété PathToDisk dans l’instance DiskRef.</span><span class="sxs-lookup"><span data-stu-id="59db4-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="59db4-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59db4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59db4-121">Création d’une classe</span><span class="sxs-lookup"><span data-stu-id="59db4-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



