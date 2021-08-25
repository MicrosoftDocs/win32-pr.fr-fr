---
title: Utilisation de JavaScript et de JScript
description: Utilisation de JavaScript et de JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960679"
---
# <a name="using-javascript-and-jscript"></a>Utilisation de JavaScript et de JScript

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

si vous utilisez JavaScript ou microsoft JScript pour accéder à l’interface de programmation de microsoft Agent, suivez les conventions de ce langage pour spécifier des méthodes ou des propriétés :

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript n’a actuellement pas de syntaxe d’événement pour les objets non HTML. Toutefois, avec Internet Explorer, vous pouvez utiliser les `<SCRIPT>` balises **pour...** Syntaxe de l’événement :

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Dans la mesure où tous les navigateurs ne prennent pas en charge cette syntaxe d’événement, vous souhaiterez peut-être utiliser JavaScript uniquement pour les pages qui prennent en charge Microsoft Internet Explorer ou pour du code qui ne requiert pas de gestion des événements.

pour accéder aux collections d’objets de l’Agent, utilisez la fonction d' [**énumérateur**](https://www.bing.com/search?q=**Enumerator**) JScript. toutefois, les versions de JScript incluses avant Internet Explorer 4,0 ne prennent pas en charge cette fonction et ne prennent pas en charge les collections. Pour accéder aux méthodes et aux propriétés de l’objet [**character**](/windows/desktop/lwef/the-characters-object) , utilisez la méthode [**caractère**](character-method.md) . De même, pour accéder aux propriétés d’un objet [**Command**](/windows/desktop/lwef/the-command-object) , utilisez la méthode [**Command**](command-method.md) .

 

 