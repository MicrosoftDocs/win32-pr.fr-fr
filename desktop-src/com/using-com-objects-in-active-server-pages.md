---
title: Utilisation d’objets COM dans des pages Active Server
description: Vous pouvez générer des scripts d’objets COM dans des applications ASP (Active Server Pages).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519349"
---
# <a name="using-com-objects-in-active-server-pages"></a>Utilisation d’objets COM dans des pages Active Server

Vous pouvez générer des scripts d’objets COM dans des applications ASP (Active Server Pages). Pour ce faire, vous devez d’abord créer une instance de l’objet à l’aide de la balise OBJECT ou en appelant la méthode CreateObject de l’objet serveur ASP. Une fois qu’un objet COM a été créé, vous pouvez l’utiliser dans les scripts suivants sur la page ASP.

À l’aide d’ASP, vous pouvez travailler avec différents types de moteurs de script, chacun prenant en charge un langage de script différent. ASP est fourni avec des moteurs de script VBScript et JScript. Vous pouvez également intégrer des moteurs de script développés par d’autres entreprises pour prendre en charge des langages tels que PerlScript, PScript, Python et d’autres.

Si vous ne définissez pas le langage de script pour une page ASP, VBScript est la valeur par défaut. Pour spécifier un langage de script autre que VBScript, ajoutez une ligne telle que la suivante en haut de chaque page ASP :

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Pour utiliser un objet COM dans une page ASP, vous devez d’abord créer une instance de cet objet. Pour ce faire, utilisez la balise OBJECT et spécifiez la valeur « SERVER » pour l’attribut RUNAT, comme indiqué dans l’exemple suivant. Par défaut, la balise OBJECT crée une instance de l’objet sur le client. L’affectation de la valeur SERVER à l’attribut RUNAT entraîne la création de l’objet sur le serveur. L’objet doit s’exécuter sur le serveur afin d’être utilisé par ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

Vous pouvez également créer une instance d’un objet COM sur une page ASP en appelant la méthode CreateObject de l’objet serveur ASP. L’utilisation de Server. CreateObject est plus lente que la création de l’objet à l’aide d’une balise OBJECT, mais elle est légèrement plus lisible, car elle spécifie l’identificateur programmatique au lieu de l’identificateur de classe de l’objet COM. L’objet serveur est exposé par ASP et n’a pas besoin d’être créé. L’appel de Server. CreateObject est illustré dans les exemples suivants. Le premier exemple est VBScript :

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

L’exemple suivant est JScript :

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

L’appel de CreateObject est plus lent que l’utilisation de la balise OBJECT pour créer un objet COM. Dans les applications où les performances sont critiques, vous devez utiliser la balise OBJECT.

Une fois que vous avez créé une instance de l’objet COM, vous pouvez l’utiliser dans des scripts. Cela est illustré dans l’exemple VBScript suivant, qui définit la valeur de la propriété border de l’objet COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de scripts avec des objets COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




