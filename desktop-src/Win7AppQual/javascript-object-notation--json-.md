---
description: JSON (JavaScript Object Notation)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JSON (JavaScript Object Notation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088187"
---
# <a name="javascript-object-notation-json"></a>JSON (JavaScript Object Notation)

[JavaScript Object Notation (JSON)](https://www.json.org/) est un format d’échange de données simple et léger basé sur un sous-ensemble de la notation de littéral d’objet du langage JavaScript. Le moteur JavaScript de Windows Internet Explorer 8 implémente la [proposition json 3,1 JSON](https://www.ecma-international.org/) pour les fonctions de gestion JSON natives (qui utilisent [l’API json2.js de Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).

Internet Explorer 8 comprend un objet JSON natif qui est conforme à la prise en charge de JSON décrite dans le [brouillon de travail](https://www.ecma-international.org/)de la proposition de la version 3.1. Certaines pages Web détectent l’objet JSON natif, puis l’utilisent de manière non standard. Cette utilisation provoque généralement une erreur de script et interrompt la gestion des demandes AJAX. L’exemple de code suivant montre une façon incorrecte d’utiliser l’objet JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Au lieu de cela, l’exemple de code suivant montre une bonne façon d’utiliser l’objet JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer inclut des prises en charge natives pour JSON en introduisant un objet JSON global qui a deux méthodes intégrées : **stringify** et **Parse**. L’objet JSON global est défini dans le moteur JavaScript et est créé au cours de la phase d’initialisation du moteur. Pour assurer la compatibilité descendante, cette fonctionnalité est disponible uniquement quand un site Web utilise la dernière version des fonctionnalités JavaScript en utilisant le mode de disposition (document) « normes Internet Explorer 8 ». Cette fonctionnalité peut également affecter le comportement des pages Web qui dépendent d’une variable globale JSON ou utilisent [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Vous pouvez remplacer l’objet JSON global. Mais lorsqu’une page Web utilise le mode de disposition (document) « normes Internet Explorer 8 », il ne s’agit plus d’un objet non défini. Étant donné que JSON est instancié comme un nom global par le moteur JavaScript, vérifie que « if ( ! this.JSON) » prend la valeur false et doit être modifié dans le code utilisateur.

Les pages Web qui utilisent [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) ne sont probablement pas affectées. À quelques exceptions près, ces pages devraient fonctionner plus rapidement. Les exceptions sont dues aux différences entre l’implémentation du format JSON natif d’Internet Explorer et json2.js. Par exemple, lors de la sérialisation, l’implémentation JSON Native détecte les cycles et ne passe pas par une récurrence infinie comme json.js. Pour plus d’informations sur ces exceptions, consultez les [blogs JavaScript](/archive/blogs/jscript/).

Pour plus d’informations, consultez [documentation JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) et contrôle [de version et prise en charge des versions du moteur JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
