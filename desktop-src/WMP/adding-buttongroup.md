---
title: Ajout de BUTTONGROUP
description: Ajout de BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- création d’apparences, élément BUTTONGROUP
- habillages Lecteur Windows Media, élément BUTTONGROUP
- habillages, élément BUTTONGROUP
- fichiers de définition d’apparence, élément BUTTONGROUP
- Élément BUTTONGROUP
- éléments, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865188"
---
# <a name="adding-buttongroup"></a>Ajout de BUTTONGROUP

Cet exemple utilise l’élément **BUTTONGROUP** pour le codage dans le fichier de définition d’apparence. **BUTTONGROUP** crée un moyen simple de traiter des événements de souris sans avoir à calculer des emplacements exacts sur l’écran et utilise la couleur au lieu des coordonnées x et y.

Tout d’abord, vous devez ajouter les balises **BUTTONGROUP** au fichier de définition d’apparence que vous avez créé. Placez-les après les attributs de balise de **thème** .


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Laissez quelques lignes vides au-dessus de la balise de fermeture **BUTTONGROUP** pour les boutons que vous ajouterez ensuite.

Les attributs suivants sont utilisés pour définir **BUTTONGROUP**:

**mappingImage**

Il s’agit du nom de fichier du fichier d’illustration de mappage que vous avez créé précédemment, celui avec les cercles rouge et vert. Cet attribut est obligatoire pour les **BUTTONGROUP**.

**hoverImage**

Il s’agit du nom de fichier du fichier image de survol que vous avez créé précédemment, celui avec les deux boutons jaunes qui lisent « lire » et « fermer ». Ce n’est pas obligatoire, mais une image de survol permet de fournir des commentaires à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




