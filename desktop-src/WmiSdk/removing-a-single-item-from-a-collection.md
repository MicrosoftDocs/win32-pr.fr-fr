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
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Suppression d’un seul élément d’une collection WMI

L’un des principaux objectifs de l’accès à une collection est de supprimer un élément de la collection. Vous pouvez supprimer un élément d’une collection à l’aide d’un appel à la méthode [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) . Cette méthode n’est pas disponible pour [**SWbemObjectSet**](swbemobjectset.md) ou [**SWbemMethodSet**](swbemmethodset.md).

Les éléments sont supprimés par nom de [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)et [**SWbemNamedValueSet**](swbemnamedvalueset.md). Toutefois, les éléments dans [**SWbemRefresher**](swbemrefresher.md) sont supprimés par index et à partir de [**SWbemPrivilegeSet**](swbemprivilegeset.md) par la constante qui représente le nom de privilège.

**Pour supprimer un élément d’une collection**

-   L’exemple de code suivant montre comment supprimer l’élément avec un appel à la méthode [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    L’exemple suivant crée une nouvelle classe nommée « NewClass » dans l' \\ espace de noms racine par défaut et lui ajoute trois propriétés. Le script utilise ensuite le code de l’exemple précédent pour supprimer la deuxième propriété.

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

    

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md), [accès à une collection](accessing-a-collection.md)et [Suppression de plusieurs éléments d’une collection](removing-multiple-items-from-a-collection.md).

 

 



