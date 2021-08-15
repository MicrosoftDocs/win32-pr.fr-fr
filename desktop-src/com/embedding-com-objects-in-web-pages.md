---
title: Incorporation d’objets COM dans des pages Web
description: Vous pouvez utiliser des objets COM dans des pages Web. Pour ce faire, commencez par créer une instance de cet objet COM. Une fois qu’une instance d’objet est créée, vous pouvez l’utiliser dans les scripts suivants sur cette page Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d13a92bd2de152e71ac4284ce37b977e8305f25dcb2aef5eb94d6019d115812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736890"
---
# <a name="embedding-com-objects-in-web-pages"></a>Incorporation d’objets COM dans des pages Web

Vous pouvez utiliser des objets COM dans des pages Web. Pour ce faire, commencez par créer une instance de cet objet COM. Une fois qu’une instance d’objet est créée, vous pouvez l’utiliser dans les scripts suivants sur cette page Web.

Pour créer une instance d’objet COM dans une page Web, vous pouvez utiliser une balise d’objet. Si votre langage de script fournit une méthode native pour créer des objets COM, vous pouvez également créer une instance d’objet à l’aide d’un script.

notez que l’incorporation d’objets COM dans des pages web fonctionne uniquement avec les navigateurs qui prennent en charge ActiveX et COM, par exemple Internet Explorer.

L’exemple suivant illustre l’utilisation de la balise OBJECT pour incorporer un objet COM dans une page Web :

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

Vous pouvez également créer une instance d’objet COM dans un script, si votre langage de script permet de créer des objets COM. par exemple, VBScript fournit la méthode CreateObject et JScript fournit l’objet ActiveXObject. La création d’objets dans le script est illustrée dans les exemples suivants.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

en plus de la méthode CreateObject et de l’objet ActiveXObject, VBScript et JScript fournissent la méthode GetObject, qui retourne une instance d’objet.

Une fois qu’un objet COM a été créé, vous pouvez le référencer dans les scripts suivants à l’aide de l’identificateur spécifié dans l’attribut ID de la balise d’objet. Dans l’exemple précédent, cet identificateur a été spécifié en tant que « vid ». Notez que le script qui utilise l’objet COM doit apparaître après la balise d’objet ou le script qui crée l’instance d’objet ; dans le cas contraire, l’identificateur d’objet n’est pas défini. Le script suivant utilise l’objet objXL pour afficher les informations de version de Microsoft Excel.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Si vous écrivez des scripts incorporés dans une page Web, le navigateur expose également un modèle objet auquel vos scripts peuvent accéder. Le modèle utilisé par Internet Explorer est conforme au Document Object Model (DOM) proposé par le World Wide Web Consortium (W3C).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de scripts avec des objets COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




