---
description: L’un des principaux objectifs de l’accès à une collection est de supprimer un élément de la collection. Vous pouvez supprimer un élément d’une collection à l’aide d’un appel à la méthode SWbemPropertySet. Remove. Cette méthode n’est pas disponible pour SWbemObjectSet ou SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Suppression d’un seul élément d’une collection WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527811"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="dccad-105">Suppression d’un seul élément d’une collection WMI</span><span class="sxs-lookup"><span data-stu-id="dccad-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="dccad-106">L’un des principaux objectifs de l’accès à une collection est de supprimer un élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="dccad-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="dccad-107">Vous pouvez supprimer un élément d’une collection à l’aide d’un appel à la méthode [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="dccad-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="dccad-108">Cette méthode n’est pas disponible pour [**SWbemObjectSet**](swbemobjectset.md) ou [**SWbemMethodSet**](swbemmethodset.md).</span><span class="sxs-lookup"><span data-stu-id="dccad-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="dccad-109">Les éléments sont supprimés par nom de [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)et [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span><span class="sxs-lookup"><span data-stu-id="dccad-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="dccad-110">Toutefois, les éléments dans [**SWbemRefresher**](swbemrefresher.md) sont supprimés par index et à partir de [**SWbemPrivilegeSet**](swbemprivilegeset.md) par la constante qui représente le nom de privilège.</span><span class="sxs-lookup"><span data-stu-id="dccad-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="dccad-111">**Pour supprimer un élément d’une collection**</span><span class="sxs-lookup"><span data-stu-id="dccad-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="dccad-112">L’exemple de code suivant montre comment supprimer l’élément avec un appel à la méthode [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="dccad-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="dccad-113">L’exemple suivant crée une nouvelle classe nommée « NewClass » dans l' \\ espace de noms racine par défaut et lui ajoute trois propriétés.</span><span class="sxs-lookup"><span data-stu-id="dccad-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="dccad-114">Le script utilise ensuite le code de l’exemple précédent pour supprimer la deuxième propriété.</span><span class="sxs-lookup"><span data-stu-id="dccad-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="dccad-115">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md), [accès à une collection](accessing-a-collection.md)et [Suppression de plusieurs éléments d’une collection](removing-multiple-items-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="dccad-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



