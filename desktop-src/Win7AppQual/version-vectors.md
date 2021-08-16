---
description: Un vecteur de version traite les commentaires conditionnels dans une page Web HTML. Autrement dit, les vecteurs de version vous permettent de créer un balisage basé sur la version du navigateur.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vecteurs de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ba3fb77d13ce6aa08a095f4ae95e88c1ffaecf57251b7d9ad718f51be3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328605"
---
# <a name="version-vectors"></a>Vecteurs de version

Un *vecteur de version* traite les commentaires conditionnels dans une page Web HTML. Autrement dit, les vecteurs de version vous permettent de créer un balisage basé sur la version du navigateur.

Considérez l’exemple de code suivant.


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



dans ce cas, si la Windows version du navigateur Internet Explorer est au moins 5,5, le paragraphe correspondant est affiché dans la page web. Bien que la première condition de cet exemple illustre la fonction des commentaires conditionnels, ces commentaires ne sont généralement pas utilisés pour afficher le balisage comme la première condition. Au lieu de cela, les commentaires conditionnels restants dans l’exemple précédent sont plus courants. Dans ces commentaires restants, les commentaires conditionnels utilisent une feuille de style différente pour chaque version différente du navigateur.

l’exemple de code précédent vérifie également l’égalité pour Microsoft internet explorer 6 et Windows internet explorer 7. toutefois, pour Windows Internet Explorer 8, l’exemple utilise l’opérateur gte (supérieur ou égal à). Cet opérateur aide à la prochaine épreuve l’exemple afin que la version la plus conforme à la norme de la feuille de style soit utilisée lorsqu’une nouvelle version du navigateur est libérée (au lieu d’utiliser une feuille de style ou aucune feuille de style incorrecte). Souvent, les applications existantes ne considèrent pas une version d’Internet Explorer antérieure à 7 (ou la version la plus récente d’Internet Explorer pour laquelle le site est conçu). Pour plus d’informations sur les vecteurs de version, consultez [vecteurs de version](/previous-versions/cc817577(v=msdn.10)) dans MSDN Library.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



