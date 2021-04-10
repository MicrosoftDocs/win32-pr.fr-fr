---
title: Création de l’image de survol
description: Création de l’image de survol
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- création d’apparences, images de survol
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, les images de survol
- Apparences du lecteur Windows Media, images de survol
- apparences, images de survol
- images de survol dans les enveloppes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d7f5bbb8b57820c2805b9b9d6ea79762933035
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309297"
---
# <a name="creating-the-hover-image"></a>Création de l’image de survol

L’image principale de cette apparence est deux boutons assis sur un ovale. Pour permettre à l’utilisateur d’obtenir un indice sur la marche à suivre, vous pouvez ajouter des images de pointage. Il s’agit d’images de remplacement qui s’affichent lorsque l’utilisateur place le pointeur de la souris sur un bouton. Les boutons sensitifs contiennent également les symboles de contrôle Play et Stop VCR pour que les utilisateurs sachent exactement ce qu’ils peuvent faire. L’utilisation d’images de survol vous permet de créer des enveloppes artistiques complexes, auto-documentées.

Pour créer l’image de survol, vous devez prendre les deux boutons que vous avez créés pour le fichier art principal, les copier dans de nouvelles couches et ajouter d’autres couches pour le texte. Utiliser les étapes suivantes :

1.  Copiez la couche du bouton Fermer et renommez-la « fermer le pointage ».
2.  Utilisez le sélecteur de couleurs pour créer une couleur de premier plan d’un jaune clair ( \# CCFF33). Cela a été choisi pour comparer avec les couleurs de bouton. Utilisez ensuite l’outil Pot de peinture pour remplir l’intérieur du cercle dans la couche de survol.
3.  Copiez la couche du bouton de lecture et renommez-la « lire le pointage ».
4.  Utilisez l’outil Pot de peinture pour remplir l’intérieur du cercle dans la couche de pointage de lecture avec la même couleur que le cercle de survol.
5.  Créez une nouvelle couche et nommez-la « fermer le carré ». Utilisez le sélecteur de couleurs pour créer une couleur de premier plan du bleu foncé. Utilisez l’outil plume pour dessiner un carré, le transformer en sélection, le remplir et supprimer le tracé. À l’aide de l’outil déplacement, déplacez le carré et centrez-le sur le bouton de survol.
6.  Créez une nouvelle couche et nommez-la « triangle de lecture ». Utilisez l’outil plume pour créer le triangle pour la « lecture » en utilisant les mêmes techniques que celles que vous avez utilisées pour créer la couche carrée de fermeture. Centrez-le sur le bouton de lecture.

Vous êtes maintenant prêt à créer le fichier art de survol. Masquer toutes les couches, puis afficher uniquement les couches suivantes, dans cet ordre (de haut en bas) :

Triangle de lecture

Fermer le carré

Lire le pointage

Fermer le pointage

Enregistrez dans un nouveau fichier à l’aide de la commande Enregistrer une copie du menu fichier. Sélectionnez l’option BMP dans la partie enregistrer sous de la boîte de dialogue Enregistrer une copie, puis tapez un nom de fichier auquel vous allez vous référer ultérieurement dans votre fichier de définition d’apparence. Dans l’idéal, vous devez enregistrer ce fichier dans le même répertoire que votre fichier de définition d’apparence. Par exemple, vous pouvez appeler cette hover.bmp. Choisissez les paramètres par défaut et enregistrez le fichier.

Votre fichier art au survol doit ressembler à l’illustration suivante.

![image de survol](images/absam01h.png)

Le bouton sensitif jaune s’affiche à la place du bouton normal. Si vous pointez sur le bouton droit de votre apparence, le bouton jaune intitulé « lecture » s’affiche et, si vous pointez sur le bouton gauche, l’utilisateur verra « fermer ». Les deux images de survol ne seront jamais affichées en même temps, car la souris ne peut pas pointer sur les deux boutons en même temps. Vous devez activer le pointage et disposer d’un fichier image de survol qui correspond aux zones des fichiers de mappage aux zones du fichier de survol.

Lorsque vous enregistrez votre fichier, le nom de fichier que vous choisissez sera ultérieurement utilisé comme valeur de l’attribut **hoverImage** de l’élément **BUTTONGROUP** dans votre fichier de définition d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de votre première apparence**](building-your-first-skin.md)
</dt> </dl>

 

 




