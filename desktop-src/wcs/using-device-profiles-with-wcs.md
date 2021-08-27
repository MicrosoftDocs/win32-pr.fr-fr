---
title: Utilisation de profils d’appareil avec WCS
description: Les profils d’appareil sont un outil de base pour la gestion des couleurs.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Système de couleurs (WCS), profils d’appareil
- WCS (Windows Color System), profils d’appareil
- gestion des couleurs des images, profils d’appareil
- gestion des couleurs, profils d’appareil
- couleurs, profils d’appareil
- Windows Système de couleurs (WCS), profils
- WCS (Windows Color System), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- profils d’appareil
- conversion de couleurs
- profils de lien de périphérique
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8211ff883f8e30e7b67b0168e6da980744b252cbb1b89412fc834ac6370cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090069"
---
# <a name="using-device-profiles-with-wcs"></a>Utilisation de profils d’appareil avec WCS

Les profils d’appareil sont un outil de base pour la gestion des couleurs. Un [profil d’appareil](d.md) est un fichier qui contient des informations sur la façon de convertir les couleurs de l’espace de couleurs et la [gamme](./g.md) des couleurs d’un appareil spécifique dans un espace de couleurs indépendant du périphérique. L’espace de couleurs indépendant du périphérique utilisé par ICM2 est appelé espace de connexion de profil (PCS). Un profil d’appareil contient également des informations sur la façon de convertir les couleurs des PC dans l’espace de couleurs et la gamme de couleurs d’un appareil spécifique.

Ces deux ensembles d’informations de conversion sont utilisés pour la [conversion des couleurs](c.md) et la gestion des couleurs. Par exemple, une image peut être créée dans l’espace de couleurs et la gamme de couleurs d’un affichage vidéo. Les informations contenues dans les fichiers de profil de périphérique peuvent être utilisées pour afficher une représentation d’une image imprimée. Les utilisateurs veulent souvent voir à l’écran comment les couleurs sont modifiées lors de l’impression d’une image. C’est ce que l’on appelle la vérification. Une image peut être vérifiée en convertissant les couleurs de la gamme de couleurs source (l’écran) en couleurs de [PC](p.md) , puis en les convertissant à partir des PC dans la gamme de couleurs de destination (l’imprimante). L’image résultante peut être affichée à l’écran, ce qui permet à l’utilisateur de voir à quoi ressemblera l’image finale lorsqu’il sera imprimé.

Les profils d’appareil permettent également des utilisations plus complexes. Par exemple, ils peuvent être utilisés pour obtenir une idée de ce à quoi ressemble une image créée sur un écran vidéo lorsqu’elle est imprimée sur une imprimante laser haute résolution. L’exemple devient plus complexe s’il n’y a qu’une imprimante à jet d’encre standard sur laquelle la vérifier. ICM2 convertit l’image de la [gamme](./g.md) de l’affichage, dans la gamme de l’imprimante à jet d’encre. À partir de là, il est converti en gamme de l’imprimante laser. L’image résultante peut être imprimée sur l’imprimante à jet d’encre. Bien sûr, l’image serait à une résolution plus élevée lorsqu’elle est imprimée sur l’imprimante laser couleur. Toutefois, les couleurs de l’image de vérification imprimée sur l’imprimante à jet d’encre sont une correspondance proche des couleurs que l’imprimante laser peut imprimer.

Les conversions d’un profil d’appareil peuvent être concaténées ensemble en un seul fichier, appelé *profil de lien de périphérique*. Si une série de conversions est utilisée à plusieurs reprises, la création d’un profil de lien de périphérique pour ceux-ci raccourcit le temps de conversion.

Les profils d’appareil peuvent être gérés. La gestion des profils est le processus qui consiste à associer des profils de couleur à des instances d’appareil. Tout périphérique de sortie en couleur peut avoir un ensemble d’un ou plusieurs profils de couleurs associés. Les fabricants de matériel et les tiers qui fournissent des profils de couleurs doivent effectuer la gestion des profils.

Les ensembles de profils peuvent être partagés entre les appareils ou dédiés à des appareils spécifiques. Supposons, par exemple, que vous ayez deux imprimantes couleur du même modèle. Chaque imprimante nécessite un ensemble de profils de couleurs à associer. L’ensemble de profils de couleurs pour une imprimante correspond aux différentes configurations possibles dans ce modèle. Dans le même modèle, les deux imprimantes peuvent partager un ensemble de profils. L’alternative consiste à attribuer à chaque imprimante son propre jeu de profils distinct. Dans ce dernier cas, les profils de couleurs de l’ensemble peuvent être étalonnés précisément sur la sortie individuelle de l’imprimante, et pas seulement sur les caractéristiques de sortie générales du modèle.

Il existe trois classes différentes de profils ICC : les profils d’entrée, les profils d’affichage et les profils de sortie. Les profils d’entrée sont généralement associés à un appareil, tel qu’un scanneur. Les profils d’affichage sont généralement associés à un moniteur d’ordinateur. Les profils de sortie sont généralement associés aux imprimantes.

La spécification autorise également les profils d’appareil, les profils abstraits, les profils de lien de périphérique, les profils de couleurs nommés et les profils d’espace colorimétrique.

Un profil d’appareil décrit l’espace colorimétrique d’un appareil particulier.

Un profil abstrait fournit une méthode générique permettant aux utilisateurs de modifier les couleurs subjectives des images ou des objets graphiques en transformant les données de couleur sur les PC.

Comme mentionné précédemment, un profil de lien de périphérique concatène une série de profils dans une transformation.

Les profils de couleurs nommés peuvent être considérés comme des profils frères pour les profils d’appareil. Pour un appareil donné, il existe un ou plusieurs profils d’appareil pour gérer les conversions de couleurs de processus et un ou plusieurs profils de couleurs nommés pour gérer les couleurs nommées. Il peut y avoir plusieurs profils de couleurs nommés pour tenir compte de différents consommables ou de plusieurs fournisseurs de couleurs nommées.

Un profil d’espace colorimétrique décrit un espace de couleurs indépendant du périphérique.

Le tableau suivant récapitule les différents types de profils.



| Type de profil        | Description                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Profil abstrait    | Profil ajusté pour répondre aux préférences particulières d’un utilisateur.                                                     |
| Profil d’espace colorimétrique | Profil qui décrit un espace de couleurs indépendant du périphérique.                                                                    |
| Profil de lien de l’appareil | Série de profils concaténés dans un seul profil.                                                    |
| Profil d’appareil      | Profil décrivant l’espace colorimétrique d’un appareil particulier.                                                              |
| Profil d’affichage     | Classe ou catégorie de profils qui comprend tout type de profil associé à un affichage.                                  |
| Profil d’entrée       | Classe ou catégorie de profils qui comprend tout type de profil associé à un périphérique d’entrée, tel qu’un scanneur.          |
| Profil de couleurs nommé | Profil pour un espace de couleurs qui se compose de couleurs nommées.                                                                    |
| Profils de sortie     | Classe ou catégorie de profils qui comprend tout type de profil associé à un périphérique de sortie papier tel qu’une imprimante. |



 

Les transformations de couleur peuvent être créées avec un ou plusieurs profils. Si une transformation est créée avec un seul profil, le profil doit être un profil de liaison d’appareil. Une transformation peut également avoir deux profils ou plus dans une chaîne. Si c’est le cas, il ne peut pas contenir de profils de liaison d’appareil. Les profils abstraits ne peuvent être qu’au milieu de la chaîne. Les premier et dernier profils doivent être des profils d’appareil ou des profils d’espace colorimétrique.

 

 