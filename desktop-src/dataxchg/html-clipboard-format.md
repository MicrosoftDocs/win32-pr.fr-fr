---
title: Format de presse-papiers HTML
description: Cette section décrit le format de presse-papiers HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Interface utilisateur, presse-papiers
- presse-papiers, découper des données
- presse-papiers, copier des données
- presse-papiers, coller des données
- presse-papiers, formats
- presse-papiers, format HTML
- presse-papiers, couper du texte HTML
- presse-papiers, coller du texte HTML
- Format du presse-papiers CF_HTML
- presse-papiers, format CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d73b5101d26fc55002d55e0c15144646b80445
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884985"
---
# <a name="html-clipboard-format"></a>Format de presse-papiers HTML

La configuration requise pour le transfert de texte HTML au moyen du presse-papiers diffère selon le scénario. Cet article s’intéresse à la coupe et au collage de fragments d’un document HTML. Il peut y avoir des conditions requises pour le transfert de documents HTML entiers dans le presse-papiers. Toutefois, cet article est piloté par une nécessité de transférer des fragments de texte HTML sélectionné. Par conséquent, une méthode qui nécessitait la copie de l’intégralité du document HTML dans le presse-papiers s’affiche comme trop haute.

Le \_ format de presse-papiers html CF permet de stocker un fragment de texte HTML brut et son contexte dans le presse-papiers au format ASCII. Cela permet au contexte du fragment HTML, qui se compose de toutes les balises précédentes, d’être examiné par une application afin que les balises environnantes du fragment HTML puissent être notées avec leurs attributs. Bien qu’il s’agisse d’applications pour décider de l’interprétation de tels fragments, certaines recommandations de base sont incluses ici en fonction des implémentations de IE4/MSHTML.

Le nom officiel du presse-papiers (la chaîne utilisée par RegisterClipboardFormat) est au format HTML.

-   [Description](#description)
-   [Scénarios](#scenarios)

## <a name="description"></a>Description

CF \_ HTML est un format de texte intégral (c’est-à-dire, entre autres choses, dans l’esprit html et utilise UTF-8) et comprend un `description` , un facultatif `context` et, dans le contexte, le `fragment` .

Voici un exemple de presse-papiers :


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



La description comprend le numéro de version et les décalages du presse-papiers, indiquant où le contexte et le début et la fin du fragment. La description est une liste de mots clés de texte ASCII (min/Maj n’est pas significative) suivie d’une chaîne et séparée par un signe deux-points ( :).

**Version**: numéro de version VV du presse-papiers. La version de démarrage est 0,9.

**StartHTML**: byteCount du début du presse-papiers jusqu’au début du contexte, ou-1 si aucun contexte n’est présent.

**Polydhtml**: byteCount du début du presse-papiers jusqu’à la fin du contexte, ou-1 si aucun contexte n’est présent.

**StartFragment**: byteCount du début du presse-papiers jusqu’au début du fragment.

**EndFragment**: byteCount du début du presse-papiers jusqu’à la fin du fragment.

**StartSelection**: byteCount du début du presse-papiers jusqu’au début de la sélection.

**EndSelection**: byteCount du début du presse-papiers jusqu’à la fin de la sélection.

Les mots clés StartSelection et EndSelection sont facultatifs et doivent tous deux être omis si vous ne souhaitez pas que l’application génère ces informations.

D’autres informations de ce genre peuvent être ajoutées ici plus tard, puisque le code HTML commence au StartHTMLoffset. Par exemple, plusieurs paires de StartFragment/EndFragment peuvent être ajoutées ultérieurement pour prendre en charge une sélection non contiguë de fragments.

Pour la commodité des programmes qui génèrent le bytecounts, les bytecounts peuvent être laissés remplis par des zéros. Par exemple, les programmes qui génèrent le bytecounts peuvent avoir un impact arbitraire sur dix (10) zéros pour chaque mot clé (StartHTML : 0000000000), puis, lorsque l’byteCount exact de StartHTML est connu (par exemple, 71), le programme peut remplacer le nombre approprié de zéros par le byteCount (StartHTML : 0000000071).

Le seul jeu de caractères pris en charge par le presse-papiers est Unicode dans son encodage UTF-8. Étant donné que les premiers caractères d’UTF-8 et d’ASCII correspondent, la description est toujours ASCII, mais les octets du contexte (à partir de StartHTML) peuvent utiliser n’importe quel autre caractère codé au format UTF-8.

La fin des lignes dans l’en-tête du format du presse-papiers peut être CR ou CR/LF ou LF.

Le fragment contient du code HTML pur et valide qui représente la zone sélectionnée par l’utilisateur (pour la copie, par exemple). Il contient le texte sélectionné, ainsi que les balises d’ouverture et les attributs d’un élément qui a une balise de fin dans le texte sélectionné, et des balises de fin à la fin du fragment pour toute balise de début incluse. Il s’agit de toutes les informations requises pour le collage de base d’un fragment HTML.

Le fragment doit être précédé et suivi des commentaires HTML <!--StartFragment--> et <!--EndFragment--> (aucun espace n’est autorisé entre le !--et le texte) pour indiquer facilement où le fragment démarre et se termine. Par conséquent, le début et la fin du fragment sont indiqués par la présence de ces commentaires et par le nombre d’octets StartFragment et EndFragment dans la description. Les outils sont censés produire ces informations. Cette redondance a été introduite pour pouvoir trouver rapidement le début du fragment (à partir du nombre d’octets) et marquer la position du fragment directement dans l’arborescence HTML.

La sélection indique à l’intérieur du fragment la zone HTML exacte que l’utilisateur a sélectionnée (pour la copie, par exemple). Cela ajoute plus d’informations au fragment en indiquant le texte exact sélectionné, sans les balises d’ouverture et de fin qui ont été ajoutées pour s’assurer que le fragment est correctement formé.

La sélection est facultative, car des informations suffisantes sont incluses dans le fragment pour le collage de base. Si la sélection n’est pas stockée, StartSelection et EndSelection ne sont pas stockés dans l’en-tête.

Le contexte est un document HTML valide et complet. Cet article contient le fragment et toutes les balises précédentes adjacentes (balises de début et de fin ; ces balises précédentes représentent tous les nœuds parents du fragment, jusqu’au nœud HTML). L’article contient également l’en-tête complet et permet aux éléments de BASE et de titre, par exemple, d’être inclus afin que ces informations supplémentaires puissent être obtenues. Une application copiant un fragment de code HTML dans le presse-papiers peut choisir de créer un élément de BASE à inclure dans le contexte si ce type d’élément n’est pas déjà présent afin que les URL partielles dans le fragment puissent être résolues.

Le contexte est facultatif, car des informations suffisantes sont incluses dans le fragment pour que le collage de base d’un fragment HTML soit effectué. Si le contexte n’est pas stocké, le fragment est stocké uniquement et StartHTML = endhtml =-1.

## <a name="scenarios"></a>Scénarios

Les scénarios suivants décrivent comment l’éditeur HTML IE4/MSHTML gère les opérations couper-coller HTML. d’autres applications peuvent ou non suivre ces scénarios. Le format du presse-papiers décrit ici est destiné à permettre la flexibilité de la façon dont une application choisit de fonctionner. (Ces scénarios affichent uniquement du code HTML correct, autrement dit, aucune balise qui se chevauche.)

1.  Fragment de code HTML simple.
    -   -   Texte HTML :

            &lt;Le corps est normal. il s’agit de l' &gt; <B> </B> <I> <B>Italique gras </B>. il s’agit </I>de l’italique &lt; /Body&gt;

        -   Apparaît comme suit :

            Ceci est normal. Ceci est **le gras****_italique_* il s’agit* de l’italique  

        -   Le texte entre le \* \* est sélectionné et copié dans le presse-papiers :

            Ceci **est normal.** ceci est le gras \* \* **_italique_** il \* \* *s’agit* de l’italique   

        -   C’est ce qui se trouve dans le presse-papiers (Notez qu’il s’agit de l’interprétation de IE4/MSHTML) :

            Version : 0,9

            StartHTML : 71

            DHTML : 160

            StartFragment : 130

            EndFragment : 150

            **StartSelection : 130**

            **EndSelection : 150**

            <!DOCTYPE ...>

            &lt;ORGANISMES&gt;

            <!-- StartFragment -->>

            **<B>gras</B>en <I><B>italique</B></I>**

            <!-- EndFragment -->

            &lt;/BODY&gt;

            &lt;/HTML&gt;

        -   Dans ce scénario, seule la balise BODY et la balise HTML apparaissent dans le contexte, car elle précède le fragment sélectionné. Notez que les balises de début et de fin sont incluses dans le contexte. La sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.

2.  Fragment d’une table en HTML.
    -   -   Texte HTML :

            &lt;ORGANISMES&gt;<TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Élément 2</TD><TD>Élément 3</TD><TD>Élément 4</TD></TR><TR><TD>Élément 5</TD><TD>Élément 6</TD><TD>Élément 7</TD><TD>Élément 8</TD></TR><TR><TH>Head2</TH><TD>Élément 9</TD><TD>Élément 10</TD><TD>Élément 11</TD><TD>Élément 12</TD></TR></TABLE>&lt;/BODY&gt;

        -   S’affiche sous la forme : ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Élément 2</TD><TD>Élément 3</TD><TD>Élément 4</TD></TR><TR><TD>Élément 5</TD><TD>Élément 6</TD><TD>Élément 7</TD><TD>Élément 8</TD></TR><TR><TH>Head2</TH><TD>Élément 9</TD><TD>Élément 10</TD><TD>Élément 11</TD><TD>Élément 12</TD></TR></TABLE>< ! \[ CDATA\[\]\]>
        -   Les éléments élément 6, Item7, élément 10 et élément 11 de la table sont sélectionnés en tant que bloc et copiés dans le presse-papiers.
        -   C’est ce qui se trouve dans le presse-papiers (Notez qu’il s’agit de l’interprétation de IE4/MSHTML) :

            <!DOCTYPE ...>

            &lt;&gt; &lt; corps HTML&gt;<TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Élément 6 élément </TD> <TD> 7 élément 10 article </TD> </TR> <TR> <TD> </TD> <TD> 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            &lt;/BODY &gt; &lt; /HTML &gt; la sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.

3.  Collage d’un fragment d’une liste triée dans du texte brut.
    -   -   Texte HTML :

            &lt;ORGANISMES&gt;<OL TYPE = a><LI>Item 1<LI>Élément 2<LI>Élément 3<LI>Élément 4<LI>Élément 5<LI>Élément 6</OL>&lt;/BODY&gt;

        -   Apparaît comme suit :
            1.  Item 1
            2.  Élément 2
            3.  Élément 3
            4.  Élément 4
            5.  Élément 5
            6.  Élément 6
        -   L’utilisateur sélectionne et copie les éléments 3 à 5 dans le presse-papiers. Le code HTML suivant se trouve dans le presse-papiers :

            <DOCTYPE... >&lt; &gt; &lt; corps HTML&gt;<OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Élément 3 élément <LI> 4 élément <LI> 5**

            <!-- EndFragment-->

            </OL>&lt;/BODY&gt;&lt;/HTML&gt;

            La sélection, délimitée par StartSelection et EndSelection, est affichée en gras.

        -   Si ce fragment est collé dans un document vide, le code HTML suivant sera créé :

            &lt;ORGANISMES&gt;<OL TYPE = a><LI>Élément 3<LI>Élément 4<LI>Élément 5</OL>&lt;/BODY&gt;

        -   Apparaître comme suit :
            1.  Élément 3
            2.  Élément 4
            3.  Élément 5

4.  Collage d’une zone partiellement sélectionnée.
    -   -   Texte HTML :

            <P> IE4/MSHTML est un éditeur WYSIWYG qui prend en charge les éléments suivants :<UL><LI>Couper<LI>Copier<LI>Coller</UL><P>C’est un excellent outil !

        -   Apparaît comme suit : IE4/MSHTML est un éditeur WYSIWYG qui prend en charge les éléments suivants :
            -   -   Couper
                -   Copier
                -   Coller

        -   L’utilisateur sélectionne « WYSIWYG » jusqu’à « COP ». Le code HTML suivant se trouve dans le presse-papiers :

            <DOCTYPE... >&lt; &gt; &lt; corps HTML&gt;

            <!-- StartFragment-->

            <P>

            **Éditeur WYSIWYG, qui prend en charge**

            **<UL><LI>Couper <LI> COP**

            </UL>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML &gt; la sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.

     
    -   -   L’utilisateur sélectionne « opier » jusqu’à « belle ».

            Le code HTML suivant se trouve dans le presse-papiers :

            <DOCTYPE... >&lt; &gt; &lt; corps HTML&gt;

            <!-- StartFragment-->

            <UL><LI>

            **copier <LI> coller </UL> <P> c’est un excellent**

            </P>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML&gt;

            La sélection, délimitée par StartSelection et EndSelection, s’affiche en gras.

 

 




