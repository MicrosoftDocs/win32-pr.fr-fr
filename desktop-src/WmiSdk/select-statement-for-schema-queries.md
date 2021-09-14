---
description: Les requêtes de données de schéma utilisent l’instruction SELECT avec une syntaxe similaire à celle utilisée pour les requêtes de données.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916920"
---
# <a name="select-statement-for-schema-queries"></a>Instruction SELECT pour les requêtes de schéma

Les requêtes de données de schéma utilisent l’instruction SELECT avec une syntaxe similaire à celle utilisée pour les [requêtes de données](select-statement-for-data-queries.md). La différence est l’utilisation d’une classe spéciale appelée « meta \_ Class », qui identifie la requête en tant que requête de schéma.

L’exemple suivant demande toutes les définitions de classe qui se trouvent dans l’espace de noms actuel.


```sql
SELECT * FROM meta_class
```



Les requêtes de schéma prennent uniquement en charge « \* ». Pour limiter l’étendue des définitions retournées, un fournisseur peut ajouter une clause WHERE qui spécifie une classe particulière.

L’exemple suivant montre comment ajouter une clause WHERE pour spécifier une classe particulière.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



La propriété **\_ \_ spéciale appelée identifie** la classe cible d’une requête de schéma. Notez que l’opérateur ISA doit être utilisé avec la propriété **\_ \_ This** pour demander des définitions pour les sous-classes de la classe cible. La requête ci-dessus retourne la définition de la classe et des définitions de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pour toutes ses sous-classes.

L’exemple suivant montre comment demander une définition de classe pour une classe unique à l’aide de la propriété système de **\_ \_ classe** .


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Cette requête équivaut à appeler la méthode [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) avec le paramètre Path de l’objet défini sur « Win32 \_ LogicalDisk ».

L’exemple de code VBScript suivant récupère toutes les classes enfants d’une classe WMI de niveau supérieur. La \_ \_ propriété système WMI Dynasty contient le nom de la classe de niveau supérieur à partir de laquelle une classe est dérivée, que vous pouvez utiliser pour récupérer toutes les classes d’un espace de noms dérivé d’une classe de niveau supérieur, y compris cette classe.


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



Le VBScript suivant récupère des classes enfants immédiates pour une classe WMI.


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



Le VBScript suivant récupère les classes de niveau supérieur. Pour toutes les classes de niveau supérieur dans un espace de noms WMI, la \_ \_ propriété système de la superclasse est null. Par conséquent, il est possible de récupérer les classes de niveau supérieur en recherchant une superclasse null.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
