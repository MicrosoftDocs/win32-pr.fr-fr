---
title: Ajout du BUTTONELEMENT étroit
description: Ajout du BUTTONELEMENT étroit
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- créer des apparences, BUTTONELEMENT, élément
- habillages Lecteur Windows Media, élément BUTTONELEMENT
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons Fermer
- apparences de Lecteur Windows Media, boutons fermer
- apparences, boutons Fermer
- fichiers de définition d’apparence, boutons Fermer
- Boutons Fermer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765473"
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

Il s’agit de la valeur de couleur de la région dans le fichier art de mappage que vous avez créé précédemment. Dans ce cas, il s’agit de la couleur rouge unie. Cet attribut est obligatoire pour tout **BUTTONELEMENT**. en définissant cette couleur, vous indiquez Lecteur Windows Media pour associer cette zone de couleur au code XML de ce bouton.

**Info-bulle**

Définit le texte qui s’affiche lorsque l’utilisateur pointe la souris sur le bouton. C’est le même que le bouton de lecture, sauf qu’il est étiqueté « Close » (fermer).

**onClick**

Cela définit l’événement qui se produit lorsque la souris clique sur le bouton. la valeur de cet attribut d’événement est appelée un gestionnaire d’événements et sera soit une ligne de code JScript Microsoft, soit une fonction JScript dans un fichier texte externe qui est chargé par l’attribut **loadScript** d’une **vue**. dans ce cas, le code JScript appelle la méthode **close** de l’élément **view** à l’aide de la **vue** global attribute, qui ferme la vue et arrête Lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




