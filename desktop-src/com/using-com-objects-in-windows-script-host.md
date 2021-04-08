---
title: Utilisation d’objets COM dans Windows Script Host
description: Microsoft Windows Script Host est un utilitaire de script que vous pouvez utiliser pour exécuter des scripts dans le système d’exploitation de base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761587"
---
# <a name="using-com-objects-in-windows-script-host"></a>Utilisation d’objets COM dans Windows Script Host

Microsoft Windows Script Host est un utilitaire de script que vous pouvez utiliser pour exécuter des scripts dans le système d’exploitation de base. Vous pouvez utiliser Windows Script Host pour automatiser les tâches courantes et créer des macros et des scripts d’ouverture de session performants. Windows Script Host est fourni avec les moteurs de script ActiveX VBScript et JScript. D’autres éditeurs de logiciels fournissent des moteurs de script ActiveX pour les langages tels que PerlScript, PScript, Python, etc.

Pour utiliser un objet COM dans un script exécuté par Windows Script Host, vous devez d’abord créer une instance de l’objet. Après avoir créé un objet COM, vous pouvez l’utiliser dans des scripts.

Windows Script Host se compose de deux applications. L’une exécute des scripts à partir du bureau Windows ( `WScript.exe` ); l’autre exécute des scripts à partir de l’invite de commandes ( `CScript.exe` ).

Pour exécuter un script à partir du bureau, double-cliquez simplement sur un fichier de script. Les fichiers de script sont des fichiers texte. Par Convention, les fichiers VBScript ont l’extension `.vbs` et les fichiers JScript `.js` .

Pour exécuter un script à partir de l’invite de commandes, exécutez l' `Cscript.exe` application avec une ligne de commande telle que la suivante :

```console
cscript "c:\\sample scripts\\chart.vbs"
```

où `c:\\sample scripts\\chart.vbs` est le chemin d’accès au fichier contenant le script.

Vous pouvez imprimer une liste des paramètres pris en charge par Cscript.exe en entrant la ligne de commande suivante :

```console
call cscript //?
```

Pour utiliser un objet COM dans un script exécuté par Windows Script Host, vous devez d’abord créer une instance de l’objet. Dans VBScript, vous pouvez effectuer cette opération en appelant la `CreateObject()` méthode. En JScript, il est possible d’utiliser l' `ActiveXObject` objet ou la `WScript.CreateObject()` méthode. L’exemple suivant illustre l’appel `CreateObject()` à l’aide de VBScript :


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



L’exemple suivant illustre la création d’un `ActiveXObject` objet à l’aide de JScript :


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
Vous pouvez également utiliser la `WScript.CreateObject()` méthode dans JScript :

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Après avoir créé une instance de l’objet COM, vous pouvez écrire un script qui utilise l’objet, par exemple :


```VB
objXL.Visible = true;
 
```



En plus de la méthode CreateObject et de l’objet ActiveXObject, VBScript et JScript fournissent la méthode GetObject, qui retourne une instance d’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de scripts avec des objets COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




