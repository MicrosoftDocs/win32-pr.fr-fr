---
description: Si vous tentez de supprimer plusieurs éléments dans une collection, vous constaterez peut-être que certains éléments ne sont pas supprimés.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Suppression de plusieurs éléments d’une collection WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524479"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Suppression de plusieurs éléments d’une collection WMI

Si vous tentez de supprimer plusieurs éléments dans une collection, vous constaterez peut-être que certains éléments ne sont pas supprimés. Vous ne pouvez pas itérer une collection lors de la suppression d’éléments, car lorsque vous supprimez un élément d’une collection, le pointeur de collection est déplacé vers l’élément suivant. Par exemple, une tentative de suppression de tous les éléments d’une collection entraîne la suppression de tous les autres éléments. Vous pouvez voir ce problème lorsque vous supprimez des éléments avec les méthodes [**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md) ou [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) . Vous pouvez éviter ce problème en effectuant une boucle dans la collection et en plaçant les noms des éléments à supprimer dans un tableau. Vous pouvez ensuite parcourir le tableau et supprimer les éléments nommés dans le tableau. Les collections, telles que [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)et [**SWbemRefresher**](swbemrefresher.md), disposent également d’une méthode qui supprime tous les éléments du conteneur d’actualisation.

Le script suivant montre comment supprimer plusieurs éléments d’une collection.


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



Vous ne pouvez pas supprimer des propriétés et des qualificateurs dans une instance de classe ou une classe dérivée qui a des propriétés héritées. Une telle tentative de suppression génère une erreur et la propriété ou le qualificateur n’est pas supprimé ; au lieu de cela, WMI rétablit la valeur par défaut de la propriété ou du qualificateur. Dans le cas d’une classe dérivée avec des propriétés héritées, WMI rétablit la valeur par défaut de la propriété héritée de la propriété dans la classe parente.

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md), [accès à une collection](accessing-a-collection.md)et [Suppression d’un seul élément d’une collection](removing-a-single-item-from-a-collection.md).

 

 



