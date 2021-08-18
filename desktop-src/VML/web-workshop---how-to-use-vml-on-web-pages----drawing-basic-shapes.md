---
title: Dessin de formes de base
description: cet article décrit le dessin de formes de base dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Atelier Web, formes de dessin
- conception de pages Web, dessin de formes
- Langage VML (VML), dessins, formes
- VML (langage VML), formes de dessin
- graphiques vectoriels, formes de dessin
- dessiner des formes
- Formes VML, dessin
- Langage VML (VML), XML
- VML (langage VML), XML
- graphiques vectoriels, XML
- Langage VML (VML), CSS2
- VML (langage VML), CSS2
- graphiques vectoriels, CSS2
- Langage VML (VML), éléments
- VML (langage VML), éléments
- graphiques vectoriels, éléments
- Éléments VML, formes de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4a8b7985371d9cffc6e7359cef1a17c69c403c7802de458b68d9df8c36e3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136922"
---
# <a name="drawing-basic-shapes"></a>Dessin de formes de base

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer combien il est facile de dessiner une forme à l’aide de VML.

Pour créer un ovale rouge sur une page Web, comme illustré dans l’image suivante, vous pouvez dessiner l’ovale à l’aide d’un outil d’édition graphique, enregistrer votre dessin en tant que bitmap, puis insérer l’image bitmap sur votre page Web :

![oval1.gif (627 octets)](images/oval1.gif)

Vous pouvez également utiliser VML pour dessiner des graphiques. Dans l’exemple précédent, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web pour dessiner l’ovale rouge :


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` et `</v:...>` sont les balises de début et de fin dans la [syntaxe XML](#xml-structure).`style='width:100pt; height:75pt'` fournit des [informations CSS](#css-information). **Oval** et **FillColor**= "Red" sont des [éléments VML](#vml-elements).

Vous pouvez modifier les graphiques en modifiant simplement leurs attributs de propriété dans VML. Dans l’exemple précédent, si vous remplacez `fillcolor="red"` par `fillcolor="blue"` , comme indiqué dans la représentation VML suivante, le ovale rouge passe en bleu :


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Les navigateurs qui prennent en charge le langage VML peuvent afficher et afficher les graphiques représentés dans VML sans avoir à télécharger des fichiers image distincts. La plupart des graphiques représentés dans VML sont rendus plus rapidement dans les navigateurs et nécessitent moins d’espace disque et le temps de téléchargement.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="xml-structure"></a>Structure XML

Le format VML est mis en forme en fonction des règles de Extensible Markup Language (XML). N’importe quel analyseur XML standard peut analyser le VML et transmettre les données résultantes à un processeur spécifique à VML. Pour permettre aux navigateurs de savoir comment transférer des données vers un processeur VML spécifique, vous devez taper des informations telles que les [espaces de noms](web-workshop---how-to-use-vml-on-web-pages----appendix.md) et les [objets personnalisés incorporés](web-workshop---how-to-use-vml-on-web-pages----appendix.md). Vous pouvez ensuite utiliser VML pour taper des graphiques dans la `<BODY>` région, comme vous l’avez fait dans l’exemple précédent.

Le `"v:"` préfixe de chaque balise XML identifie la balise en tant que Vml. Le `"v:"` préfixe de la `<BODY>` région doit être cohérent avec `<html xmlns:v="...">` .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="css-information"></a>Informations CSS

VML utilise [feuilles de style en cascade, niveau 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) pour déterminer la taille des graphiques et positionner les graphiques sur une page Web. Dans l’exemple précédent, nous avons spécifié la taille de l’ovale sous la forme de 100 points (largeur) de 75 points (hauteur) ( `style='width:100pt;height:75pt'` ).

[![retour au début ](images/top.gif) en haut](#top)

## <a name="vml-elements"></a>Éléments VML

Dans l’exemple précédent, nous avons utilisé un élément prédéfini VML `<oval>` pour dessiner un ovale. Nous avons ensuite utilisé l’attribut de propriété **FillColor** de l' `<oval>` élément pour remplir l’ovale en rouge.

En se basant sur les balises de [début, les balises de fin et les balises de Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) de la [spécification XML 1,0](https://www.w3.org/TR/REC-xml), les balises d’éléments vides peuvent être utilisées pour tout élément sans contenu. Par exemple, comme indiqué dans la représentation VML suivante, il n’y a aucun contenu (sous-élément) dans l' `<oval>` élément. (Notez que le **style** et **FillColor** sont les attributs de l' `<oval>` élément ; il ne s’agit pas de sous-éléments.)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Par conséquent, vous pouvez utiliser la balise d’élément vide, comme indiqué dans la représentation VML suivante, pour représenter la même chose que la ligne ci-dessus.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![retour au début ](images/top.gif) en haut](#top)

## <a name="summary"></a>Résumé

Vous pouvez utiliser VML pour dessiner des graphiques sur une page Web, puis personnaliser ces graphiques en modifiant simplement leurs attributs de propriété. En outre, la plupart des graphiques représentés dans VML sont rendus plus rapidement dans les navigateurs et prennent moins de temps de téléchargement et d’espace disque.

 

 