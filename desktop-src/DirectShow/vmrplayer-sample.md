---
description: Exemple VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemple VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863398"
---
# <a name="vmrplayer-sample"></a>Exemple VMRPlayer

## <a name="description"></a>Description

Cet exemple utilise le filtre de mixage vidéo 9 (VMR-9) pour mélanger alpha une ou deux vidéos en cours d’exécution et une image statique.

## <a name="usage"></a>Utilisation

Pour ouvrir la première vidéo, choisissez **ouvrir le flux principal** dans le menu **fichier** . Pour ouvrir une deuxième vidéo, choisissez **ouvrir un flux secondaire** dans le menu **fichier** (vous devez d’abord ouvrir le flux de données principal). Pour lire la vidéo, cliquez sur le bouton **lecture** .

Vous pouvez définir la position, la taille et les valeurs alpha des vidéos en sélectionnant **flux principal** ou **flux Secondard** dans le menu **Propriétés de VMR** .

Pour ajouter une image bitmap statique sur la vidéo, choisissez **image d’application statique** dans le menu **Propriétés de VMR** , puis cliquez sur la zone afficher l’image de l' **application** . Vous pouvez utiliser la même boîte de dialogue pour contrôler la position, la taille et la valeur alpha de la bitmap.

Pour capturer l’image vidéo fusionnée, choisissez **capturer l’image bitmap** dans le menu **Propriétés de VMR** .

Vous pouvez également spécifier le flux de l’image principale à partir de la ligne de commande :

**VMRPlayer** **/p** *nom_fichier*

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



