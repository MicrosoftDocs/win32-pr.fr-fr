---
title: Exemple d’art simple
description: Exemple d’art simple
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- habillages Lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les habillages, exemples
- skins Lecteur Windows Media, exemples
- Skins, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615949"
---
# <a name="simple-art-example"></a>Exemple d’art simple

Trois fichiers art sont nécessaires pour créer une apparence simple avec deux boutons. Une image principale et une image de mappage sont nécessaires, et une autre image fournit à l’utilisateur un signal visuel permettant à l’utilisateur de cliquer sur un bouton.

Ces fichiers art ont été créés dans un programme art qui utilise des couches. Grâce aux couches, vous pouvez facilement vous assurer que vos images principales, de mappage et de remplacement sont toutes de la même taille et être alignées les unes avec les autres.

Les instructions détaillées sur la création de l’illustration sont dans le [Guide de création d’apparence](skin-creation-guide.md).

## <a name="primary-image"></a>Image principale

l’image principale est une ellipse jaune simple avec deux boutons, une couleur rose à démarrer Lecteur Windows Media et un bouton violet pour l’arrêter. L’arrière-plan est légèrement plus sombre que l’ovale. Cette image est représentée dans l’illustration suivante.

![image principale](images/absam01b.png)

L’image principale provient des images suivantes, chacune dans une couche distincte. Tout d’abord, un ovale a été créé avec un effet biseau et relief de couche. Cette image est représentée dans l’illustration suivante.

![image ovale](images/absam01s.png)

Les deux boutons ont été créés, ainsi que les effets de biseau et de relief de couche. L'illustration ci-dessous décrit cela.

![deux boutons](images/absam01p.png)

Ensuite, l’arrière-plan de l’image a été créé. Un jaune légèrement plus sombre a été choisi afin que tout anticrénelage entre l’ovale et l’arrière-plan ne soit pas remarqué. La valeur de couleur est \# CCCC00. Cette image est représentée dans l’illustration suivante.

![image d’arrière-plan](images/absam01y.png)

Les couches qui contiennent ces images ont été rendues visibles et enregistrées sous forme de copie au format bitmap, créant ainsi l’image principale. L’image composite principale sera utilisée par l’attribut **BackgroundImage** de l’élément **View** .

## <a name="mapping-image"></a>Image de mappage

Une image de mappage est nécessaire pour spécifier quand et où un clic est effectué sur une apparence. Une image de mappage a été créée avec une zone rouge et une zone verte. Cette image est représentée dans l’illustration suivante.

![image de mappage](images/absam01m.png)

la zone verte sera utilisée pour identifier la zone de l’apparence qui démarrera Lecteur Windows Media et la zone rouge sera utilisée pour l’arrêter. L’image de mappage a la même taille que l’image principale.

L’image de mappage a été créée en copiant la couche de bouton sur une nouvelle couche et en désactivant l’effet de biseau et de relief. les images plates sont nécessaires pour le mappage, car Lecteur Windows Media recherchera des valeurs de couleur uniques dans chaque zone. Elle peut uniquement Rechercher une couleur que vous définissez, telle que le rouge ( \# FF0000). Si votre image a un biseau ou un autre effet, ce n’est pas tout ce dont vous avez besoin.

Pour que les boutons de mappage aient une couleur facile à mémoriser, les images ont été remplies avec du rouge pur et du vert pur, mais toute couleur peut être utilisée. Vous devez mémoriser les numéros de couleur de votre mappage afin qu’ils puissent être entrés dans le fichier de définition d’apparence XML. Dans ce cas, Red est \# FF0000 et Green est \# 00FF00.

Ensuite, lorsque seule la nouvelle couche est visible, l’image a été enregistrée en tant que copie dans un fichier BMP. Elle est appelée par l’attribut **mappingImage** de l’élément **BUTTONGROUP** .

## <a name="alternate-image"></a>Image de remplacement

Les autres images ne sont pas requises, mais elles sont très utiles pour fournir des signaux visuels à l’utilisateur. Dans ce cas, il est recommandé d’utiliser une image de survol afin que l’utilisateur sache quelles zones peuvent être cliquées.

Une image de remplacement a été créée avec deux boutons jaunes. L'illustration ci-dessous décrit cela.

![image de survol](images/absam01h.png)

L’image de remplacement a été créée en copiant la couche de bouton d’origine sur une nouvelle couche, puis en remplaçant la couleur de remplissage par jaune. L’effet de biseau et de relief était conservé. Une nouvelle couche a été créée et des images ont été ajoutées : la flèche indique « Play » et le carré indique « stop ». Ensuite, avec uniquement les nouveaux boutons jaunes et les couches de type visibles, l’image a été enregistrée en tant que copie dans un fichier bitmap.

le résultat est que lorsque la souris pointe sur une zone définie par l’image de mappage, l’image de survol s’affiche et avertit le lecteur que s’il clique sur cet endroit, il peut lire ou arrêter Lecteur Windows Media.

## <a name="final-image"></a>Image finale

Voici l’image finale de l’apparence.

![image finale](images/absam01f.png)

Il s’agit de l’image que vous verrez si vous pointez sur le bouton rose à droite.

![bouton pointer sur la droite](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Code XML pour l’exemple de motif

Les détails de l’écriture de code XML sont fournis dans le [Guide de création d’apparence](skin-creation-guide.md), mais pour montrer la quantité de code nécessaire pour créer une apparence de travail, voici le code de l’illustration dans cet exemple.

Les boutons prédéfinis sont utilisés pour les fonctions de lecture et d’arrêt. vous devez charger un fichier ou une sélection à partir de l’ancre de support Windows. lorsque Lecteur Windows Media passe en mode apparence, une petite zone s’affiche dans le coin inférieur droit de l’écran. Cette zone est appelée « ancre ». le fait de cliquer sur l’ancre vous donne les fonctionnalités minimales nécessaires, au cas où une apparence ne permet pas de revenir au mode complet de Lecteur Windows Media. L’utilisateur peut basculer entre les modes en utilisant le menu **affichage** en mode complet ou en cliquant sur le point d’ancrage en mode apparence.


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files.md)
</dt> </dl>

 

 




