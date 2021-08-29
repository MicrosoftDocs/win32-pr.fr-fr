---
description: Les programmes de lecture d’écran peuvent uniquement lire le texte d’un contrôle RadioButtonGroup qui a été créé dans la colonne text de la table RadioButton.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Ajout de texte supplémentaire aux cases d’option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a1274faeffc3bf98702cc6f549e0be02e0d1d1ba003914d295e4fe004aa39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145982"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Ajout de texte supplémentaire aux cases d’option

Les programmes de lecture d’écran peuvent uniquement lire le texte d’un [contrôle RadioButtonGroup](radiobuttongroup-control.md) qui a été créé dans la colonne text de la [table RadioButton](radiobutton-table.md). Si ce texte est une description insuffisante des cases d’option, des [contrôles de texte](text-control.md) se chevauchant peuvent être ajoutés pour fournir du texte descriptif supplémentaire. Ces contrôles de texte doivent se chevaucher dans la boîte de dialogue et comporter des conditions définies dans la [table ControlCondition](controlcondition-table.md) de sorte qu’un seul contrôle de texte s’affiche à la fois. Les contrôles de texte ne doivent pas chevaucher le contrôle RadioButtonGroup ou d’autres contrôles dans la boîte de dialogue, car cela rend les contrôles invisibles pour les lecteurs d’écran. Lorsque l’utilisateur place le curseur sur le contrôle de texte, le programme de lecture d’écran lit le texte supplémentaire.

Dans l’exemple suivant, la boîte de dialogue MySample contient un contrôle RadioButtonGroup nommé couleurs avec deux options pour la valeur de la propriété TheColor. Pour chaque choix, il existe un contrôle de texte avec une condition à masquer ou à afficher, selon le choix actuel sélectionné pour TheColor. Une valeur TheColor initiale est définie dans la table de propriétés. Les contrôles de texte ont le texte descriptif supplémentaire créé dans le champ de texte de la table de RadioButton. Quand un utilisateur place le curseur sur le contrôle de texte dans la boîte de dialogue, le lecteur d’écran peut lire la description supplémentaire du choix actuel.

[Table de boîtes de dialogue](dialog-table.md)



| Boîte de dialogue   | HCentering | VCentering | Largeur | Hauteur | Attributs | Titre                    | \_Premier contrôle | \_Valeur par défaut du contrôle | Annuler le contrôle \_ |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Cases d’option accessibles | Couleurs         | Suivant             |                 |



 

[Table de contrôle](control-table.md)



| Boîte de dialogue\_ | Contrôler    | Type             | X   | O   | Largeur | Hauteur | Attributs | Propriété | Texte                               | Contrôle \_ suivant | Aide |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Couleurs     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | TheColor |                                    | Suivant          |      |
| MySample | HowIsBlue  | Texte             | 20  | 80  | 150   | 15     | 2          |          | C’est comme le ciel à un jour clair. |               |      |
| MySample | HowIsGreen | Texte             | 20  | 80  | 150   | 15     | 2          |          | C’est comme herbe dans le ressort.    |               |      |



 

[Table RadioButton](radiobutton-table.md)



| Propriété | Commande | Valeur | X   | O   | Largeur | Hauteur | Texte   | Aide |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| TheColor | 1     | Bleu  | 10  | 10  | 80    | 15     | &bleu  |      |
| TheColor | 2     | Vert | 10  | 30  | 80    | 15     | &vert |      |



 

[Table de propriétés](property-table.md)



| Propriété | Valeur |
|----------|-------|
| TheColor | Bleu  |



 

[Table ControlCondition](controlcondition-table.md)



| Boîte de dialogue\_ | contrôle\_  | Action | Condition                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | Masquer   | TheColor <>  « Blue »  |
| MySample | HowIsBlue  | Afficher   | TheColor = "Blue"         |
| MySample | HowIsGreen | Masquer   | TheColor <>  « Green » |
| MySample | HowIsGreen | Afficher   | TheColor = "Green"        |



 

Pour plus d’informations, consultez [accessibilité](accessibility.md).

 

 



