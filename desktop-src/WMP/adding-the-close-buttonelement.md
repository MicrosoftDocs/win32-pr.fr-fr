---
title: Ajout du BUTTONELEMENT étroit
description: Ajout du BUTTONELEMENT étroit
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- créer des apparences, BUTTONELEMENT, élément
- Apparences du lecteur Windows Media, BUTTONELEMENT, élément
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons Fermer
- Apparences du lecteur Windows Media, boutons de fermeture
- apparences, boutons Fermer
- fichiers de définition d’apparence, boutons Fermer
- Boutons Fermer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196869"
---
# <a name="adding-the-close-buttonelement"></a>Ajout du BUTTONELEMENT étroit

Le bouton Fermer est similaire au concept de bouton de lecture, mais il a des codes et des couleurs différents.

Placez le code **BUTTONELEMENT** étroit après le crochet pointu fermant du **BUTTONELEMENT** Play.


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



Les attributs suivants sont utilisés pour définir **BUTTONELEMENT** pour le bouton Fermer :

**mappingColor**

Il s’agit de la valeur de couleur de la région dans le fichier art de mappage que vous avez créé précédemment. Dans ce cas, il s’agit de la couleur rouge unie. Cet attribut est obligatoire pour tout **BUTTONELEMENT**. En définissant cette couleur, vous indiquez au lecteur Windows Media d’associer cette zone de couleur au code XML de ce bouton.

**Info-bulle**

Définit le texte qui s’affiche lorsque l’utilisateur pointe la souris sur le bouton. C’est le même que le bouton de lecture, sauf qu’il est étiqueté « Close » (fermer).

**onClick**

Cela définit l’événement qui se produit lorsque la souris clique sur le bouton. La valeur de cet attribut d’événement est appelée gestionnaire d’événements et sera soit une ligne de code Microsoft JScript, soit une fonction JScript dans un fichier texte externe qui est chargée par l’attribut **loadScript** d’une **vue**. Dans ce cas, le code JScript appelle la méthode **Close** de l’élément **View** à l’aide de la **vue** global Attribute, qui ferme la vue et arrête le lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




