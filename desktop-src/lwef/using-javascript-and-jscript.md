---
title: Utilisation de JavaScript et de JScript
description: Utilisation de JavaScript et de JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101589"
---
# <a name="using-javascript-and-jscript"></a>Utilisation de JavaScript et de JScript

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Si vous utilisez JavaScript ou Microsoft JScript pour accéder à l’interface de programmation de Microsoft Agent, suivez les conventions de ce langage pour spécifier des méthodes ou des propriétés :

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

Pour accéder aux collections d’objets de l’agent, utilisez la fonction d' [**énumérateur**](https://www.bing.com/search?q=**Enumerator**) JScript. Toutefois, les versions de JScript incluses avant Internet Explorer 4,0 ne prennent pas en charge cette fonction et ne prennent pas en charge les collections. Pour accéder aux méthodes et aux propriétés de l’objet [**character**](/windows/desktop/lwef/the-characters-object) , utilisez la méthode [**caractère**](character-method.md) . De même, pour accéder aux propriétés d’un objet [**Command**](/windows/desktop/lwef/the-command-object) , utilisez la méthode [**Command**](command-method.md) .

 

 