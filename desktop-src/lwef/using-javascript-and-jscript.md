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
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="09e58-103">Utilisation de JavaScript et de JScript</span><span class="sxs-lookup"><span data-stu-id="09e58-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="09e58-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09e58-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="09e58-105">Si vous utilisez JavaScript ou Microsoft JScript pour accéder à l’interface de programmation de Microsoft Agent, suivez les conventions de ce langage pour spécifier des méthodes ou des propriétés :</span><span class="sxs-lookup"><span data-stu-id="09e58-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="09e58-106">JavaScript n’a actuellement pas de syntaxe d’événement pour les objets non HTML.</span><span class="sxs-lookup"><span data-stu-id="09e58-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="09e58-107">Toutefois, avec Internet Explorer, vous pouvez utiliser les `<SCRIPT>` balises **pour...** Syntaxe de l’événement :</span><span class="sxs-lookup"><span data-stu-id="09e58-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="09e58-108">Dans la mesure où tous les navigateurs ne prennent pas en charge cette syntaxe d’événement, vous souhaiterez peut-être utiliser JavaScript uniquement pour les pages qui prennent en charge Microsoft Internet Explorer ou pour du code qui ne requiert pas de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="09e58-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="09e58-109">Pour accéder aux collections d’objets de l’agent, utilisez la fonction d' [**énumérateur**](https://www.bing.com/search?q=**Enumerator**) JScript.</span><span class="sxs-lookup"><span data-stu-id="09e58-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="09e58-110">Toutefois, les versions de JScript incluses avant Internet Explorer 4,0 ne prennent pas en charge cette fonction et ne prennent pas en charge les collections.</span><span class="sxs-lookup"><span data-stu-id="09e58-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="09e58-111">Pour accéder aux méthodes et aux propriétés de l’objet [**character**](/windows/desktop/lwef/the-characters-object) , utilisez la méthode [**caractère**](character-method.md) .</span><span class="sxs-lookup"><span data-stu-id="09e58-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="09e58-112">De même, pour accéder aux propriétés d’un objet [**Command**](/windows/desktop/lwef/the-command-object) , utilisez la méthode [**Command**](command-method.md) .</span><span class="sxs-lookup"><span data-stu-id="09e58-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 