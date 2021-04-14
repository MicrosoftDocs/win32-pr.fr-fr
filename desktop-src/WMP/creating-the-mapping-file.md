---
title: Création du fichier de mappage
description: Création du fichier de mappage
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- création d’apparences, mappage de fichiers
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, mappage d’images
- Apparences du lecteur Windows Media, mappage d’images
- apparences, mappage d’images
- mappage d’images dans des apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379620"
---
# <a name="creating-the-mapping-file"></a>Création du fichier de mappage

Une fois que vous avez créé les éléments de votre fichier art principal, il est relativement facile de créer un fichier de mappage. Vous allez créer le nouveau fichier de mappage en combinant l’image des deux couches de bouton que vous avez déjà créées.

1.  Vous devrez prendre les deux boutons que vous avez créés pour le fichier art principal et les copier dans une nouvelle couche. Procédez comme suit : copiez la couche du bouton Fermer, supprimez tous les effets de couche, puis renommez-la « fermer le mappage ». L’illustration doit paraître plate, sans biseau.
2.  Utilisez le sélecteur de couleurs pour créer une couleur de premier plan du rouge pur. Assurez-vous que la valeur du numéro de couleur est « \# FF0000 ». Utilisez ensuite l’outil Pot de peinture pour remplir l’intérieur du cercle de la couche de fermeture de la carte.
3.  Copiez la couche du bouton de lecture, supprimez tous les effets de couche, puis renommez-la « Play map ». Là encore, l’art doit paraître plat. Vous ne souhaitez pas d’effets dans la couche de mappage, car vous définissez simplement des régions de la bitmap que le lecteur Windows Media utilisera pour déterminer où la souris effectue une action et ce que vous souhaitez en faire.
4.  Utilisez le sélecteur de couleurs pour créer une couleur de premier plan du vert pur. Assurez-vous que la valeur du numéro de couleur est « \# 00FF00 ». Utilisez ensuite l’outil Pot de peinture pour remplir l’intérieur du cercle de la couche de lecture.

Vous êtes maintenant prêt à créer le fichier art de mappage. Masquer toutes les couches, puis afficher uniquement les couches suivantes, dans cet ordre (de haut en bas) :

Lire le mappage

Fermer le mappage

Enregistrez dans un nouveau fichier à l’aide de la commande Enregistrer une copie du menu fichier. Sélectionnez l’option BMP dans la partie enregistrer sous de la boîte de dialogue Enregistrer une copie et tapez un nom de fichier auquel vous allez vous référer ultérieurement dans votre fichier de définition d’apparence. Dans l’idéal, il doit se trouver dans le même répertoire que votre fichier de définition d’apparence. Par exemple, vous pouvez appeler ce fichier map.bmp. Choisissez les paramètres par défaut et enregistrez le fichier.

Votre fichier de mappage doit ressembler à l’illustration suivante.

![Fichier de mappage](images/g01map.png)

Comme vous pouvez le deviner, la zone verte est utilisée pour déterminer le moment où le lecteur Windows Media démarre et la zone rouge pour indiquer qu’il doit s’arrêter. Les deux couleurs peuvent être utilisées, à condition que vous utilisiez les numéros de couleur lorsque vous configurez le fichier de définition d’apparence. Assurez-vous que les couleurs de la carte sont des couleurs pures pour la région que vous souhaitez utiliser et que vous avez des bords distincts. Une couleur pure est une couleur où chaque pixel d’une zone a la même valeur de couleur. L’utilisation d’un effet peut atténuer ou déformer le bord, ce qui modifie légèrement les couleurs de certains pixels. Le fichier de mappage n’est visible que par la souris, pas par un homme, donc ne vous ne devez pas le décorer, et supprimez les effets de couche que vous avez pu effectuer à partir d’autres couches.

Lorsque vous enregistrez votre fichier, le nom de fichier que vous choisissez sera ultérieurement utilisé comme valeur de l’attribut **mappingImage** de l’élément **BUTTONGROUP** dans votre fichier de définition d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de votre première apparence**](building-your-first-skin.md)
</dt> </dl>

 

 




