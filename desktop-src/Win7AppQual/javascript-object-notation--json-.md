---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JSON (JavaScript Object Notation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203364"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="09325-103">JSON (JavaScript Object Notation)</span><span class="sxs-lookup"><span data-stu-id="09325-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="09325-104">[JavaScript Object Notation (JSON)](https://www.json.org/) est un format d’échange de données simple et léger basé sur un sous-ensemble de la notation de littéral d’objet du langage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="09325-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="09325-105">Le moteur JavaScript de Windows Internet Explorer 8 implémente la [proposition json 3,1 JSON](https://www.ecma-international.org/) pour les fonctions de gestion JSON natives (qui utilisent [l’API json2.js de Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span><span class="sxs-lookup"><span data-stu-id="09325-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="09325-106">Internet Explorer 8 comprend un objet JSON natif qui est conforme à la prise en charge de JSON décrite dans le [brouillon de travail](https://www.ecma-international.org/)de la proposition de la version 3.1.</span><span class="sxs-lookup"><span data-stu-id="09325-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="09325-107">Certaines pages Web détectent l’objet JSON natif, puis l’utilisent de manière non standard.</span><span class="sxs-lookup"><span data-stu-id="09325-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="09325-108">Cette utilisation provoque généralement une erreur de script et interrompt la gestion des demandes AJAX.</span><span class="sxs-lookup"><span data-stu-id="09325-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="09325-109">L’exemple de code suivant montre une façon incorrecte d’utiliser l’objet JSON.</span><span class="sxs-lookup"><span data-stu-id="09325-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="09325-110">Au lieu de cela, l’exemple de code suivant montre une bonne façon d’utiliser l’objet JSON.</span><span class="sxs-lookup"><span data-stu-id="09325-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="09325-111">Windows Internet Explorer inclut des prises en charge natives pour JSON en introduisant un objet JSON global qui a deux méthodes intégrées : **stringify** et **Parse**.</span><span class="sxs-lookup"><span data-stu-id="09325-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="09325-112">L’objet JSON global est défini dans le moteur JavaScript et est créé au cours de la phase d’initialisation du moteur.</span><span class="sxs-lookup"><span data-stu-id="09325-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="09325-113">Pour assurer la compatibilité descendante, cette fonctionnalité est disponible uniquement quand un site Web utilise la dernière version des fonctionnalités JavaScript en utilisant le mode de disposition (document) « normes Internet Explorer 8 ».</span><span class="sxs-lookup"><span data-stu-id="09325-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="09325-114">Cette fonctionnalité peut également affecter le comportement des pages Web qui dépendent d’une variable globale JSON ou utilisent [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="09325-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="09325-115">Vous pouvez remplacer l’objet JSON global.</span><span class="sxs-lookup"><span data-stu-id="09325-115">You can override the global JSON object.</span></span> <span data-ttu-id="09325-116">Mais lorsqu’une page Web utilise le mode de disposition (document) « normes Internet Explorer 8 », il ne s’agit plus d’un objet non défini.</span><span class="sxs-lookup"><span data-stu-id="09325-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="09325-117">Étant donné que JSON est instancié comme un nom global par le moteur JavaScript, vérifie que « if ( ! this.JSON) » prend la valeur false et doit être modifié dans le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09325-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="09325-118">Les pages Web qui utilisent [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) ne sont probablement pas affectées.</span><span class="sxs-lookup"><span data-stu-id="09325-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="09325-119">À quelques exceptions près, ces pages devraient fonctionner plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="09325-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="09325-120">Les exceptions sont dues aux différences entre l’implémentation du format JSON natif d’Internet Explorer et json2.js.</span><span class="sxs-lookup"><span data-stu-id="09325-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="09325-121">Par exemple, lors de la sérialisation, l’implémentation JSON Native détecte les cycles et ne passe pas par une récurrence infinie comme json.js.</span><span class="sxs-lookup"><span data-stu-id="09325-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="09325-122">Pour plus d’informations sur ces exceptions, consultez les [blogs JavaScript](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="09325-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="09325-123">Pour plus d’informations, consultez [documentation JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) et contrôle [de version et prise en charge des versions du moteur JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span><span class="sxs-lookup"><span data-stu-id="09325-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09325-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09325-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09325-125">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="09325-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
