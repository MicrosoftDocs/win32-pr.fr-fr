---
description: Les requêtes de données de schéma utilisent l’instruction SELECT avec une syntaxe similaire à celle utilisée pour les requêtes de données.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210202"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="7017b-103">Instruction SELECT pour les requêtes de schéma</span><span class="sxs-lookup"><span data-stu-id="7017b-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="7017b-104">Les requêtes de données de schéma utilisent l’instruction SELECT avec une syntaxe similaire à celle utilisée pour les [requêtes de données](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="7017b-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="7017b-105">La différence est l’utilisation d’une classe spéciale appelée « meta \_ Class », qui identifie la requête en tant que requête de schéma.</span><span class="sxs-lookup"><span data-stu-id="7017b-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="7017b-106">L’exemple suivant demande toutes les définitions de classe qui se trouvent dans l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="7017b-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="7017b-107">Les requêtes de schéma prennent uniquement en charge « \* ».</span><span class="sxs-lookup"><span data-stu-id="7017b-107">Schema queries only support "\*".</span></span> <span data-ttu-id="7017b-108">Pour limiter l’étendue des définitions retournées, un fournisseur peut ajouter une clause WHERE qui spécifie une classe particulière.</span><span class="sxs-lookup"><span data-stu-id="7017b-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="7017b-109">L’exemple suivant montre comment ajouter une clause WHERE pour spécifier une classe particulière.</span><span class="sxs-lookup"><span data-stu-id="7017b-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="7017b-110">La propriété **\_ \_ spéciale appelée identifie** la classe cible d’une requête de schéma.</span><span class="sxs-lookup"><span data-stu-id="7017b-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="7017b-111">Notez que l’opérateur ISA doit être utilisé avec la propriété **\_ \_ This** pour demander des définitions pour les sous-classes de la classe cible.</span><span class="sxs-lookup"><span data-stu-id="7017b-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="7017b-112">La requête ci-dessus retourne la définition de la classe et des définitions de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pour toutes ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="7017b-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="7017b-113">L’exemple suivant montre comment demander une définition de classe pour une classe unique à l’aide de la propriété système de **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="7017b-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="7017b-114">Cette requête équivaut à appeler la méthode [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) avec le paramètre Path de l’objet défini sur « Win32 \_ LogicalDisk ».</span><span class="sxs-lookup"><span data-stu-id="7017b-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="7017b-115">L’exemple de code VBScript suivant récupère toutes les classes enfants d’une classe WMI de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7017b-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="7017b-116">La \_ \_ propriété système WMI Dynasty contient le nom de la classe de niveau supérieur à partir de laquelle une classe est dérivée, que vous pouvez utiliser pour récupérer toutes les classes d’un espace de noms dérivé d’une classe de niveau supérieur, y compris cette classe.</span><span class="sxs-lookup"><span data-stu-id="7017b-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="7017b-117">Le VBScript suivant récupère des classes enfants immédiates pour une classe WMI.</span><span class="sxs-lookup"><span data-stu-id="7017b-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="7017b-118">Le VBScript suivant récupère les classes de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7017b-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="7017b-119">Pour toutes les classes de niveau supérieur dans un espace de noms WMI, la \_ \_ propriété système de la superclasse est null.</span><span class="sxs-lookup"><span data-stu-id="7017b-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="7017b-120">Par conséquent, il est possible de récupérer les classes de niveau supérieur en recherchant une superclasse null.</span><span class="sxs-lookup"><span data-stu-id="7017b-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
