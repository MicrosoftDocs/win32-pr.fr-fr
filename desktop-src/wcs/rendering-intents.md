---
title: Rendu des intentions
description: Le consortium de couleurs internationaux (ICC) a défini quatre valeurs différentes, appelées intentions de rendu.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), rendu des intentions
- WCS (Windows Color System), rendu des intentions
- gestion des couleurs des images, rendu des intentions
- gestion des couleurs, rendu des intentions
- couleurs, rendu des intentions
- rendu des intentions
- ICC (International Color Consortium)
- IIC (International Color Consortium)
- Intention de l’image
- Intention graphique
- Intention de preuve
- Intention de correspondance
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523765"
---
# <a name="rendering-intents"></a>Rendu des intentions

Le consortium de couleurs internationaux (ICC) a défini quatre valeurs différentes, appelées *intentions de rendu*. Elles représentent quatre approches différentes de la création d’un rendu des couleurs. Ces quatre intentions, ainsi que les constantes utilisées pour y faire référence dans le code, sont les suivantes.



| Intentionnel                            | Nom ICC              | Description                    |
|-----------------------------------|-----------------------|--------------------------------|
| Image | Perceptuelles            | \_perception intentionnelle             |
| Graphic | Saturation            | \_saturation intentionnelle             |
| Proof     | Colorimétrie relative | \_Colorimétrie relative à l’intention \_ |
| Correspond     | Colorimétrie absolue | \_Colorimétrie absolue \_ intentionnelle |




 

La spécification de format de profil ICC version 3,4, qui décrit ces intentions, peut être téléchargée à partir de color.org.

## <a name="picture-intent"></a>Intention de l’image

Appelée « intention de perception » dans la clause de la spécification ICC 4,9, un motif d’image permet de compresser ou d’étendre la [gamme](./g.md) complète de l’image pour remplir la gamme de l’appareil de destination, de sorte que la balance grise soit préservée mais que la précision colorimétrique ne puisse pas être préservée.

En d’autres termes, si certaines couleurs d’une image se trouvent en dehors de la plage de couleurs que l’appareil de sortie peut afficher, l’intention de l’image est ajustée de façon à ce que toutes les couleurs de l’image se trouvent dans la plage qui peut être rendue et que la relation entre les couleurs soit conservée autant que possible.

Cet objectif est particulièrement adapté à l’affichage des photographies et des images, et est généralement l’intention par défaut.

## <a name="graphic-intent"></a>Intention graphique

La clause de la spécification ICC 4,12 appelle l’intention graphique une intention de [saturation](s.md) . Il conserve la chrominance des couleurs dans l’image au détriment de la [teinte](h.md) et de la [luminosité](l.md).

L’implémentation de cette intention reste un peu problématique, et la ICC continue de fonctionner sur les méthodes pour atteindre les effets souhaités.

Cet objectif est particulièrement adapté aux graphiques professionnels tels que les graphiques, où il est plus important que les couleurs soient éclatantes et contrastées les unes avec les autres plutôt qu’une couleur spécifique.

## <a name="proof-intent"></a>Intention de preuve

L’intention de la preuve, appelée intention de colorimétrie dans la spécification ICC, est définie de telle sorte que toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut restituer soient ajustées à la couleur la plus proche qui peut être rendue, alors que toutes les autres couleurs restent inchangées.

L’intention de la preuve ne préserve pas le [point blanc](w.md).

Par exemple, le blanc le plus blanc d’un papier est plus jaune que le blanc le plus blanc d’un moniteur d’ordinateur. Une image convertie dans la gamme de l’imprimante à l’aide d’une intention de Colorimétrie relative entraînerait une plus grande couleur pour toutes les couleurs. Le point blanc de l’image est déplacé pour correspondre au point blanc de l’imprimante. Toutes les autres couleurs de l’image conservent leur position par rapport au point blanc. Cela produit une image qui reflète de manière plus précise l’aspect de l’image imprimée. Toutefois, l’utilisateur peut se déconcerter visuellement.

## <a name="match-intent"></a>Intention de correspondance

Dans un but de correspondance, toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut restituer sont ajustées à la couleur la plus proche qui peut être rendue, alors que toutes les autres couleurs restent inchangées. La spécification ICC appelle l’intention de l’intention de correspondance absolue colorimétrie.

L’intention de correspondance conserve le point blanc.

Par exemple, le blanc le plus blanc d’un papier est plus jaune que le blanc le plus blanc d’un moniteur d’ordinateur. Une image convertie dans la [gamme](./g.md) de l’imprimante à l’aide de la fonction match a pour résultat que toutes les couleurs sont converties et mises en correspondance avec la gamme de l’imprimante. Le point blanc de l’image n’est pas déplacé pour correspondre au point blanc de l’imprimante. Par conséquent, la distance entre les couleurs et le point blanc peut changer. Cela produit une image qui est moins visuellement déconcertée pour l’utilisateur, mais qui est également un rendu moins précis de la sortie de l’imprimante.

 

 